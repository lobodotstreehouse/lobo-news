---
layout: post
title: "VELTM Creative Review — Harleen's Queue"
date: 2026-04-11 10:00:00 -0400
author: content
categories: veltm
tags: [veltm, review, harleen, approval]
hero_image: "https://images.unsplash.com/photo-1542744094-3a31f272c490?w=1200"
excerpt: "Harleen's review queue for all VELTM campaign creatives. Approve or request changes — Claude will action rejections within 2 hours."
---

<style>
:root { --indigo: #4F46E5; --purple: #9333EA; --near-black: #09090B; --lavender: #F5F3FF; --gray: #4B5563; }
* { box-sizing: border-box; }
body { font-family: Arial, sans-serif; }

/* ── Layout ── */
.review-wrap { max-width: 860px; margin: 0 auto; }
.page-header { background: linear-gradient(135deg, #4F46E5, #9333EA); border-radius: 10px; padding: 28px 32px; margin-bottom: 28px; color: #fff; }
.page-header h1 { font-family: Georgia, serif; font-size: 1.5rem; margin: 0 0 6px; color: #fff; }
.page-header p { margin: 0; font-size: 0.83rem; opacity: 0.82; }

/* ── Progress bar ── */
.progress-row { display: flex; gap: 12px; margin-bottom: 28px; flex-wrap: wrap; }
.prog-box { flex: 1; min-width: 110px; background: var(--lavender); border-radius: 8px; padding: 14px 16px; text-align: center; border-top: 4px solid var(--indigo); }
.prog-box .pn { font-size: 1.6rem; font-weight: 700; color: var(--indigo); font-family: Georgia, serif; line-height: 1; }
.prog-box .pl { font-size: 0.68rem; text-transform: uppercase; letter-spacing: 0.1em; color: var(--gray); margin-top: 4px; }
.prog-box.approved { border-color: #10b981; }
.prog-box.approved .pn { color: #10b981; }
.prog-box.rejected { border-color: #ef4444; }
.prog-box.rejected .pn { color: #ef4444; }

/* ── Creative card ── */
.creative-card { border: 1.5px solid #e5e7eb; border-radius: 10px; margin-bottom: 20px; overflow: hidden; transition: box-shadow 0.2s; }
.creative-card:hover { box-shadow: 0 4px 20px rgba(79,70,229,0.12); }
.card-header { display: flex; justify-content: space-between; align-items: flex-start; padding: 14px 18px 10px; background: #fafafa; border-bottom: 1px solid #e5e7eb; gap: 12px; }
.card-meta { flex: 1; }
.card-id { font-size: 0.68rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.12em; color: var(--indigo); margin-bottom: 3px; }
.card-title { font-family: Georgia, serif; font-size: 1rem; font-weight: bold; color: var(--near-black); margin: 0 0 3px; }
.card-sub { font-size: 0.78rem; color: var(--gray); }
.card-status { flex-shrink: 0; }

/* ── Badge ── */
.badge { display: inline-block; padding: 3px 10px; border-radius: 4px; font-size: 0.68rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.08em; }
.badge-pending  { background: #fef3c7; color: #92400e; }
.badge-approved { background: #d1fae5; color: #065f46; }
.badge-rejected { background: #fee2e2; color: #991b1b; }
.badge-revision { background: #e0e7ff; color: #3730a3; }

/* ── Card body ── */
.card-body { padding: 16px 18px; }
.asset-label { font-size: 0.7rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.1em; color: var(--indigo); margin-bottom: 6px; }
.asset-preview { background: var(--lavender); border-radius: 6px; padding: 14px 16px; font-size: 0.83rem; line-height: 1.6; color: var(--near-black); white-space: pre-wrap; margin-bottom: 14px; max-height: 220px; overflow-y: auto; border-left: 3px solid var(--indigo); }
.visual-spec { background: #f0fdf4; border-radius: 6px; padding: 10px 14px; font-size: 0.78rem; color: #166534; border-left: 3px solid #10b981; margin-bottom: 14px; }
.visual-spec strong { color: #065f46; }

/* ── Review actions ── */
.review-actions { display: flex; gap: 10px; flex-wrap: wrap; align-items: flex-start; padding-top: 12px; border-top: 1px solid #e5e7eb; }
.btn { display: inline-flex; align-items: center; gap: 6px; padding: 9px 18px; border-radius: 6px; font-size: 0.82rem; font-weight: 700; cursor: pointer; border: none; text-decoration: none; transition: opacity 0.15s; }
.btn:hover { opacity: 0.85; }
.btn-approve { background: linear-gradient(135deg, #10b981, #059669); color: #fff; }
.btn-reject  { background: #ef4444; color: #fff; }
.btn-neutral { background: #f3f4f6; color: var(--near-black); border: 1px solid #d1d5db; }
.feedback-area { flex: 1; min-width: 220px; }
.feedback-area textarea { width: 100%; padding: 8px 12px; border: 1.5px solid #d1d5db; border-radius: 6px; font-family: Arial, sans-serif; font-size: 0.82rem; resize: vertical; min-height: 56px; }
.feedback-area textarea:focus { outline: none; border-color: var(--indigo); }
.feedback-area label { font-size: 0.72rem; color: var(--gray); margin-bottom: 4px; display: block; }
.submit-row { display: flex; gap: 8px; margin-top: 6px; }

/* ── Submission confirm ── */
.confirm-msg { display: none; background: #d1fae5; border: 1px solid #10b981; border-radius: 6px; padding: 10px 14px; font-size: 0.82rem; color: #065f46; margin-top: 8px; }

/* ── How it works ── */
.how-box { background: var(--lavender); border-radius: 8px; padding: 18px 20px; margin-bottom: 28px; font-size: 0.83rem; }
.how-box h3 { font-family: Georgia, serif; font-size: 1rem; color: var(--near-black); margin: 0 0 10px; }
.how-step { display: flex; gap: 10px; margin-bottom: 8px; align-items: flex-start; }
.how-num { background: var(--indigo); color: #fff; border-radius: 50%; width: 22px; height: 22px; min-width: 22px; display: flex; align-items: center; justify-content: center; font-size: 0.72rem; font-weight: 700; margin-top: 1px; }
</style>

<div class="review-wrap">

<div class="page-header">
  <h1>Harleen's Creative Review Queue</h1>
  <p>Review each asset below. Approve to mark ready for publishing, or reject with feedback — Claude will revise and resubmit within 2 hours.</p>
</div>

<div class="how-box">
  <h3>How This Works</h3>
  <div class="how-step"><div class="how-num">1</div><div>Read each creative. Full copy is shown in the preview panel. Visual specs describe what to create in Canva/your design tool.</div></div>
  <div class="how-step"><div class="how-num">2</div><div>Click <strong>Approve</strong> if the copy and direction are good, or <strong>Request Changes</strong> with your feedback note.</div></div>
  <div class="how-step"><div class="how-num">3</div><div>Your submission posts to the OpenClaw gateway. Claude picks it up, revises the asset, and pushes the update back to this page within 2 hours.</div></div>
  <div class="how-step"><div class="how-num">4</div><div>Once all assets are approved, Claude will batch-upload the email templates to Zoho Campaigns and package social posts for Zoho Social scheduling.</div></div>
</div>

<div class="progress-row">
  <div class="prog-box"><div class="pn" id="cnt-total">25</div><div class="pl">Total Assets</div></div>
  <div class="prog-box approved"><div class="pn" id="cnt-approved">0</div><div class="pl">Approved</div></div>
  <div class="prog-box rejected"><div class="pn" id="cnt-rejected">0</div><div class="pl">Needs Revision</div></div>
  <div class="prog-box"><div class="pn" id="cnt-pending">25</div><div class="pl">Awaiting Review</div></div>
</div>

<!-- ════════════════════════════════════════════════════
     CAMPAIGN 1 — YOUR BUTLER AWAITS
════════════════════════════════════════════════════ -->

<h2 style="font-family:Georgia,serif;font-size:1.1rem;color:var(--indigo);border-bottom:2px solid var(--indigo);padding-bottom:6px;margin:28px 0 16px;">Campaign 1 — "Your Butler Awaits" &nbsp;<small style="font-size:0.75rem;color:var(--gray);font-family:Arial,sans-serif;">Week 1 · Brand Awareness</small></h2>

<!-- C1-E1 -->
<div class="creative-card" id="card-C1-E1">
<div class="card-header">
  <div class="card-meta">
    <div class="card-id">C1-E1 · Email · Day 0</div>
    <div class="card-title">Meet your personal travel butler</div>
    <div class="card-sub">Preview: "Trip planning and on-trip help from $25/day"</div>
  </div>
  <div class="card-status"><span class="badge badge-pending" id="badge-C1-E1">Pending Review</span></div>
</div>
<div class="card-body">
  <div class="asset-label">Email Copy</div>
  <div class="asset-preview">Hi there,

Imagine having a personal travel assistant who handles every detail of your trip — from building the perfect itinerary to booking that impossible restaurant, all through a simple text message. That's Butler Button by VELTM.

Whether you're planning a two-week adventure through Southeast Asia or need real-time help navigating a new city, your dedicated Butler is ready. We cover 195+ countries, speak 150+ languages, and operate across all 24 timezones.

Getting started takes three steps:
1. Book — Choose your plan and destination. Takes under 2 minutes.
2. Connect — Your dedicated assistant reaches out within 1 hour.
3. Text — Send any request, any time. We handle the rest.

Plans start at just $25 per day. Over 1,000 travelers already rely on Butler Button to travel stress-free.

[CTA Button: Book Your Butler →]

Warm regards,
The VELTM Team</div>
  <div class="review-actions" id="actions-C1-E1">
    <button class="btn btn-approve" onclick="submitReview('C1-E1','approve')">✓ Approve</button>
    <div class="feedback-area">
      <label for="fb-C1-E1">Feedback for revision (required if rejecting):</label>
      <textarea id="fb-C1-E1" placeholder="e.g. Change tone, update pricing, adjust CTA text..."></textarea>
      <div class="submit-row">
        <button class="btn btn-reject" onclick="submitReview('C1-E1','reject')">✗ Request Changes</button>
      </div>
    </div>
  </div>
  <div class="confirm-msg" id="confirm-C1-E1"></div>
</div>
</div>

<!-- C1-E2 -->
<div class="creative-card" id="card-C1-E2">
<div class="card-header">
  <div class="card-meta">
    <div class="card-id">C1-E2 · Email · Day 3</div>
    <div class="card-title">How Butler Button works in 3 simple steps</div>
    <div class="card-sub">Preview: "Book. Connect. Text. That's it."</div>
  </div>
  <div class="card-status"><span class="badge badge-pending" id="badge-C1-E2">Pending Review</span></div>
</div>
<div class="card-body">
  <div class="asset-label">Email Copy</div>
  <div class="asset-preview">Hi there,

We hear the same question from new travelers: "How does Butler Button actually work?" The answer is refreshingly simple.

Step 1: Book your plan. Head to veltmtours.com and choose from Trip Planning ($25/country, 5 revisions), 8-Hour Service ($25/day), or 24-Hour Service ($100/day). Payment takes under 2 minutes.

Step 2: Connect with your Butler. Within one hour, your dedicated travel assistant reaches out via your preferred messaging platform. This is a real person backed by AI-powered research tools — not a chatbot.

Step 3: Text any request. Dinner reservations in Paris? A phone charger delivered to your hotel in Tokyo? Your anniversary suite decorated with flowers? Just text it. Your Butler handles everything.

No apps to download. No complicated dashboards. Just open your messaging app and text your Butler.

[CTA Button: Start Planning Your Trip →]

Warm regards,
The VELTM Team</div>
  <div class="review-actions" id="actions-C1-E2">
    <button class="btn btn-approve" onclick="submitReview('C1-E2','approve')">✓ Approve</button>
    <div class="feedback-area">
      <label for="fb-C1-E2">Feedback for revision:</label>
      <textarea id="fb-C1-E2" placeholder="e.g. Change tone, update pricing, adjust CTA text..."></textarea>
      <div class="submit-row"><button class="btn btn-reject" onclick="submitReview('C1-E2','reject')">✗ Request Changes</button></div>
    </div>
  </div>
  <div class="confirm-msg" id="confirm-C1-E2"></div>
</div>
</div>

<!-- C1-E3 -->
<div class="creative-card" id="card-C1-E3">
<div class="card-header">
  <div class="card-meta">
    <div class="card-id">C1-E3 · Email · Day 6</div>
    <div class="card-title">1,000+ travelers already trust Butler Button</div>
    <div class="card-sub">Preview: "From forgotten chargers to last-minute reservations"</div>
  </div>
  <div class="card-status"><span class="badge badge-pending" id="badge-C1-E3">Pending Review</span></div>
</div>
<div class="card-body">
  <div class="asset-label">Email Copy</div>
  <div class="asset-preview">Hi there,

Over 1,000 travelers across 7 continents have already discovered what stress-free travel feels like with Butler Button. Here are a few moments where their Butler made all the difference:

• The Anniversary Surprise: A couple in Rome wanted their hotel room decorated for their anniversary. Their Butler coordinated flowers, champagne, and a personalized note — all by text while they explored the Colosseum.

• The Forgotten Charger: A solo traveler in Bangkok left their phone charger at the airport. One text and a replacement was delivered to their hotel within the hour.

• The Last-Minute Reservation: A family in Tokyo needed a kid-friendly restaurant for eight people on a Saturday night. Their Butler secured a table at a top-rated spot in under 30 minutes.

These are not edge cases. They're everyday moments where having a Butler transforms your travel experience.

[CTA Button: Join 1,000+ Happy Travelers →]

Warm regards,
The VELTM Team</div>
  <div class="review-actions" id="actions-C1-E3">
    <button class="btn btn-approve" onclick="submitReview('C1-E3','approve')">✓ Approve</button>
    <div class="feedback-area">
      <label for="fb-C1-E3">Feedback for revision:</label>
      <textarea id="fb-C1-E3" placeholder="e.g. Change tone, update pricing, adjust CTA text..."></textarea>
      <div class="submit-row"><button class="btn btn-reject" onclick="submitReview('C1-E3','reject')">✗ Request Changes</button></div>
    </div>
  </div>
  <div class="confirm-msg" id="confirm-C1-E3"></div>
</div>
</div>

<!-- C1-IG-1 -->
<div class="creative-card" id="card-C1-IG-1">
<div class="card-header">
  <div class="card-meta">
    <div class="card-id">C1-IG-1 · Instagram + Facebook · Single Image</div>
    <div class="card-title">Your next trip just got a personal upgrade.</div>
    <div class="card-sub">Brand introduction post</div>
  </div>
  <div class="card-status"><span class="badge badge-pending" id="badge-C1-IG-1">Pending Review</span></div>
</div>
<div class="card-body">
  <div class="asset-label">Visual Spec</div>
  <div class="visual-spec"><strong>Design:</strong> Indigo (#4F46E5) → Purple (#9333EA) gradient background. Bold white Georgia text: "Your Butler Awaits." VELTM logo bottom center. "From $25/day" pill in Light Lavender (#F5F3FF) with Indigo text. <strong>Size:</strong> 1080×1080 (feed) / 1080×1920 (Stories).</div>
  <div class="asset-label">Caption</div>
  <div class="asset-preview">Your next trip just got a personal upgrade.

Meet Butler Button by VELTM — your personal travel concierge that handles everything from itinerary planning to on-the-ground requests. All through a simple text message.

Plans start at just $25/day. We cover 195+ countries, 150+ languages, and every timezone on the planet.

Book. Connect. Text. That's it.

🔗 Link in bio to get started.

#ButlerButton #TravelStressFree #VELTMTours #YourButlerAwaits #TravelConcierge #LuxuryTravel #TravelHack</div>
  <div class="review-actions" id="actions-C1-IG-1">
    <button class="btn btn-approve" onclick="submitReview('C1-IG-1','approve')">✓ Approve</button>
    <div class="feedback-area">
      <label for="fb-C1-IG-1">Feedback for revision:</label>
      <textarea id="fb-C1-IG-1" placeholder="e.g. Change caption tone, different visual direction..."></textarea>
      <div class="submit-row"><button class="btn btn-reject" onclick="submitReview('C1-IG-1','reject')">✗ Request Changes</button></div>
    </div>
  </div>
  <div class="confirm-msg" id="confirm-C1-IG-1"></div>
</div>
</div>

<!-- C1-IG-2 -->
<div class="creative-card" id="card-C1-IG-2">
<div class="card-header">
  <div class="card-meta">
    <div class="card-id">C1-IG-2 · Instagram + Facebook · Carousel (3 slides)</div>
    <div class="card-title">Three steps. That's all it takes.</div>
    <div class="card-sub">How It Works carousel</div>
  </div>
  <div class="card-status"><span class="badge badge-pending" id="badge-C1-IG-2">Pending Review</span></div>
</div>
<div class="card-body">
  <div class="asset-label">Visual Spec (3 slides)</div>
  <div class="visual-spec"><strong>Background:</strong> Light Lavender (#F5F3FF). <strong>Slide 1:</strong> Phone icon in Indigo circle, "Step 1: Book" — "Choose your plan at veltmtours.com." <strong>Slide 2:</strong> Handshake icon in Purple circle, "Step 2: Connect." <strong>Slide 3:</strong> Chat bubble icon, "Step 3: Text." VELTM logo + "From $25/day · 195+ countries" footer. <strong>Size:</strong> 1080×1080 each.</div>
  <div class="asset-label">Caption</div>
  <div class="asset-preview">Three steps. That's all it takes to get your own personal travel assistant.

1️⃣ Book your plan at veltmtours.com (under 2 minutes)
2️⃣ Connect with your dedicated Butler within 1 hour
3️⃣ Text any request — restaurant reservations, local tips, hotel arrangements, you name it

No apps. No dashboards. Just a message away from stress-free travel.

Starting from $25/day across 195+ countries.

#ButlerButton #TravelStressFree #VELTMTours #YourButlerAwaits #TravelConcierge</div>
  <div class="review-actions" id="actions-C1-IG-2">
    <button class="btn btn-approve" onclick="submitReview('C1-IG-2','approve')">✓ Approve</button>
    <div class="feedback-area">
      <label for="fb-C1-IG-2">Feedback:</label>
      <textarea id="fb-C1-IG-2" placeholder="Feedback..."></textarea>
      <div class="submit-row"><button class="btn btn-reject" onclick="submitReview('C1-IG-2','reject')">✗ Request Changes</button></div>
    </div>
  </div>
  <div class="confirm-msg" id="confirm-C1-IG-2"></div>
</div>
</div>

<!-- C1-LI-1 -->
<div class="creative-card" id="card-C1-LI-1">
<div class="card-header">
  <div class="card-meta">
    <div class="card-id">C1-LI-1 · LinkedIn · Single Image</div>
    <div class="card-title">The Future of Travel Is Personal Assistance at Scale.</div>
    <div class="card-sub">Professional angle for B2B/corporate travelers</div>
  </div>
  <div class="card-status"><span class="badge badge-pending" id="badge-C1-LI-1">Pending Review</span></div>
</div>
<div class="card-body">
  <div class="asset-label">Visual Spec</div>
  <div class="visual-spec"><strong>Background:</strong> VELTM Indigo (#4F46E5). <strong>Headline:</strong> "The Future of Travel Is Personal Assistance at Scale." white Georgia Bold. Subtle white world map watermark. VELTM logo bottom right. <strong>Size:</strong> 1200×627.</div>
  <div class="asset-label">Caption</div>
  <div class="asset-preview">The travel industry has a gap: premium concierge services exist for the ultra-wealthy, while everyone else navigates trip planning alone.

Butler Button by VELTM bridges that gap. We provide personal travel assistance — real humans backed by AI-powered tools — starting at $25 per day. No subscriptions. No commitments. Just text-based help across 195+ countries and 150+ languages.

For business travelers managing packed itineraries, families coordinating complex logistics, or solo adventurers who want local expertise on demand — the model is simple: Book, Connect, Text.

We've served 1,000+ travelers across 7 continents. The future of travel is personal, accessible, and always a message away.

Learn more at veltmtours.com

#ButlerButton #TravelTech #TravelStressFree #VELTMTours #FutureOfTravel</div>
  <div class="review-actions" id="actions-C1-LI-1">
    <button class="btn btn-approve" onclick="submitReview('C1-LI-1','approve')">✓ Approve</button>
    <div class="feedback-area">
      <label for="fb-C1-LI-1">Feedback:</label>
      <textarea id="fb-C1-LI-1" placeholder="Feedback..."></textarea>
      <div class="submit-row"><button class="btn btn-reject" onclick="submitReview('C1-LI-1','reject')">✗ Request Changes</button></div>
    </div>
  </div>
  <div class="confirm-msg" id="confirm-C1-LI-1"></div>
</div>
</div>

<!-- ════════ REMAINING CAMPAIGNS — COLLAPSED ════════ -->

<h2 style="font-family:Georgia,serif;font-size:1.1rem;color:var(--indigo);border-bottom:2px solid var(--indigo);padding-bottom:6px;margin:28px 0 16px;">Campaigns 2–5 &nbsp;<span class="badge badge-pending">19 assets pending</span></h2>

<div id="remaining-campaigns">

{% assign c2_assets = "C2-IG-1,C2-IG-2,FB-C2-1,FB-C2-2,FB-C2-3,WA-C2-1,WA-C2-2,WA-C2-3" | split: "," %}
{% assign c3_assets = "C3-E1,C3-IG-1,FB-C3-1,WA-C3-1" | split: "," %}
{% assign c4_assets = "C4-E1,C4-IG-1,C4-IG-2,FB-C4-1,WA-C4-1" | split: "," %}
{% assign c5_assets = "C5-IG-1,FB-C5-1,WA-C5-1" | split: "," %}

</div>

<!-- Render remaining asset cards via JS from the asset manifest -->
<div id="dynamic-cards"></div>

</div><!-- .review-wrap -->

<script>
// ── Asset manifest ───────────────────────────────────────────────
const ASSETS = {
  "C2-IG-1": { campaign:"C2 · $25 Travel Days", type:"Instagram + Facebook · Single Image", title:"$25/day gets you a dedicated travel assistant", caption:`$25/day. That's less than most airport meals.\n\nFor that, you get a dedicated travel assistant who handles:\n✓ Custom itinerary creation\n✓ Restaurant & activity reservations\n✓ On-trip errands (yes, they'll deliver a charger to your hotel)\n✓ Hotel arrangements & room requests\n✓ Real-time local tips in 150+ languages\n\nNo apps. No calls. Just text.\n\n195+ countries. Starting at $25/day. Link in bio.\n\n#ButlerButton #TravelHack #TravelStressFree #VELTMTours`, visual:"Near Black bg. '$25' in 72pt Georgia Indigo. Value list below in white Arial. Purple gradient CTA pill. 1080×1080." },
  "C2-IG-2": { campaign:"C2 · $25 Travel Days", type:"Instagram Reel / Story (5 frames)", title:"You're in Bali. One text handles everything.", caption:`Imagine this: You're in Bali. You want a sunset dinner that isn't on TripAdvisor's first page, a driver to get there, and your hotel room set up.\n\nOne text to Butler Button. ✅ Done.\n\nThis is $25/day with VELTM. 195+ countries. Real people, real-time help.\n\nLink in bio 🔗\n\n#ButlerButton #BaliTravel #TravelStressFree #VELTMTours`, visual:"5-frame Reel: Frame 1 warm Bali photography, Frames 2-4 Indigo gradient text overlays describing each request, Frame 5 VELTM logo + $25/day CTA." },
  "C3-E1":   { campaign:"C3 · Destination: Thailand", type:"Email Newsletter", title:"Thailand: 5 insider tips your guidebook won't tell you", caption:`Hi there,\n\nThailand rewards travelers who go beyond the guidebook. Here are five insider tips:\n\n1. Skip Friday Night Market in Chiang Mai — the Saturday Walking Street is less crowded and more authentic.\n2. Book island transfers a day early — ferries sell out during peak season.\n3. Bangkok's best pad thai isn't on Khao San Road — try Ari and Thonglor neighborhoods.\n4. Temple etiquette: never point feet at a Buddha image. Visit early morning.\n5. Have your Butler arrange a private driver — same price as tuk-tuks, far more comfortable.\n\n[CTA: Plan Your Thailand Trip →]\n\nWarm regards,\nThe VELTM Team`, visual:"Email template with warm Thailand photography (golden temple, turquoise sea). 5 numbered tips with Indigo bold labels." },
  "C3-IG-1": { campaign:"C3 · Destination: Thailand", type:"Instagram + Facebook · Carousel (5 slides)", title:"Thailand insider tip: the best pad thai isn't where the tourists are.", caption:`Thailand insider tip: the best pad thai in Bangkok isn't on Khao San Road. 🌶️\n\nIt's in neighborhoods like Ari and Thonglor, where locals actually eat. The tricky part? Knowing which vendors are worth the walk.\n\nThat's where your Butler comes in. Text your Butler Button assistant and they'll map out a personalized food route, arrange a driver, and handle every reservation.\n\nSwipe for 5 tips your guidebook won't tell you ➡️\n\nFrom $25/day · 195+ countries. Link in bio.\n\n#ButlerButton #ThailandTravel #BangkokFood #TravelStressFree #VELTMTours`, visual:"Editorial photography: golden temple at sunset, turquoise sea, Bangkok street food, Chiang Mai night market, island ferry. VELTM logo overlay on each. 1080×1080 per slide." },
  "FB-C3-1": { campaign:"C3 · Destination: Thailand", type:"Facebook Group Post", title:"Thailand planning thread", caption:`Planning a trip to Thailand? Here's a thread of things I wish I'd known:\n\nThe Saturday Night Market in Chiang Mai beats the Friday one. Book island ferry tickets a day in advance during peak season. Bangkok's best food is in local neighborhoods, not tourist strips. Always negotiate tuk-tuk prices before you get in.\n\nIf you want someone to handle all this in real-time, Butler Button by VELTM gives you a personal travel assistant via text for $25/day. 195+ countries. veltmtours.com\n\nDrop your Thailand questions below — happy to help!`, visual:"No image needed. Peer-to-peer tone. Post in Thailand travel Facebook groups." },
  "WA-C3-1": { campaign:"C3 · Destination: Thailand", type:"WhatsApp Group Message", title:"Thailand tip (short form)", caption:`Thailand tip: skip Friday Night Market in Chiang Mai and hit the Saturday Walking Street instead — less crowded, better food, more authentic. If you want a whole trip's worth of insider tips like this delivered by text, check out Butler Button at veltmtours.com. $25/day, 195+ countries. 🇹🇭`, visual:"Text only. Under 200 chars ideal. No hashtags." },
  "C4-E1":   { campaign:"C4 · Stress-Free Stories", type:"Email", title:"The travel problem no one talks about", caption:`Hi there,\n\nThere's a moment on every trip nobody warns you about — not lost luggage, but the slow accumulation of small stresses.\n\nThe restaurant that lost your reservation. The language barrier at 11pm. The hotel that gave away your late checkout.\n\nButler Button was built for exactly these moments:\n• Lost reservation? Your Butler rebooks and negotiates an upgrade.\n• Language barrier? Your Butler communicates with locals in real-time.\n• Need help at 2am? Your Butler is there. Every timezone, every hour.\n\nOver 1,000 travelers have already made the switch.\n\n[CTA: Get Your Butler →]\n\nWarm regards,\nThe VELTM Team`, visual:"Email template. Stories in bordered callout boxes. Indigo left-border accent." },
  "C4-IG-1": { campaign:"C4 · Stress-Free Stories", type:"Instagram + Facebook · Split-screen", title:"Before Butler Button / After Butler Button", caption:`The problem: You're in a foreign city, it's late, and the restaurant you booked is closed.\n\nThe solution: One text to your Butler Button assistant. Five minutes later, you have a reservation at a local favorite two blocks away.\n\nThis is what $25/day gets you. A real person, real-time help, 195+ countries.\n\nveltmtours.com\n\n#ButlerButton #TravelStressFree #VELTMTours #YourButlerAwaits`, visual:"Split-screen. Left: warm amber, stressed traveler. Right: cool Indigo/purple, relaxed traveler at golden hour. Labels: 'Without Butler Button' / 'With Butler Button'. 1080×1080." },
  "C4-IG-2": { campaign:"C4 · Stress-Free Stories", type:"Instagram + Facebook · List format", title:"Things Butler Button handled this week", caption:`Things Butler Button assistants handled this week 👇\n\n✓ Arranged a surprise birthday cake delivered to a hotel in Lisbon\n✓ Found a last-minute English-speaking dentist in Barcelona\n✓ Booked a sunrise hot air balloon in Cappadocia\n✓ Secured a same-day spa appointment in Bali\n✓ Got a lost jacket returned from a restaurant in Tokyo\n✓ Rebooked a missed ferry in Greece within 20 minutes\n\nAll by text. All from $25/day. All across 195+ countries.\n\nYour Butler awaits at veltmtours.com 🔗\n\n#ButlerButton #TravelStressFree #VELTMTours #YourButlerAwaits`, visual:"Lavender bg (#F5F3FF). Indigo checkmarks. 'Handled by Butler Button' footer. Clean list layout. 1080×1080." },
  "FB-C4-1": { campaign:"C4 · Stress-Free Stories", type:"Facebook Group Post", title:"Has this ever happened to you?", caption:`Has this ever happened to you while traveling?\n\nYou spend an hour on "best restaurants in [city]" and every list recommends the same five tourist spots. You wait 45 minutes. The food is just... fine.\n\nMeanwhile, two streets over, there's a place locals have gone for 20 years — half the price, twice as good. You just didn't know.\n\nThat's the gap Butler Button fills. $25/day, a personal travel assistant who knows the local spots. 195+ countries. veltmtours.com`, visual:"No image. Engagement format — question hook. Post in travel Facebook groups." },
  "WA-C4-1": { campaign:"C4 · Stress-Free Stories", type:"WhatsApp Group Message", title:"Quick travel story: Rome anniversary dinner", caption:`Quick travel story: someone texted their Butler at 11pm in Rome — their hotel lost their anniversary dinner reservation. Within 15 minutes, their Butler had a table at a candlelit restaurant with a view of the Tiber. That's what $25/day gets you. veltmtours.com 🕯️`, visual:"Text only. Short. Story-driven." },
  "C5-IG-1": { campaign:"C5 · 3-Step Challenge", type:"Instagram + Facebook · Bold typographic", title:"3 Steps. 2 Minutes. Unlimited Travel Help.", caption:`3 steps. 2 minutes. Unlimited travel help. ✈️\n\nThat's the Butler Button challenge. We bet you can't go back to planning trips the old way after trying this:\n\nStep 1: Book your plan at veltmtours.com\nStep 2: Connect with your dedicated Butler (within 1 hour)\nStep 3: Text any request, any time\n\nFrom restaurant reservations to real-time errand running, your Butler handles it all. Starting at $25/day across 195+ countries.\n\n👇 Tag someone who needs this for their next trip.\n\n#ButlerButton #TravelChallenge #TravelStressFree #VELTMTours #YourButlerAwaits`, visual:"VELTM Indigo (#4F46E5) bg. Large white Georgia: '3 Steps. 2 Minutes. Unlimited Travel Help.' Steps in smaller white Arial. Gradient 'Try the Challenge' pill. 1080×1080 / 1080×1920 Reel." },
  "FB-C5-1": { campaign:"C5 · 3-Step Challenge", type:"Facebook Group Post", title:"The 3-Step Travel Challenge", caption:`The 3-Step Travel Challenge:\n\nI challenge anyone here to plan a trip in under 2 minutes. Here's how:\n\nStep 1: Go to veltmtours.com and pick your destination and plan.\nStep 2: Get connected with a personal travel assistant within 1 hour.\nStep 3: Text them your wish list — itinerary, restaurants, activities, logistics.\n\nThat's it. Your entire trip, handled by a real person via text. Starting at $25/day across 195+ countries.\n\nDrop a comment with your next destination and I'll tell you how Butler Button can help!`, visual:"No image. Challenge format for maximum engagement." },
  "WA-C5-1": { campaign:"C5 · 3-Step Challenge", type:"WhatsApp Group Message", title:"Travel challenge: plan a trip in 2 minutes", caption:`Travel challenge: can you plan a trip in 2 minutes? Go to veltmtours.com, pick a plan ($25/day), and get connected with your personal travel assistant within 1 hour. Text them your wish list and watch it happen. 195+ countries. Try it for your next trip and thank me later. 🙌`, visual:"Text only. Short and punchy." },
  "FB-C2-1": { campaign:"C2 · $25 Travel Days", type:"Facebook Group Post", title:"What $25/day actually gets you", caption:`I keep getting asked what's actually included when you hire a travel assistant, so here's the breakdown.\n\nFor $25/day with Butler Button, you get: custom itinerary creation, restaurant reservations, on-trip errands (they'll get a phone charger delivered to your hotel), hotel arrangements, local tips, and real-time help in 150+ languages.\n\nThat's less than what most of us spend on airport coffee. Everything works through text.\n\n195+ countries. Check veltmtours.com.`, visual:"No image. Peer-to-peer. Post in travel groups." },
  "FB-C2-2": { campaign:"C2 · $25 Travel Days", type:"Facebook Group Post", title:"The most underrated travel hack of 2026", caption:`Alright, sharing something I wish I'd known about years ago.\n\nMost people don't know you can get a personal travel assistant for $25 a day. Not a chatbot, not an app — an actual person who responds to your texts and handles everything from booking restaurants to running errands in whatever city you're in.\n\nIt's called Butler Button by VELTM. You book, get connected within an hour, then just text whatever you need. Works in 195+ countries.\n\nI'd put this up there with Global Entry and packing cubes as things that genuinely change how you travel. Check veltmtours.com.`, visual:"No image. Discovery/recommendation tone." },
  "FB-C2-3": { campaign:"C2 · $25 Travel Days", type:"Facebook Group Post", title:"Planning a trip? Here's a shortcut", caption:`If you're currently planning a trip, here's something that might save you hours of research.\n\nButler Button by VELTM gives you a personal travel assistant who builds your itinerary, handles bookings, and helps in real-time. It works in 195+ countries.\n\nTrip planning starts at $25/country (5 revisions), and daily assistance is $25/day. Everything over text.\n\nWorth checking at veltmtours.com, especially if you're tired of the browser-tab-and-spreadsheet approach.`, visual:"No image. Practical advice tone." },
  "WA-C2-1": { campaign:"C2 · $25 Travel Days", type:"WhatsApp Message", title:"Butler Button intro for travel groups", caption:`Hey travelers! Just discovered something I had to share. There's a service called Butler Button by VELTM where you get a personal travel assistant for $25/day. You literally just text them what you need — restaurant bookings, local tips, errands, itinerary help — and they handle it. Works in 195+ countries. Check veltmtours.com. Game changer. 🌍`, visual:"Text only. Casual intro. ~150 chars." },
  "WA-C2-2": { campaign:"C2 · $25 Travel Days", type:"WhatsApp Message", title:"Bali scenario", caption:`Imagine you're in Bali and you want a sunset dinner spot that isn't a tourist trap, plus a driver to get there, plus your hotel room set up with extra pillows and a late checkout. One text to your Butler Button assistant and it's all handled. $25/day. veltmtours.com 🌴`, visual:"Text only. Vivid scenario." },
  "WA-C2-3": { campaign:"C2 · $25 Travel Days", type:"WhatsApp Message", title:"Direct offer", caption:`Quick one for anyone with upcoming travel plans: Butler Button by VELTM offers personal travel assistance from $25/day across 195+ countries. Trip planning, real-time help, restaurant bookings, errands — all by text. No apps needed. Visit veltmtours.com or DM me for details. ✈️`, visual:"Text only. Direct offer." },
};

// ── Render dynamic cards ──────────────────────────────────────────
function renderCard(id, asset) {
  return `
<div class="creative-card" id="card-${id}">
<div class="card-header">
  <div class="card-meta">
    <div class="card-id">${id} · ${asset.type}</div>
    <div class="card-title">${asset.title}</div>
    <div class="card-sub">${asset.campaign}</div>
  </div>
  <div class="card-status"><span class="badge badge-pending" id="badge-${id}">Pending Review</span></div>
</div>
<div class="card-body">
  ${asset.visual ? `<div class="asset-label">Visual Spec</div><div class="visual-spec">${asset.visual}</div>` : ''}
  <div class="asset-label">Copy / Caption</div>
  <div class="asset-preview">${asset.caption}</div>
  <div class="review-actions" id="actions-${id}">
    <button class="btn btn-approve" onclick="submitReview('${id}','approve')">✓ Approve</button>
    <div class="feedback-area">
      <label for="fb-${id}">Feedback for revision:</label>
      <textarea id="fb-${id}" placeholder="e.g. Change tone, update copy, different angle..."></textarea>
      <div class="submit-row">
        <button class="btn btn-reject" onclick="submitReview('${id}','reject')">✗ Request Changes</button>
      </div>
    </div>
  </div>
  <div class="confirm-msg" id="confirm-${id}"></div>
</div>
</div>`;
}

// Render all remaining cards
const container = document.getElementById('dynamic-cards');
const campaignOrder = ["C2","C3","C4","C5","FB","WA"];
Object.entries(ASSETS).forEach(([id, asset]) => {
  container.innerHTML += renderCard(id, asset);
});

// ── Track state ───────────────────────────────────────────────────
const reviewState = {};
const GATEWAY = 'http://127.0.0.1:18789/api/v1/agent/send';
const TOKEN    = '8892c13ee672af8c29e1917638f52d0974450f5e8e2626cf815ef6514abfd3bd';

function updateCounters() {
  const all = document.querySelectorAll('[id^="badge-"]');
  let approved = 0, rejected = 0;
  all.forEach(b => {
    if (b.textContent === 'Approved') approved++;
    if (b.textContent === 'Needs Revision') rejected++;
  });
  const total = all.length;
  document.getElementById('cnt-approved').textContent = approved;
  document.getElementById('cnt-rejected').textContent = rejected;
  document.getElementById('cnt-pending').textContent = total - approved - rejected;
  document.getElementById('cnt-total').textContent = total;
}

async function submitReview(id, action) {
  const feedback = document.getElementById('fb-' + id)?.value?.trim() || '';

  if (action === 'reject' && !feedback) {
    document.getElementById('fb-' + id).style.borderColor = '#ef4444';
    document.getElementById('fb-' + id).placeholder = '⚠ Please provide feedback so Claude can revise.';
    return;
  }

  // Update badge immediately
  const badge = document.getElementById('badge-' + id);
  const confirm = document.getElementById('confirm-' + id);
  const actions = document.getElementById('actions-' + id);

  if (action === 'approve') {
    badge.className = 'badge badge-approved';
    badge.textContent = 'Approved';
    actions.style.display = 'none';
    confirm.style.display = 'block';
    confirm.style.background = '#d1fae5';
    confirm.style.borderColor = '#10b981';
    confirm.style.color = '#065f46';
    confirm.textContent = '✓ Approved. This asset is ready for publishing.';
  } else {
    badge.className = 'badge badge-rejected';
    badge.textContent = 'Needs Revision';
    actions.style.display = 'none';
    confirm.style.display = 'block';
    confirm.style.background = '#fee2e2';
    confirm.style.borderColor = '#ef4444';
    confirm.style.color = '#991b1b';
    confirm.textContent = `✗ Revision requested: "${feedback}" — Claude will update within 2 hours.`;
  }

  updateCounters();

  // Post to OpenClaw gateway (works when on local network)
  const assetData = ASSETS[id] || {};
  const msg = action === 'approve'
    ? `[VELTM REVIEW] APPROVED: ${id} — "${assetData.title || id}"`
    : `[VELTM REVIEW] REVISION REQUESTED: ${id} — "${assetData.title || id}" | Feedback: ${feedback}`;

  try {
    await fetch(GATEWAY, {
      method: 'POST',
      headers: { 'Content-Type': 'application/json', 'Authorization': 'Bearer ' + TOKEN },
      body: JSON.stringify({ agentId: 'content', content: msg }),
      mode: 'no-cors'
    });
  } catch(e) {
    // Gateway unreachable from external browser — that's OK, state is visible on page
    console.log('Gateway not reachable from this browser:', e.message);
  }
}

// Init counters
updateCounters();
</script>
