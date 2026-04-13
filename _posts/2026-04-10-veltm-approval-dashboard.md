---
layout: post
title: "VELTM Campaign Approval Dashboard"
date: 2026-04-10 18:00:00 -0400
author: orchestrator
categories: veltm
tags: [veltm, approval, dashboard]
hero_image: "https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?w=1200"
excerpt: "Central approval tracker for all VELTM Butler Button campaign assets — built from Brand Guidelines + Campaign Playbook Apr 2026."
---

<style>
:root { --indigo: #4F46E5; --purple: #9333EA; --deep: #312E81; --near-black: #09090B; --lavender: #F5F3FF; --gray: #4B5563; }
.db-wrap { font-family: Arial, sans-serif; }
.db-header { background: linear-gradient(135deg, #4F46E5, #9333EA); color: #fff; border-radius: 10px; padding: 28px 32px; margin-bottom: 28px; }
.db-header h1 { font-family: Georgia, serif; font-size: 1.6rem; margin: 0 0 6px; color: #fff; }
.db-header p { margin: 0; font-size: 0.85rem; opacity: 0.8; }
.stat-row { display: grid; grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); gap: 14px; margin-bottom: 28px; }
.stat { background: var(--lavender); border-radius: 8px; padding: 16px 20px; border-left: 4px solid var(--indigo); }
.stat .n { font-size: 1.8rem; font-weight: 700; color: var(--indigo); font-family: Georgia, serif; line-height: 1; }
.stat .l { font-size: 0.7rem; text-transform: uppercase; letter-spacing: 0.12em; color: var(--gray); margin-top: 4px; }
.section-title { font-family: Georgia, serif; font-size: 1.15rem; font-weight: bold; color: var(--near-black); border-bottom: 2px solid var(--indigo); padding-bottom: 6px; margin: 28px 0 14px; }
table.at { width: 100%; border-collapse: collapse; font-size: 0.82rem; margin-bottom: 20px; }
table.at th { background: var(--near-black); color: #fff; padding: 8px 12px; text-align: left; font-size: 0.72rem; text-transform: uppercase; letter-spacing: 0.08em; }
table.at td { padding: 7px 12px; border-bottom: 1px solid #e5e7eb; vertical-align: top; }
table.at tr:nth-child(even) td { background: var(--lavender); }
.badge { display: inline-block; padding: 2px 8px; border-radius: 4px; font-size: 0.68rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.08em; }
.badge-ready   { background: #d1fae5; color: #065f46; }
.badge-pending { background: #fef3c7; color: #92400e; }
.badge-blocked { background: #fee2e2; color: #991b1b; }
.badge-review  { background: #e0e7ff; color: #3730a3; }
.campaign-block { border: 1px solid #e5e7eb; border-radius: 8px; margin-bottom: 20px; overflow: hidden; }
.campaign-header { background: linear-gradient(135deg, #4F46E5, #9333EA); color: #fff; padding: 12px 18px; display: flex; justify-content: space-between; align-items: center; }
.campaign-header h3 { margin: 0; font-family: Georgia, serif; font-size: 1rem; color: #fff; }
.campaign-header .obj { font-size: 0.75rem; opacity: 0.8; margin-top: 2px; }
.campaign-body { padding: 0; }
.note-box { background: #fef3c7; border-left: 4px solid #f59e0b; padding: 12px 16px; margin: 0 0 20px; border-radius: 0 6px 6px 0; font-size: 0.82rem; }
.note-box strong { color: #92400e; }
.cta-btn { display: inline-block; background: linear-gradient(135deg, #4F46E5, #9333EA); color: #fff; padding: 8px 18px; border-radius: 5px; font-size: 0.8rem; font-weight: bold; text-decoration: none; margin-top: 4px; }
</style>

<div class="db-wrap">

<div class="db-header">
  <h1>VELTM Campaign Approval Dashboard</h1>
  <p>Butler Button Awareness &amp; Lead Generation — April 2026 &nbsp;·&nbsp; Built from Brand Guidelines + Campaign Playbook</p>
</div>

<div class="stat-row">
  <div class="stat"><div class="n">5</div><div class="l">Email Templates</div></div>
  <div class="stat"><div class="n">9</div><div class="l">Social Posts</div></div>
  <div class="stat"><div class="n">5</div><div class="l">FB Group Posts</div></div>
  <div class="stat"><div class="n">6</div><div class="l">WhatsApp Msgs</div></div>
  <div class="stat"><div class="n">5</div><div class="l">Campaigns</div></div>
  <div class="stat"><div class="n">25</div><div class="l">Total Assets</div></div>
</div>

<div class="note-box">
  <strong>⚠️ Zoho Upload Blocked</strong> — Campaign creation API returns error 1004 (plan restriction). All 5 HTML email templates are built and ready. Two actions required before launch: (1) Enable API access in Zoho Campaigns Settings, (2) Disable double opt-in on "My Sample List" (Campaigns → Lists → Signup Settings). Assets are at <code>/tmp/veltm-campaign-assets/</code> on the Mac mini.
</div>

---

<div class="section-title">Campaign 1 — "Your Butler Awaits" &nbsp;<span class="badge badge-ready">Assets Ready</span></div>
<p style="font-size:0.85rem;color:var(--gray);">Objective: Introduce Butler Button to cold audiences. 3-email drip + 3 social posts. Week 1.</p>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Email Sequence (3 emails, 3 days apart)</h3><div class="obj">Welcome drip: triggered on new contact creation</div></div><span class="badge badge-ready">3 of 3 Built</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Email</th><th>Subject</th><th>Preview Text</th><th>File</th><th>Status</th></tr></thead>
<tbody>
<tr><td>E1 — Day 0</td><td>Meet your personal travel butler</td><td>Trip planning and on-trip help from $25/day</td><td>c1-email1-introduction.html</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>E2 — Day 3</td><td>How Butler Button works in 3 simple steps</td><td>Book. Connect. Text. That's it.</td><td>c1-email2-how-it-works.html</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>E3 — Day 6</td><td>1,000+ travelers already trust Butler Button</td><td>From forgotten chargers to last-minute reservations</td><td>c1-email3-social-proof.html</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
</tbody>
</table>
</div>
</div>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Social Posts</h3><div class="obj">Instagram, Facebook, LinkedIn</div></div><span class="badge badge-ready">3 of 3 Built</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Post ID</th><th>Platform</th><th>Format</th><th>Visual Direction</th><th>Status</th></tr></thead>
<tbody>
<tr><td>C1-IG-1</td><td>Instagram + Facebook</td><td>Single image</td><td>Indigo→Purple gradient bg, "Your Butler Awaits" in white Georgia</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>C1-IG-2</td><td>Instagram + Facebook</td><td>Carousel (3 slides)</td><td>Lavender bg, 3 icon panels: Book → Connect → Text</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>C1-LI-1</td><td>LinkedIn</td><td>Single image</td><td>VELTM Indigo bg, world map watermark, professional headline</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
</tbody>
</table>
</div>
</div>

---

<div class="section-title">Campaign 2 — "$25 Travel Days" &nbsp;<span class="badge badge-ready">Assets Ready</span></div>
<p style="font-size:0.85rem;color:var(--gray);">Objective: Lead with the $25/day price point. Facebook Groups + WhatsApp Groups + Social. Week 2.</p>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Facebook Group Posts (3)</h3><div class="obj">Manual posting by Harleen — peer-to-peer tone</div></div><span class="badge badge-ready">3 of 3 Built</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Post ID</th><th>Hook</th><th>Status</th></tr></thead>
<tbody>
<tr><td>FB-C2-1</td><td>"What $25/day actually gets you when traveling"</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>FB-C2-2</td><td>"The most underrated travel hack of 2026"</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>FB-C2-3</td><td>"Planning a trip? Here's a shortcut"</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
</tbody>
</table>
</div>
</div>

<div class="campaign-block">
<div class="campaign-header"><div><h3>WhatsApp Messages (3)</h3><div class="obj">Manual posting by Harleen — under 200 chars each</div></div><span class="badge badge-ready">3 of 3 Built</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Msg ID</th><th>Opening</th><th>Status</th></tr></thead>
<tbody>
<tr><td>WA-C2-1</td><td>"Hey travelers! Just discovered something I had to share..."</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>WA-C2-2</td><td>"Imagine you're in Bali and you want a sunset dinner spot..."</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>WA-C2-3</td><td>"Quick one for anyone with upcoming travel plans..."</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
</tbody>
</table>
</div>
</div>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Social Posts (2)</h3><div class="obj">Instagram + Facebook</div></div><span class="badge badge-ready">2 of 2 Built</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Post ID</th><th>Visual</th><th>Status</th></tr></thead>
<tbody>
<tr><td>C2-IG-1</td><td>Near-black bg, "$25" in 72pt Indigo Georgia, value breakdown</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>C2-IG-2</td><td>Bali scenario Reel/Story (5-frame sequence)</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
</tbody>
</table>
</div>
</div>

---

<div class="section-title">Campaign 3 — "Destination Spotlight: Thailand" &nbsp;<span class="badge badge-ready">Assets Ready</span></div>
<p style="font-size:0.85rem;color:var(--gray);">Objective: Provide travel value, warm audiences, introduce Butler naturally. All channels. Week 3.</p>

<div class="campaign-block">
<div class="campaign-header"><div><h3>All Channels</h3><div class="obj">Email + Social + Facebook Group + WhatsApp</div></div><span class="badge badge-ready">4 of 4 Built</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Asset</th><th>Subject / Hook</th><th>Status</th></tr></thead>
<tbody>
<tr><td>Email Newsletter</td><td>"Thailand: 5 insider tips your guidebook won't tell you" (c3-email1-thailand-spotlight.html)</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>C3-IG-1 (Carousel)</td><td>"Thailand insider tip: the best pad thai in Bangkok isn't on Khao San Road" — 5-slide editorial carousel</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>FB-C3-1</td><td>"Planning a trip to Thailand? Here's a thread of things I wish I'd known..."</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>WA-C3-1</td><td>"Thailand tip: skip Friday Night Market in Chiang Mai..."</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
</tbody>
</table>
</div>
</div>

---

<div class="section-title">Campaign 4 — "Stress-Free Stories" &nbsp;<span class="badge badge-ready">Assets Ready</span></div>
<p style="font-size:0.85rem;color:var(--gray);">Objective: Social proof. Real-world Butler moments. All channels. Week 4.</p>

<div class="campaign-block">
<div class="campaign-header"><div><h3>All Channels</h3><div class="obj">Email + 2 Social Posts + Facebook Group + WhatsApp</div></div><span class="badge badge-ready">5 of 5 Built</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Asset</th><th>Hook</th><th>Status</th></tr></thead>
<tbody>
<tr><td>Email</td><td>"The travel problem no one talks about" (c4-email1-stress-free-stories.html)</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>C4-IG-1</td><td>Split-screen: Without Butler / With Butler — problem→solution format</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>C4-IG-2</td><td>"Things Butler Button assistants handled this week" — checklist format</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>FB-C4-1</td><td>"Has this ever happened to you while traveling?"</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>WA-C4-1</td><td>"Quick travel story: someone texted their Butler at 11pm in Rome..."</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
</tbody>
</table>
</div>
</div>

---

<div class="section-title">Campaign 5 — "The 3-Step Challenge" &nbsp;<span class="badge badge-ready">Assets Ready</span></div>
<p style="font-size:0.85rem;color:var(--gray);">Objective: Engagement + virality. Runs all month in parallel across WhatsApp + Facebook Groups + Social.</p>

<div class="campaign-block">
<div class="campaign-header"><div><h3>All Group Channels</h3><div class="obj">FB Groups + WhatsApp + Instagram/Facebook</div></div><span class="badge badge-ready">3 of 3 Built</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Asset</th><th>Hook</th><th>Status</th></tr></thead>
<tbody>
<tr><td>C5-IG-1</td><td>"3 Steps. 2 Minutes. Unlimited Travel Help." — bold Indigo typographic post</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>FB-C5-1</td><td>"The 3-Step Travel Challenge: I challenge anyone here to plan a trip in under 2 minutes."</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
<tr><td>WA-C5-1</td><td>"Travel challenge: can you plan a trip in 2 minutes?"</td><td><span class="badge badge-review">Awaiting Harleen Review</span></td></tr>
</tbody>
</table>
</div>
</div>

---

<div class="section-title">Zoho Upload Status &nbsp;<span class="badge badge-blocked">Action Required</span></div>

<div class="note-box">
<strong>Campaign API: Error 1004 (plan restriction)</strong><br>
All 5 HTML email templates are production-ready and on the Mac mini at <code>/tmp/veltm-campaign-assets/emails/</code>. The Zoho Campaigns API is returning error 1004 on all write endpoints — this is a plan-level restriction, not an authentication issue. To unblock:<br><br>
<strong>Step 1:</strong> Zoho Campaigns → Settings → Integrations → API → Enable API Access<br>
<strong>Step 2:</strong> Zoho Campaigns → Lists → My Sample List → Signup Settings → Disable double opt-in<br>
<strong>Step 3:</strong> Once unblocked, Claude will upload all 5 campaigns automatically.<br><br>
Until then, Harleen can upload manually: Zoho Campaigns → Campaigns → Create Campaign → HTML Campaign → paste HTML file contents.
</div>

<div class="section-title">Posting Schedule</div>

<table class="at">
<thead><tr><th>Week</th><th>Campaign</th><th>Channel</th><th>Content</th><th>Best Day</th><th>Best Time EST</th></tr></thead>
<tbody>
<tr><td>1</td><td>Your Butler Awaits</td><td>Email (automated)</td><td>3-email drip on new contact signup</td><td>—</td><td>—</td></tr>
<tr><td>1</td><td>Your Butler Awaits</td><td>Instagram + Facebook</td><td>C1-IG-1 (intro) + C1-IG-2 (how it works)</td><td>Tue + Fri</td><td>9am + 12pm</td></tr>
<tr><td>1</td><td>Your Butler Awaits</td><td>LinkedIn</td><td>C1-LI-1 (professional angle)</td><td>Wed</td><td>8am</td></tr>
<tr><td>2</td><td>$25 Travel Days</td><td>Facebook Groups</td><td>FB-C2-1, FB-C2-2, FB-C2-3</td><td>Wed + Thu + Fri</td><td>1pm</td></tr>
<tr><td>2</td><td>$25 Travel Days</td><td>WhatsApp Groups</td><td>WA-C2-1, WA-C2-2, WA-C2-3</td><td>Tue + Thu + Sat</td><td>10am</td></tr>
<tr><td>2</td><td>$25 Travel Days</td><td>Instagram + Facebook</td><td>C2-IG-1 + C2-IG-2</td><td>Wed + Fri</td><td>12pm + 6pm</td></tr>
<tr><td>3</td><td>Destination: Thailand</td><td>All channels</td><td>Email + C3-IG-1 + FB-C3-1 + WA-C3-1</td><td>Wed + Thu</td><td>9am + 1pm</td></tr>
<tr><td>4</td><td>Stress-Free Stories</td><td>All channels</td><td>Email + C4-IG-1 + C4-IG-2 + FB-C4-1 + WA-C4-1</td><td>Tue–Thu</td><td>12pm + 3pm</td></tr>
<tr><td>1–4</td><td>3-Step Challenge</td><td>Groups + Social</td><td>C5-IG-1 + FB-C5-1 + WA-C5-1 (ongoing)</td><td>Fri</td><td>3pm</td></tr>
</tbody>
</table>

<div class="section-title">KPIs</div>

<table class="at">
<thead><tr><th>Metric</th><th>Target</th><th>Tool</th></tr></thead>
<tbody>
<tr><td>Email open rate</td><td>&gt; 25%</td><td>Zoho Campaigns analytics</td></tr>
<tr><td>Email click-through rate</td><td>&gt; 3%</td><td>Zoho Campaigns analytics</td></tr>
<tr><td>Social engagement rate</td><td>&gt; 4%</td><td>Zoho Social analytics</td></tr>
<tr><td>Leads per week</td><td>&gt; 10</td><td>Zoho CRM pipeline</td></tr>
<tr><td>Lead-to-booking conversion</td><td>&gt; 15%</td><td>Zoho CRM pipeline</td></tr>
<tr><td>Cost per acquisition</td><td>&lt; $20</td><td>Zoho CRM + manual</td></tr>
</tbody>
</table>

</div>
