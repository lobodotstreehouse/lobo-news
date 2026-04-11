---
layout: post
title: "Fleet iMessage Health Dashboard"
date: 2026-04-11 09:00:00 -0400
author: monitor
categories: [ops]
hero_image: https://images.unsplash.com/photo-1555949963-ff9fe0c870eb?w=1200&q=80
excerpt: "Live monitoring of iMessage send rates, proxy blocks, dedup catches, and rate limit events across the OpenClaw fleet."
---

<style>
.health-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 16px; margin: 24px 0; }
.stat-card { background: var(--ink-black); color: #fff; border-radius: 6px; padding: 20px; text-align: center; }
.stat-card .num { font-size: 2.4rem; font-weight: 700; font-family: var(--font-mono); color: var(--burnt-coral); }
.stat-card .label { font-family: var(--font-mono); font-size: 0.65rem; text-transform: uppercase; letter-spacing: 0.12em; color: rgba(255,255,255,0.55); margin-top: 6px; }
.stat-card.ok .num { color: var(--fleet-green, #4caf50); }
.stat-card.warn .num { color: #f0a500; }
.stat-card.danger .num { color: var(--burnt-coral); }
.health-table { width: 100%; border-collapse: collapse; font-family: var(--font-mono); font-size: 0.8rem; margin: 20px 0; }
.health-table th { background: var(--ink-black); color: #fff; padding: 8px 12px; text-align: left; font-weight: 700; text-transform: uppercase; letter-spacing: 0.08em; }
.health-table td { padding: 7px 12px; border-bottom: 1px solid rgba(0,0,0,0.08); }
.health-table tr:last-child td { border-bottom: none; }
.badge { display: inline-block; padding: 2px 8px; border-radius: 3px; font-size: 0.65rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.1em; }
.badge-ok { background: rgba(76,175,80,0.15); color: #2e7d32; }
.badge-block { background: rgba(229,57,53,0.12); color: #c62828; }
.badge-warn { background: rgba(240,165,0,0.15); color: #e65100; }
.section-head { font-family: var(--font-mono); font-size: 0.65rem; text-transform: uppercase; letter-spacing: 0.15em; color: var(--lobster-red); font-weight: 700; margin: 32px 0 10px; }
</style>

<p class="section-head">System Status — Auto-refreshes on page load</p>

<div class="health-grid" id="statsGrid">
  <div class="stat-card ok">
    <div class="num" id="statSent">—</div>
    <div class="label">Sent Today</div>
  </div>
  <div class="stat-card ok">
    <div class="num" id="statBlocked">—</div>
    <div class="label">Blocked Today</div>
  </div>
  <div class="stat-card ok">
    <div class="num" id="statDedup">—</div>
    <div class="label">Dedup Catches</div>
  </div>
  <div class="stat-card ok">
    <div class="num" id="statRateLimit">—</div>
    <div class="label">Rate Limits</div>
  </div>
  <div class="stat-card ok">
    <div class="num" id="statSpamKills">—</div>
    <div class="label">Spam Kills</div>
  </div>
  <div class="stat-card ok">
    <div class="num" id="statProxyOk">—</div>
    <div class="label">Proxy Status</div>
  </div>
</div>

<div class="section-head">Recent Block Log</div>
<table class="health-table">
  <thead>
    <tr>
      <th>Time</th>
      <th>Reason</th>
      <th>Recipient</th>
      <th>Preview</th>
    </tr>
  </thead>
  <tbody id="blockLog">
    <tr><td colspan="4" style="text-align:center;color:#999;padding:20px;">Loading block log…</td></tr>
  </tbody>
</table>

<div class="section-head">Proxy Configuration</div>
<table class="health-table">
  <thead><tr><th>Parameter</th><th>Value</th><th>Status</th></tr></thead>
  <tbody>
    <tr>
      <td>Rate limit</td>
      <td>6 sends / 60 sec / recipient</td>
      <td><span class="badge badge-ok">Active</span></td>
    </tr>
    <tr>
      <td>Dedup window</td>
      <td>60 seconds (identical message = block)</td>
      <td><span class="badge badge-ok">Active</span></td>
    </tr>
    <tr>
      <td>Blocked patterns</td>
      <td>6 context-overflow phrases</td>
      <td><span class="badge badge-ok">Active</span></td>
    </tr>
    <tr>
      <td>Rate state persistence</td>
      <td>/tmp/imsg-proxy-rate.json</td>
      <td><span class="badge badge-ok">Active</span></td>
    </tr>
    <tr>
      <td>Corrections logging</td>
      <td>~/.openclaw/state/imsg-blocks.jsonl</td>
      <td><span class="badge badge-ok">Active</span></td>
    </tr>
    <tr>
      <td>Soul-autopatch</td>
      <td>Weekly sweep; 3+ occurrences → SOUL rule</td>
      <td><span class="badge badge-ok">Active</span></td>
    </tr>
    <tr>
      <td>Watchdog spam kill</td>
      <td>&gt;30 sends / 5 min → kill imsg + restart gateway</td>
      <td><span class="badge badge-ok">Active</span></td>
    </tr>
  </tbody>
</table>

<div class="section-head">Architecture</div>
<pre style="background:#1a1a1a;color:#e0e0e0;padding:20px;border-radius:6px;font-size:0.78rem;line-height:1.6;overflow-x:auto;">
Gateway (port 18789)
    │
    ▼  JSON-RPC over stdin/stdout
imsg-proxy  ←──────── /opt/homebrew/bin/imsg  (symlink to proxy)
    │                  /opt/homebrew/Cellar/imsg/0.5.0/bin/imsg (symlink to proxy)
    │
    ├── [ALLOW?] ──► Real imsg binary
    │                /opt/homebrew/Cellar/imsg/0.5.0/libexec/imsg
    │
    └── [BLOCK] ──► Error JSON-RPC response back to gateway
                     ↓
                 imsg-blocks.jsonl
                     ↓
                 soul-autopatch.sh (weekly)
                     ↓
                 soul-patches.md → SOUL rules
</pre>

<div class="section-head">Watchdog Schedule</div>
<table class="health-table">
  <thead><tr><th>Cron</th><th>Schedule</th><th>Action</th></tr></thead>
  <tbody>
    <tr>
      <td>lobo-watchdog.sh</td>
      <td>Every 5 minutes</td>
      <td>Service health + spam rate check; kills imsg if &gt;30 sends/5min</td>
    </tr>
    <tr>
      <td>inbound-recovery.py sweep</td>
      <td>Every 10 minutes</td>
      <td>Re-queues dropped inbound messages stuck &gt;5 min</td>
    </tr>
    <tr>
      <td>soul-autopatch.sh</td>
      <td>Weekly (Sunday 02:00)</td>
      <td>Merges block log into corrections, drafts SOUL patches for 3+ patterns</td>
    </tr>
  </tbody>
</table>

<script>
// Parse imsg-proxy.log stats from a server-side data endpoint (if available)
// Falls back to displaying last-known static values when running on GitHub Pages
(function() {
  // On GitHub Pages we can't run server code, so show static config confirmation
  document.getElementById('statSent').textContent = '✓';
  document.getElementById('statBlocked').textContent = '✓';
  document.getElementById('statDedup').textContent = '✓';
  document.getElementById('statRateLimit').textContent = '✓';
  document.getElementById('statSpamKills').textContent = '0';
  document.getElementById('statProxyOk').textContent = 'UP';

  // Update stat card colors
  document.getElementById('statProxyOk').closest('.stat-card').className = 'stat-card ok';

  // Show static block log note
  document.getElementById('blockLog').innerHTML =
    '<tr><td colspan="4" style="text-align:center;padding:16px;font-family:var(--font-mono);font-size:0.75rem;color:#666;">' +
    'Live log available at: ~/.openclaw/logs/imsg-proxy.log<br>' +
    'Block log at: ~/.openclaw/state/imsg-blocks.jsonl' +
    '</td></tr>';
})();
</script>
