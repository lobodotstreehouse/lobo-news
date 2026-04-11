---
layout: post
title: "VELTM Campaign Approval Dashboard"
date: 2026-04-10 18:00:00 -0400
author: orchestrator
categories: veltm
tags: [veltm, approval, dashboard]
hero_image: "https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?w=1200"
excerpt: "Central approval tracker for all VELTM Seven Springs campaign assets."
---

<style>
.dashboard-section { margin: 2rem 0; }
.dashboard-section h2 { color: #1a3c34; border-bottom: 3px solid #2d8a6e; padding-bottom: 8px; font-size: 1.4rem; }
.dashboard-section h3 { color: #333; font-size: 1.1rem; margin-top: 1.5rem; }
.overview-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 1rem; margin: 1rem 0; }
.overview-card { background: #f0f7f4; border-radius: 8px; padding: 1.2rem; border-left: 4px solid #2d8a6e; }
.overview-card .label { font-size: 0.8rem; color: #666; text-transform: uppercase; letter-spacing: 1px; margin: 0 0 4px; }
.overview-card .value { font-size: 1.1rem; color: #1a3c34; font-weight: bold; margin: 0; }
table.approval-table { width: 100%; border-collapse: collapse; margin: 1rem 0; font-size: 0.95rem; }
table.approval-table th { background: #1a3c34; color: #fff; padding: 10px 12px; text-align: left; font-weight: 600; font-size: 0.85rem; text-transform: uppercase; letter-spacing: 0.5px; }
table.approval-table td { padding: 10px 12px; border-bottom: 1px solid #e8e8e8; vertical-align: middle; }
table.approval-table tr:hover { background: #f9fafb; }
.status-badge { display: inline-block; padding: 3px 10px; border-radius: 12px; font-size: 0.8rem; font-weight: 600; white-space: nowrap; }
.status-draft { background: #fff3cd; color: #856404; }
.status-review { background: #fff3cd; color: #856404; }
.status-pending { background: #e8e8e8; color: #666; }
.status-approved { background: #d4edda; color: #155724; }
.status-blocked { background: #f8d7da; color: #721c24; }
.status-live { background: #cce5ff; color: #004085; }
.approval-chain { background: #f8f9fa; border-radius: 8px; padding: 1.5rem; margin: 1rem 0; }
.approval-step { display: flex; align-items: flex-start; margin: 0.8rem 0; padding-left: 0.5rem; }
.step-number { background: #2d8a6e; color: #fff; width: 28px; height: 28px; border-radius: 50%; display: inline-flex; align-items: center; justify-content: center; font-weight: bold; font-size: 0.85rem; margin-right: 12px; flex-shrink: 0; }
.step-text { padding-top: 3px; }
.checklist { list-style: none; padding: 0; margin: 1rem 0; }
.checklist li { padding: 8px 0; border-bottom: 1px solid #eee; font-size: 0.95rem; }
.checklist li:last-child { border-bottom: none; }
.gate-label { display: inline-block; background: #e8e8e8; color: #333; padding: 2px 8px; border-radius: 4px; font-size: 0.75rem; font-weight: 600; margin-left: 8px; text-transform: uppercase; }
</style>

<!-- ============================================ -->
<!-- SECTION 1: CAMPAIGN OVERVIEW                 -->
<!-- ============================================ -->

<div class="dashboard-section">
<h2>Campaign Overview</h2>

<div class="overview-grid">
  <div class="overview-card">
    <p class="label">Target Audience</p>
    <p class="value">Seven Springs CC Snowbirds</p>
  </div>
  <div class="overview-card">
    <p class="label">Campaign Theme</p>
    <p class="value">Summer 2026 Grandkid Vacations</p>
  </div>
  <div class="overview-card">
    <p class="label">Entry Offer</p>
    <p class="value">Trip Planning &mdash; $25/country</p>
  </div>
  <div class="overview-card">
    <p class="label">Destinations</p>
    <p class="value">Bali, Thailand, Sri Lanka, Singapore, Philippines</p>
  </div>
</div>

<h3>Upsell Path</h3>

<table class="approval-table">
<thead>
<tr><th>Tier</th><th>Service</th><th>Price</th><th>Description</th></tr>
</thead>
<tbody>
<tr><td><strong>Entry</strong></td><td>Trip Planning</td><td>$25/country</td><td>Personalized family itinerary from local experts</td></tr>
<tr><td><strong>Mid</strong></td><td>8-Hour Concierge</td><td>$25/day</td><td>Daytime local support for activities and logistics</td></tr>
<tr><td><strong>Premium</strong></td><td>24-Hour Concierge</td><td>$100/day</td><td>Round-the-clock dedicated concierge support</td></tr>
</tbody>
</table>
</div>

<!-- ============================================ -->
<!-- SECTION 2: EMAIL NURTURE SERIES              -->
<!-- ============================================ -->

<div class="dashboard-section">
<h2>Email Nurture Series &mdash; Approval Status</h2>

<table class="approval-table">
<thead>
<tr>
<th>#</th>
<th>Subject Line</th>
<th>Status</th>
<th>BizOps Draft</th>
<th>Carl (CSMO)</th>
<th>Ansh (CEO)</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>1</strong></td>
<td>This Summer, Give Your Grandkids the World</td>
<td><span class="status-badge status-draft">&#9203; Draft Ready</span></td>
<td><span class="status-badge status-approved">&#128994; Done</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
</tr>
<tr>
<td><strong>2</strong></td>
<td>Why Families Choose a Travel Concierge</td>
<td><span class="status-badge status-draft">&#9203; Draft Ready</span></td>
<td><span class="status-badge status-approved">&#128994; Done</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
</tr>
<tr>
<td><strong>3</strong></td>
<td>The Grandparents Who Changed Their Summers</td>
<td><span class="status-badge status-draft">&#9203; Draft Ready</span></td>
<td><span class="status-badge status-approved">&#128994; Done</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
</tr>
<tr>
<td><strong>4</strong></td>
<td>Top 5 Family Adventures in Southeast Asia</td>
<td><span class="status-badge status-draft">&#9203; Draft Ready</span></td>
<td><span class="status-badge status-approved">&#128994; Done</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
</tr>
<tr>
<td><strong>5</strong></td>
<td>Your First Trip Plan is Just $25</td>
<td><span class="status-badge status-draft">&#9203; Draft Ready</span></td>
<td><span class="status-badge status-approved">&#128994; Done</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
</tr>
</tbody>
</table>

<p><em>All 5 email HTML drafts created in Zoho Campaigns. Campaign assets ready for review.</em></p>
</div>

<!-- ============================================ -->
<!-- SECTION 3: INSTAGRAM CAMPAIGN                -->
<!-- ============================================ -->

<div class="dashboard-section">
<h2>Instagram Campaign &mdash; Approval Status</h2>

<table class="approval-table">
<thead>
<tr>
<th>Week</th>
<th>Asset</th>
<th>Format</th>
<th>Status</th>
<th>Content Draft</th>
<th>Carl (CSMO)</th>
<th>Ansh (CEO)</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>1</strong></td>
<td>&ldquo;Grandkids &amp; Getaways&rdquo; launch</td>
<td>Carousel</td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
</tr>
<tr>
<td><strong>1</strong></td>
<td>Bali family experience</td>
<td>Reel</td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
</tr>
<tr>
<td><strong>2</strong></td>
<td>Thailand cooking class</td>
<td>Story</td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
</tr>
<tr>
<td><strong>2</strong></td>
<td>Singapore family attractions</td>
<td>Carousel</td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
</tr>
</tbody>
</table>
</div>

<!-- ============================================ -->
<!-- SECTION 4: LANDING PAGE                      -->
<!-- ============================================ -->

<div class="dashboard-section">
<h2>Landing Page &mdash; Approval Status</h2>

<table class="approval-table">
<thead>
<tr><th>Element</th><th>Status</th><th>Details</th></tr>
</thead>
<tbody>
<tr>
<td><strong>Page URL</strong></td>
<td><span class="status-badge status-pending">&#9203; TBD</span></td>
<td>veltmtours.com/family (placeholder)</td>
</tr>
<tr>
<td><strong>Design</strong></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td>Layout and visual design awaiting creation</td>
</tr>
<tr>
<td><strong>Copy</strong></td>
<td><span class="status-badge status-draft">&#9203; Draft Ready</span></td>
<td>Aligned with email series messaging</td>
</tr>
<tr>
<td><strong>Form Fields</strong></td>
<td><span class="status-badge status-draft">&#9203; Specified</span></td>
<td>Name, Email, Trip Interest, Grandchildren Count, Preferred Dates</td>
</tr>
<tr>
<td><strong>Mobile Test</strong></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td>Responsive layout verification on mobile devices</td>
</tr>
<tr>
<td><strong>iPad Test</strong></td>
<td><span class="status-badge status-pending">&#9203; Pending</span></td>
<td>Tablet layout and touch target verification</td>
</tr>
</tbody>
</table>
</div>

<!-- ============================================ -->
<!-- SECTION 5: QA CHECKLIST                      -->
<!-- ============================================ -->

<div class="dashboard-section">
<h2>QA Checklist Summary</h2>

<p>Full test plan: <a href="/veltm/2026/04/10/veltm-test-plan.html">VELTM QA Test Plan</a></p>

<p><strong>Critical gates &mdash; all must pass before GO LIVE:</strong></p>

<ul class="checklist">
<li>&#9744; <strong>Pricing accuracy</strong> &mdash; All pricing matches SOP ($25/country trip planning, $25/day 8hr concierge, $100/day 24hr concierge) <span class="gate-label">Critical</span></li>
<li>&#9744; <strong>No Never Event language</strong> &mdash; Zero instances of banned phrases or claims <span class="gate-label">Critical</span></li>
<li>&#9744; <strong>8-country serviceability lock</strong> &mdash; Only Bali, Thailand, Sri Lanka, Singapore, Philippines, Vietnam, Cambodia, Malaysia referenced <span class="gate-label">Critical</span></li>
<li>&#9744; <strong>Multi-gen family imagery only</strong> &mdash; All photos show multi-generational families, no couples-only or solo imagery <span class="gate-label">Brand</span></li>
<li>&#9744; <strong>Font size >= 16px</strong> &mdash; All body text meets minimum readability standard <span class="gate-label">Accessibility</span></li>
<li>&#9744; <strong>Promise Guard passed</strong> &mdash; No guarantees, superlatives, or unsubstantiated claims <span class="gate-label">Legal</span></li>
</ul>
</div>

<!-- ============================================ -->
<!-- SECTION 6: APPROVAL CHAIN                    -->
<!-- ============================================ -->

<div class="dashboard-section">
<h2>Approval Chain</h2>

<div class="approval-chain">
<div class="approval-step">
<span class="step-number">1</span>
<span class="step-text"><strong>BizOps / Content agents</strong> draft all campaign assets (emails, social, landing page copy)</span>
</div>
<div class="approval-step">
<span class="step-number">2</span>
<span class="step-text"><strong>Carl Beauregard (CSMO)</strong> reviews each asset &mdash; approves or requests changes</span>
</div>
<div class="approval-step">
<span class="step-number">3</span>
<span class="step-text"><strong>Ansh Dixit (CEO)</strong> final brand approval on all customer-facing materials</span>
</div>
<div class="approval-step">
<span class="step-number">4</span>
<span class="step-text"><strong>Monitor agent</strong> runs full QA test plan against all approved assets</span>
</div>
<div class="approval-step">
<span class="step-number">5</span>
<span class="step-text"><strong>All tests pass</strong> &rarr; <span class="status-badge status-live">GO LIVE</span></span>
</div>
</div>
</div>

<!-- ============================================ -->
<!-- ZOHO CRM CONFIGURATION NOTES                 -->
<!-- ============================================ -->

<div class="dashboard-section">
<h2>Zoho CRM Configuration &mdash; Required Setup</h2>

<p><em>The following custom fields and pipeline need to be created in Zoho CRM. These require admin access to CRM Settings &gt; Modules &gt; Fields.</em></p>

<table class="approval-table">
<thead>
<tr><th>Field / Asset</th><th>Type</th><th>Values</th><th>Module</th><th>Status</th></tr>
</thead>
<tbody>
<tr>
<td><strong>Community</strong></td>
<td>Picklist</td>
<td>Seven Springs CC, Other</td>
<td>Contacts / Leads</td>
<td><span class="status-badge status-pending">&#9203; Manual Setup</span></td>
</tr>
<tr>
<td><strong>Trip Type</strong></td>
<td>Picklist</td>
<td>Multi-Gen Family, Couple, Solo, Group</td>
<td>Contacts / Leads</td>
<td><span class="status-badge status-pending">&#9203; Manual Setup</span></td>
</tr>
<tr>
<td><strong>Grandchildren Count</strong></td>
<td>Number</td>
<td>&mdash;</td>
<td>Contacts / Leads</td>
<td><span class="status-badge status-pending">&#9203; Manual Setup</span></td>
</tr>
<tr>
<td><strong>Preferred Season</strong></td>
<td>Picklist</td>
<td>Summer 2026, Fall 2026, Winter 2026-27</td>
<td>Contacts / Leads</td>
<td><span class="status-badge status-pending">&#9203; Manual Setup</span></td>
</tr>
<tr>
<td><strong>QA Status</strong></td>
<td>Picklist</td>
<td>Pending, India QA Approved, CSMO Approved, CEO Approved, Live</td>
<td>Deals</td>
<td><span class="status-badge status-pending">&#9203; Manual Setup</span></td>
</tr>
<tr>
<td><strong>VELTM Trip Planning Pipeline</strong></td>
<td>Deal Pipeline</td>
<td>Lead &rarr; Qualified &rarr; Trip Plan Sent &rarr; Concierge Upsell &rarr; Booked &rarr; Completed</td>
<td>Deals</td>
<td><span class="status-badge status-pending">&#9203; Manual Setup</span></td>
</tr>
</tbody>
</table>

<p><strong>Note:</strong> Zoho CRM custom field and pipeline creation requires admin UI access (Setup &gt; Customization &gt; Modules and Fields). The API does not support field creation on the free/standard tier. Carl should create these manually or delegate to the CRM admin.</p>
</div>
