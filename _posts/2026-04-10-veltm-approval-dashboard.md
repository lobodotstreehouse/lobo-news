---
layout: post
title: "VELTM Campaign Approval Dashboard"
date: 2026-04-10 18:00:00 -0400
author: orchestrator
categories: veltm
tags: [veltm, approval, dashboard]
hero_image: "https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?w=1200"
excerpt: "Full funnel: organic social authority → social selling → triggered personalized email sequence. Built from Brand Guidelines + Campaign Playbook Apr 2026."
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
.badge-new     { background: #dbeafe; color: #1e40af; }
.campaign-block { border: 1px solid #e5e7eb; border-radius: 8px; margin-bottom: 20px; overflow: hidden; }
.campaign-header { background: linear-gradient(135deg, #4F46E5, #9333EA); color: #fff; padding: 12px 18px; display: flex; justify-content: space-between; align-items: center; }
.campaign-header h3 { margin: 0; font-family: Georgia, serif; font-size: 1rem; color: #fff; }
.campaign-header .obj { font-size: 0.75rem; opacity: 0.8; margin-top: 2px; }
.campaign-body { padding: 0; }
.note-box { background: #fef3c7; border-left: 4px solid #f59e0b; padding: 12px 16px; margin: 0 0 20px; border-radius: 0 6px 6px 0; font-size: 0.82rem; }
.note-box strong { color: #92400e; }
.info-box { background: #f0fdf4; border-left: 4px solid #16a34a; padding: 12px 16px; margin: 0 0 20px; border-radius: 0 6px 6px 0; font-size: 0.82rem; }
.info-box strong { color: #166534; }
.funnel-row { display: grid; grid-template-columns: repeat(3, 1fr); gap: 0; margin-bottom: 28px; border: 1px solid #e5e7eb; border-radius: 10px; overflow: hidden; }
.funnel-step { padding: 20px; text-align: center; }
.funnel-step:not(:last-child) { border-right: 1px solid #e5e7eb; }
.funnel-step .step-num { font-family: Georgia, serif; font-size: 2rem; font-weight: bold; color: var(--indigo); line-height: 1; margin-bottom: 6px; }
.funnel-step .step-name { font-size: 0.8rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.1em; color: var(--near-black); margin-bottom: 6px; }
.funnel-step .step-desc { font-size: 0.78rem; color: var(--gray); line-height: 1.5; }
.cta-btn { display: inline-block; background: linear-gradient(135deg, #4F46E5, #9333EA); color: #fff; padding: 8px 18px; border-radius: 5px; font-size: 0.8rem; font-weight: bold; text-decoration: none; margin-top: 4px; }
code { background: #f3f4f6; padding: 1px 5px; border-radius: 3px; font-size: 0.85em; }
</style>

<div class="db-wrap">

<div class="db-header">
  <h1>VELTM Campaign Approval Dashboard</h1>
  <p>Butler Button — Full Funnel: Brand Authority → Social Selling → Personalized Triggered Email &nbsp;·&nbsp; April 2026</p>
</div>

<div class="stat-row">
  <div class="stat"><div class="n">4</div><div class="l">Triggered Emails</div></div>
  <div class="stat"><div class="n">9</div><div class="l">Brand Social Posts</div></div>
  <div class="stat"><div class="n">16</div><div class="l">Team Advocate Posts</div></div>
  <div class="stat"><div class="n">5</div><div class="l">FB Group Posts</div></div>
  <div class="stat"><div class="n">6</div><div class="l">WhatsApp Msgs</div></div>
  <div class="stat"><div class="n">1</div><div class="l">Social Selling Playbook</div></div>
</div>

<div class="section-title">The 3-Step Funnel</div>

<div class="funnel-row">
  <div class="funnel-step" style="background:#f5f3ff;">
    <div class="step-num">1</div>
    <div class="step-name">Brand Authority</div>
    <div class="step-desc">VELTM organic posts + weekly personal content from Carl, Ansh, Nils, Panveer + Harleen discovery content. Builds trust before anyone sees an email.</div>
  </div>
  <div class="funnel-step" style="background:#ede9fe;">
    <div class="step-num">2</div>
    <div class="step-name">Social Selling</div>
    <div class="step-desc">Harleen joins travel groups, replies to real questions with genuine value, bridges engaged followers to DM → CRM lead entry → list signup.</div>
  </div>
  <div class="funnel-step" style="background:#ddd6fe;">
    <div class="step-num">3</div>
    <div class="step-name">Triggered Email</div>
    <div class="step-desc">Sign-up form → CRM Lead created → Zoho Workflow fires → adds to Campaigns list → 4-email personalized autoresponder sequence begins immediately.</div>
  </div>
</div>

<div class="info-box">
  <strong>✅ Zoho CRM API: Confirmed Working</strong> — All read/write operations on Contacts, Leads, and Deals modules are available. CRM → Campaigns list sync via Workflow is the recommended automation path.<br><br>
  <strong>⚠️ Zoho Campaigns API: Plan Restriction</strong> — Campaign creation and subscriber management endpoints return error 1004. This is a plan-level restriction, not an authentication issue. Email templates are production-ready for manual upload. Full Zoho setup walkthrough: <code>/tmp/veltm-campaign-assets/ZOHO-SETUP-GUIDE.md</code><br><br>
  <strong>To unlock programmatic sends:</strong> Campaigns → Settings → Developer Space → confirm API is enabled for your plan tier. If not available, Standard plan upgrade required.
</div>

<a href="/lobo-news/veltm/2026/04/11/veltm-creative-review/" class="cta-btn">→ Open Harleen's Review Queue</a>

---

<div class="section-title">Step 1A — VELTM Brand Social Posts &nbsp;<span class="badge badge-review">Awaiting Harleen Review</span></div>
<p style="font-size:0.85rem;color:var(--gray);">VELTM-branded posts for the main account. Establish product credibility before social selling begins.</p>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Campaign 1 — "Your Butler Awaits"</h3><div class="obj">Instagram, Facebook, LinkedIn — Week 1</div></div><span class="badge badge-ready">3 Built</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Post ID</th><th>Platform</th><th>Format</th><th>Visual Direction</th><th>Status</th></tr></thead>
<tbody>
<tr><td>C1-IG-1</td><td>Instagram + Facebook</td><td>Single image</td><td>Indigo→Purple gradient, "Your Butler Awaits" Georgia white</td><td><span class="badge badge-review">Review</span></td></tr>
<tr><td>C1-IG-2</td><td>Instagram + Facebook</td><td>Carousel (3 slides)</td><td>Lavender bg, 3-panel: Book → Connect → Text</td><td><span class="badge badge-review">Review</span></td></tr>
<tr><td>C1-LI-1</td><td>LinkedIn</td><td>Single image</td><td>Indigo bg, world map watermark, professional headline</td><td><span class="badge badge-review">Review</span></td></tr>
</tbody>
</table>
</div>
</div>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Campaign 2 — "$25 Travel Days"</h3><div class="obj">Instagram, Facebook — Week 2</div></div><span class="badge badge-ready">2 Built</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Post ID</th><th>Visual</th><th>Status</th></tr></thead>
<tbody>
<tr><td>C2-IG-1</td><td>Near-black bg, "$25" in 72pt Indigo Georgia, value breakdown</td><td><span class="badge badge-review">Review</span></td></tr>
<tr><td>C2-IG-2</td><td>Bali scenario Reel/Story (5-frame sequence)</td><td><span class="badge badge-review">Review</span></td></tr>
</tbody>
</table>
</div>
</div>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Campaigns 3–5 — Destination / Stories / Challenge</h3><div class="obj">Weeks 3–4+</div></div><span class="badge badge-ready">4 Built</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Post ID</th><th>Campaign</th><th>Hook</th><th>Status</th></tr></thead>
<tbody>
<tr><td>C3-IG-1</td><td>Thailand Spotlight</td><td>5-slide editorial carousel — insider Thailand tips</td><td><span class="badge badge-review">Review</span></td></tr>
<tr><td>C4-IG-1</td><td>Stress-Free Stories</td><td>Split-screen: Without Butler / With Butler</td><td><span class="badge badge-review">Review</span></td></tr>
<tr><td>C4-IG-2</td><td>Stress-Free Stories</td><td>"Things Butler Button handled this week" — checklist</td><td><span class="badge badge-review">Review</span></td></tr>
<tr><td>C5-IG-1</td><td>3-Step Challenge</td><td>"3 Steps. 2 Minutes. Unlimited Travel Help." — typographic</td><td><span class="badge badge-review">Review</span></td></tr>
</tbody>
</table>
</div>
</div>

---

<div class="section-title">Step 1B — Team Advocate Posts (Carl, Ansh, Nils, Panveer) &nbsp;<span class="badge badge-new">New</span></div>
<p style="font-size:0.85rem;color:var(--gray);">Weekly personal posts — each person's individual LinkedIn + Instagram. Self-recorded video or thought leadership. Written as a person, not a brand. 4 weeks of posts per person = 16 posts total.</p>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Carl — CEO / Founder &nbsp;·&nbsp; 4 posts</h3><div class="obj">LinkedIn primary · 2 video, 2 written · Weekly</div></div><span class="badge badge-new">4 Posts Ready</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Week</th><th>Theme</th><th>Format</th></tr></thead>
<tbody>
<tr><td>Week 1</td><td>Why I started VELTM — the wasted afternoon in [city]</td><td>Self-recorded video, 60–90 sec</td></tr>
<tr><td>Week 2</td><td>What I learned from our first 100 customers</td><td>Written LinkedIn (400–600 words)</td></tr>
<tr><td>Week 3</td><td>The future of AI in travel — contrarian take</td><td>Written LinkedIn (300–400 words)</td></tr>
<tr><td>Week 4</td><td>Personal travel story — when plans broke down</td><td>Video or written story</td></tr>
</tbody>
</table>
</div>
</div>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Ansh — Operations &nbsp;·&nbsp; 4 posts</h3><div class="obj">LinkedIn primary · Behind-the-scenes angle · Weekly</div></div><span class="badge badge-new">4 Posts Ready</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Week</th><th>Theme</th><th>Format</th></tr></thead>
<tbody>
<tr><td>Week 1</td><td>How we vet Butler Button assistants — specific criteria</td><td>Written or short video</td></tr>
<tr><td>Week 2</td><td>Most unusual request we've fulfilled (anonymized)</td><td>Story post — specific and real</td></tr>
<tr><td>Week 3</td><td>What great travel actually requires — contrarian take</td><td>Written LinkedIn</td></tr>
<tr><td>Week 4</td><td>Quality across 195 countries — the ops challenge</td><td>Video or written</td></tr>
</tbody>
</table>
</div>
</div>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Nils — Tech / Product &nbsp;·&nbsp; 4 posts</h3><div class="obj">LinkedIn primary · Product + data angle · Weekly</div></div><span class="badge badge-new">4 Posts Ready</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Week</th><th>Theme</th><th>Format</th></tr></thead>
<tbody>
<tr><td>Week 1</td><td>The technology behind Butler Button — what was actually hard</td><td>Written LinkedIn (accessible)</td></tr>
<tr><td>Week 2</td><td>What travelers actually text about (data) — vs. what we assumed</td><td>Data/insight post with 3–5 observations</td></tr>
<tr><td>Week 3</td><td>The product decision we made differently — and why</td><td>Video or written — product philosophy</td></tr>
<tr><td>Week 4</td><td>Where AI fits in VELTM — and where it doesn't</td><td>Written LinkedIn — visionary</td></tr>
</tbody>
</table>
</div>
</div>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Panveer — Sales / Partnerships &nbsp;·&nbsp; 4 posts</h3><div class="obj">LinkedIn + Instagram · Traveler-first angle · Weekly</div></div><span class="badge badge-new">4 Posts Ready</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Week</th><th>Theme</th><th>Format</th></tr></thead>
<tbody>
<tr><td>Week 1</td><td>My favorite travel hack using Butler Button — one specific moment</td><td>Self-recorded video, 60–90 sec</td></tr>
<tr><td>Week 2</td><td>The travel communities I learn the most from</td><td>Carousel or written — genuine list</td></tr>
<tr><td>Week 3</td><td>Why travel assistance is the next big thing</td><td>Written thought leadership</td></tr>
<tr><td>Week 4</td><td>How to get the most out of $25/day — 5 specific things</td><td>Video or carousel — practical guide</td></tr>
</tbody>
</table>
</div>
</div>

<p style="font-size:0.82rem;color:var(--gray);">Full scripts, hooks, and video direction at <code>/tmp/veltm-campaign-assets/social/team-advocate-posts.md</code></p>

---

<div class="section-title">Step 2 — Harleen Social Selling &nbsp;<span class="badge badge-new">Playbook Ready</span></div>
<p style="font-size:0.85rem;color:var(--gray);">45–60 min/day. Join travel communities. Reply to real questions with genuine local knowledge. Mention Butler Button only when it's a natural fit. Bridge DMs to CRM lead entry → email sequence.</p>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Community Presence</h3><div class="obj">Facebook Groups + Reddit + LinkedIn Groups</div></div><span class="badge badge-new">Playbook Built</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Activity</th><th>Frequency</th><th>Platform</th></tr></thead>
<tbody>
<tr><td>Join 8–12 active travel groups (solo, destination-specific, nomad, luxury)</td><td>Week 1 setup</td><td>Facebook</td></tr>
<tr><td>Reply to 3–5 travel questions per day with genuine local knowledge</td><td>Daily</td><td>Facebook + Reddit</td></tr>
<tr><td>Post one original content piece per day (tip, question, story)</td><td>Daily</td><td>Facebook + Instagram</td></tr>
<tr><td>Convert DMs to CRM lead — capture destination, travel date, style</td><td>As received</td><td>All platforms</td></tr>
<tr><td>Bridge CRM lead to Campaigns list for automated email sequence</td><td>Same day as DM</td><td>Zoho CRM</td></tr>
</tbody>
</table>
</div>
</div>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Facebook Group Posts — Campaign 2 ($25 Travel Days)</h3><div class="obj">Peer-to-peer tone. Posted by Harleen manually in travel groups.</div></div><span class="badge badge-ready">3 Built</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Post ID</th><th>Hook</th><th>Status</th></tr></thead>
<tbody>
<tr><td>FB-C2-1</td><td>"What $25/day actually gets you when traveling"</td><td><span class="badge badge-review">Review</span></td></tr>
<tr><td>FB-C2-2</td><td>"The most underrated travel hack of 2026"</td><td><span class="badge badge-review">Review</span></td></tr>
<tr><td>FB-C2-3</td><td>"Planning a trip? Here's a shortcut"</td><td><span class="badge badge-review">Review</span></td></tr>
</tbody>
</table>
</div>
</div>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Facebook Group Posts — Campaigns 3–5</h3><div class="obj">Destination, stories, challenge posts</div></div><span class="badge badge-ready">3 Built</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Post ID</th><th>Hook</th><th>Status</th></tr></thead>
<tbody>
<tr><td>FB-C3-1</td><td>"Planning a trip to Thailand? Here's a thread of things I wish I'd known..."</td><td><span class="badge badge-review">Review</span></td></tr>
<tr><td>FB-C4-1</td><td>"Has this ever happened to you while traveling?"</td><td><span class="badge badge-review">Review</span></td></tr>
<tr><td>FB-C5-1</td><td>"The 3-Step Travel Challenge: plan a trip in under 2 minutes"</td><td><span class="badge badge-review">Review</span></td></tr>
</tbody>
</table>
</div>
</div>

<div class="campaign-block">
<div class="campaign-header"><div><h3>WhatsApp Group Messages</h3><div class="obj">All campaigns — under 200 chars, no hashtags</div></div><span class="badge badge-ready">6 Built</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Msg ID</th><th>Campaign</th><th>Opening</th><th>Status</th></tr></thead>
<tbody>
<tr><td>WA-C2-1</td><td>$25 Days</td><td>"Hey travelers! Just discovered something I had to share..."</td><td><span class="badge badge-review">Review</span></td></tr>
<tr><td>WA-C2-2</td><td>$25 Days</td><td>"Imagine you're in Bali and you want a sunset dinner spot..."</td><td><span class="badge badge-review">Review</span></td></tr>
<tr><td>WA-C2-3</td><td>$25 Days</td><td>"Quick one for anyone with upcoming travel plans..."</td><td><span class="badge badge-review">Review</span></td></tr>
<tr><td>WA-C3-1</td><td>Thailand</td><td>"Thailand tip: skip Friday Night Market in Chiang Mai..."</td><td><span class="badge badge-review">Review</span></td></tr>
<tr><td>WA-C4-1</td><td>Stories</td><td>"Quick travel story: someone texted their Butler at 11pm in Rome..."</td><td><span class="badge badge-review">Review</span></td></tr>
<tr><td>WA-C5-1</td><td>Challenge</td><td>"Travel challenge: can you plan a trip in 2 minutes?"</td><td><span class="badge badge-review">Review</span></td></tr>
</tbody>
</table>
</div>
</div>

<p style="font-size:0.82rem;color:var(--gray);">Full social selling playbook at <code>/tmp/veltm-campaign-assets/social/social-selling-playbook-harleen.md</code></p>

---

<div class="section-title">Step 3 — Triggered Personalized Email Sequence &nbsp;<span class="badge badge-new">Rebuilt with Zoho Merge Tags</span></div>
<p style="font-size:0.85rem;color:var(--gray);">4-email autoresponder. Fires on CRM lead creation → Campaigns list add. All templates use Zoho merge tags for personalization. Conditional blocks adapt copy based on contact's destination and travel style fields.</p>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Personalization Fields (set on Campaigns list)</h3><div class="obj">Must be configured before upload — see Zoho Setup Guide</div></div><span class="badge badge-pending">Manual Setup Required</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Field</th><th>Merge Tag</th><th>Where Populated</th></tr></thead>
<tbody>
<tr><td>First Name</td><td><code>${FIRSTNAME|Traveler}</code></td><td>Sign-up form → CRM → Campaigns sync</td></tr>
<tr><td>Destination</td><td><code>${DESTINATION|your destination}</code></td><td>Sign-up form optional field</td></tr>
<tr><td>Travel Date</td><td><code>${TRAVEL_DATE|your trip}</code></td><td>Sign-up form optional field</td></tr>
<tr><td>Travel Style</td><td><code>${TRAVEL_STYLE|your travel style}</code></td><td>Sign-up form dropdown → CRM field</td></tr>
<tr><td>Plan Type</td><td><code>${PLAN_TYPE|Butler Button}</code></td><td>Plan selected on sign-up</td></tr>
<tr><td>Source Channel</td><td><code>${SOURCE_CHANNEL}</code></td><td>UTM param → CRM Lead_Source</td></tr>
<tr><td>Signup Date</td><td><code>${SIGNUP_DATE}</code></td><td>CRM Created_Time → Campaigns sync</td></tr>
</tbody>
</table>
</div>
</div>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Email 1 — Welcome &nbsp;·&nbsp; Day 0 (Immediate)</h3><div class="obj">Trigger: Added to "Butler Button Onboarding" list · File: email-01-welcome.html</div></div><span class="badge badge-review">Review</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Element</th><th>Value</th></tr></thead>
<tbody>
<tr><td>Subject line A</td><td>Welcome to Butler Button, <code>${FIRSTNAME|Traveler}</code></td></tr>
<tr><td>Subject line B (test)</td><td>Your Butler is ready, <code>${FIRSTNAME|Traveler}</code></td></tr>
<tr><td>Personalization</td><td>First name + Destination callout block (conditional — shows if DESTINATION is populated)</td></tr>
<tr><td>Goal</td><td>Confirm account, set expectations, direct to dashboard</td></tr>
<tr><td>CTA</td><td>Go to Your Dashboard →</td></tr>
</tbody>
</table>
</div>
</div>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Email 2 — Getting Started &nbsp;·&nbsp; Day 1</h3><div class="obj">Trigger: 1 day after list add · File: email-02-getting-started.html</div></div><span class="badge badge-review">Review</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Element</th><th>Value</th></tr></thead>
<tbody>
<tr><td>Subject</td><td><code>${FIRSTNAME|Traveler}</code>, send your first text</td></tr>
<tr><td>Personalization</td><td>3 example first texts using <code>${DESTINATION}</code> and <code>${TRAVEL_STYLE}</code> — adapts to their trip context</td></tr>
<tr><td>Goal</td><td>Remove friction — show exactly what to say to start a conversation with Butler</td></tr>
<tr><td>CTA</td><td>Start Your Conversation →</td></tr>
</tbody>
</table>
</div>
</div>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Email 3 — Destination Intel &nbsp;·&nbsp; Day 3</h3><div class="obj">Trigger: 3 days after list add · Segment: DESTINATION is not blank · File: email-03-destination-intel.html</div></div><span class="badge badge-review">Review</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Element</th><th>Value</th></tr></thead>
<tbody>
<tr><td>Subject</td><td>Before you go to <code>${DESTINATION|your destination}</code></td></tr>
<tr><td>Personalization</td><td>Header and body adapt to destination: "Before you go to ${DESTINATION}" vs. "Before your next trip" (fallback)</td></tr>
<tr><td>Segment A</td><td>DESTINATION is not blank → destination-specific subject line + in-body references</td></tr>
<tr><td>Segment B</td><td>DESTINATION is blank → generic "your destination" copy (fallbacks built into template)</td></tr>
<tr><td>Goal</td><td>Deliver genuine value — establish that Butler = real local knowledge, not just logistics</td></tr>
<tr><td>CTA</td><td>Ask Your Butler Now →</td></tr>
</tbody>
</table>
</div>
</div>

<div class="campaign-block">
<div class="campaign-header"><div><h3>Email 4 — First Trip Invitation &nbsp;·&nbsp; Day 7</h3><div class="obj">Trigger: 7 days after list add, only if no link click in emails 1–3 · File: email-04-first-trip-invitation.html</div></div><span class="badge badge-review">Review</span></div>
<div class="campaign-body">
<table class="at">
<thead><tr><th>Element</th><th>Value</th></tr></thead>
<tbody>
<tr><td>Subject A</td><td><code>${FIRSTNAME|Traveler}</code>, your Butler hasn't heard from you yet</td></tr>
<tr><td>Subject B (test)</td><td>You signed up 7 days ago — here's what you've missed</td></tr>
<tr><td>Personalization</td><td>Signup date reference (<code>${SIGNUP_DATE}</code>), destination-specific CTA option C (conditional)</td></tr>
<tr><td>Content</td><td>Without Butler vs. With Butler comparison, 3 specific first-step options</td></tr>
<tr><td>Goal</td><td>Convert — get first active Butler session booked</td></tr>
<tr><td>CTA</td><td>Start Planning Your Trip →</td></tr>
</tbody>
</table>
</div>
</div>

---

<div class="section-title">Zoho Setup Checklist &nbsp;<span class="badge badge-pending">Action Required</span></div>

<div class="note-box">
<strong>Who does this:</strong> Ansh (Zoho admin access confirmed — ansh@veltmtours.com)<br><br>
☐ <strong>Step 1:</strong> Create list "Butler Button Onboarding" in Zoho Campaigns<br>
☐ <strong>Step 2:</strong> Add 7 custom contact fields (DESTINATION, TRAVEL_DATE, PLAN_TYPE, TRAVEL_STYLE, SOURCE_CHANNEL, SIGNUP_DATE — see setup guide)<br>
☐ <strong>Step 3:</strong> Upload 4 HTML email templates (email-01 through email-04)<br>
☐ <strong>Step 4:</strong> Create Autoresponder series — 4 emails, Day 0 / Day 1 / Day 3 / Day 7<br>
☐ <strong>Step 5:</strong> Create CRM Workflow: Lead Created → Add to Campaigns list with field mapping<br>
☐ <strong>Step 6:</strong> Update sign-up form to capture Destination, Travel Date, Plan Type, Travel Style<br>
☐ <strong>Step 7:</strong> Set UTM parameters on all social links → veltmtours.com<br>
☐ <strong>Step 8:</strong> Disable double opt-in on Butler Button Onboarding list<br><br>
Full step-by-step guide: <code>/tmp/veltm-campaign-assets/ZOHO-SETUP-GUIDE.md</code>
</div>

<div class="section-title">KPIs</div>

<table class="at">
<thead><tr><th>Metric</th><th>Target</th><th>Source</th></tr></thead>
<tbody>
<tr><td>Email 1 open rate</td><td>&gt; 45%</td><td>Zoho Campaigns analytics</td></tr>
<tr><td>Email 2–4 open rate</td><td>&gt; 25%</td><td>Zoho Campaigns analytics</td></tr>
<tr><td>Email click-through rate</td><td>&gt; 5%</td><td>Zoho Campaigns analytics</td></tr>
<tr><td>Social → sign-up (organic)</td><td>Track via UTM</td><td>CRM Lead_Source field</td></tr>
<tr><td>Social selling → DM → CRM lead</td><td>&gt; 5/week (Harleen)</td><td>CRM manual entry</td></tr>
<tr><td>Sign-up → first Butler conversation</td><td>&gt; 40% within 7 days</td><td>CRM Last_Activity_Time</td></tr>
<tr><td>Team advocate posts (total reach)</td><td>Track impressions/week</td><td>LinkedIn + Instagram analytics</td></tr>
</tbody>
</table>

</div>
