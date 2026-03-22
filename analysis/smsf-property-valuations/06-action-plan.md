# Action Plan — Prioritised by Impact

**Site:** smsfpropertyvaluations.com.au

---

## Phase 1: Fix What's Broken (Week 1-2)

### 1.1 Investigate & Fix the 403 Blocking Issue
**Priority:** CRITICAL
**Impact:** Everything else depends on this

- [ ] Log into WordPress admin and check security plugins (Wordfence, Sucuri, iThemes, etc.)
- [ ] Check "Block non-browser user agents" or "Block crawlers" settings
- [ ] If using Cloudflare: check Firewall Rules, Security Level, and Bot Fight Mode settings
- [ ] Verify Googlebot can crawl: use Google Search Console → URL Inspection
- [ ] Test: `curl -I https://smsfpropertyvaluations.com.au` from multiple locations
- [ ] Check server access logs for 403 responses to search engine bots
- [ ] If hosting has a WAF (Web Application Firewall), whitelist Googlebot IPs

### 1.2 Fix Duplicate Homepage
**Priority:** High
**Time:** 15 minutes

- [ ] In WordPress: Settings → Reading → verify static front page is set to the correct page
- [ ] Install Redirection plugin (or use Rank Math/Yoast redirect manager)
- [ ] Create 301 redirect: `/home-2/` → `/`
- [ ] Verify redirect works

### 1.3 Fix Broken Blog URL
**Priority:** Medium
**Time:** 5 minutes

- [ ] Create 301 redirect: `/blog/smsf/transfer-property-into-smsf/` → `/transfer-property-into-smsf/`
- [ ] Check Google Search Console for additional 404 errors
- [ ] Fix any other broken URLs found

### 1.4 Verify XML Sitemap
**Priority:** High
**Time:** 15 minutes

- [ ] Check if `/sitemap.xml` is accessible (currently returning 403)
- [ ] If using Yoast: Settings → XML Sitemaps → Enable
- [ ] If using Rank Math: Sitemap Settings → Enable
- [ ] Submit sitemap in Google Search Console
- [ ] Verify robots.txt references the sitemap

---

## Phase 2: Consolidate & Redirect (Week 2-3)

### 2.1 Merge Duplicate Commercial Pages
**Time:** 2-3 hours

| Action | From | To |
|---|---|---|
| 301 redirect | `/commercial-property-valuations/` | `/best-commercial-property-valuations/` |
| 301 redirect | `/commercial-property-values-2/` | `/commercial-property-value/` |
| 301 redirect | `/free-commercial-property-valuation-calculator/` | `/commercial-property-valuation-calculator/` |
| 301 redirect | `/commercial-property-valuation-free/` | `/commercial-property-valuation-calculator/` |

- [ ] Before redirecting, merge the best content from duplicate pages into the surviving page
- [ ] Update internal links sitewide to point to surviving URLs
- [ ] Verify redirects work

### 2.2 Remove Off-Topic Content
**Time:** 30 minutes

- [ ] `/commercial-property-insurance/` → noindex or redirect to commercial page
- [ ] `/bank-property-valuation-confirm-the-propertys-market-value/` → noindex or redirect
- [ ] `/ground-property-group/` → review purpose, noindex if not valuable
- [ ] `/commercial-property-valuer-sydney/` → redirect to `/property-valuation-sydney/` (after rewriting Sydney page)

---

## Phase 3: Create High-Priority Content (Week 3-6)

### 3.1 Division 296 Content Hub (URGENT — before July 2026)
**Time:** 4-6 hours to write
**Impact:** Highest potential new content piece

- [ ] Create `/division-296-smsf-property-valuations/`
- [ ] Cover: what Division 296 is, how it affects property valuations, $3M threshold, why accurate annual valuations matter, risks of under/overstating, preparation checklist
- [ ] Include internal links to service pages and order CTA
- [ ] Add FAQ schema
- [ ] Target: "division 296 smsf valuation," "division 296 property valuation"

### 3.2 Residential Valuations Page
**Time:** 2-3 hours

- [ ] Create `/residential-property-valuations/`
- [ ] Cover: what's included in a residential report (8-10 pages), methodology, comparable sales analysis, pricing ($245), turnaround, order process
- [ ] Add sample report download link
- [ ] Target: "smsf residential property valuation," "smsf house valuation"

### 3.3 For Accountants & Auditors Page
**Time:** 2-3 hours

- [ ] Create `/for-accountants/`
- [ ] Cover: bulk ordering, account-based billing, what auditors need to see, ATO compliance documentation, white-label options if available
- [ ] Target: "smsf valuation for accountants," "smsf property valuation bulk"

### 3.4 ATO Compliance Requirements Guide
**Time:** 3-4 hours

- [ ] Create `/smsf-valuation-ato-requirements/`
- [ ] Cite and explain ATO guidelines (link to ato.gov.au source)
- [ ] Cover: what the ATO requires, frequency, acceptable valuation types, what auditors look for, contravention risks
- [ ] Target: "smsf valuation ato requirements," "ato smsf property valuation guidelines"

---

## Phase 4: Optimise Existing Pages (Week 4-6)

### 4.1 Fix City Page Titles & Content
**Time:** 1-2 hours per page

| Page | Current Title | New Title |
|---|---|---|
| `/property-valuation-sydney/` | Property Valuation Sydney - Accurate and Reliable Results | SMSF Property Valuation Sydney \| ATO Compliant from $245 |
| `/property-valuation-melbourne/` | Property Valuation Melbourne: Buyer & Seller Guide | SMSF Property Valuation Melbourne \| From $245, Same-Day |
| `/property-valuation-brisbane/` | Property Valuation Brisbane \| SMSF Property Valuations | SMSF Property Valuation Brisbane \| ATO Compliant Reports |

For each city page:
- [ ] Update title tag and H1 to include "SMSF"
- [ ] Add city-specific market context (median prices, growth rates)
- [ ] Mention local suburbs/regions covered
- [ ] Include turnaround time and pricing
- [ ] Add ordering CTA

### 4.2 Create Missing City Pages
**Time:** 2 hours per page

- [ ] `/property-valuation-perth/`
- [ ] `/property-valuation-adelaide/`
- [ ] `/property-valuation-hobart/`
- [ ] `/property-valuation-canberra/`
- [ ] `/property-valuation-gold-coast/`

Follow the same template as optimised Sydney/Melbourne/Brisbane pages.

### 4.3 Add Schema Markup Sitewide
**Time:** 2-3 hours

- [ ] Add ProfessionalService schema to homepage
- [ ] Add Service schema to residential and commercial pages
- [ ] Add FAQ schema to pages with FAQ sections
- [ ] Add BreadcrumbList schema
- [ ] Validate with Google's Rich Results Test

---

## Phase 5: Build Authority (Ongoing, Month 2+)

### 5.1 Set Up Google Business Profile
**Time:** 1 hour

- [ ] Create GBP listing for "SMSF Property Valuations"
- [ ] Use Caringbah, NSW address (or service-area business if no office visits)
- [ ] Add categories: "Property Valuation" + "Financial Service"
- [ ] Upload photos, logo, sample report preview
- [ ] Set service areas (all of Australia)
- [ ] Ask past clients for reviews

### 5.2 Review Generation Strategy
**Time:** Ongoing

- [ ] Add review request to post-delivery email workflow
- [ ] Create direct Google Review link and share with satisfied clients
- [ ] Aim for 10+ reviews within first 3 months
- [ ] Add review snippets to website (with schema)

### 5.3 Blog Content Calendar
**Monthly cadence:**

| Month | Topic | Target Keyword |
|---|---|---|
| April 2026 | "Division 296 and Your SMSF Property: What Changes in July" | division 296 smsf property |
| April 2026 | "SMSF Valuation 30 June: Your Annual Compliance Checklist" | smsf valuation 30 june |
| May 2026 | "How Often Should You Get an SMSF Property Valuation?" | smsf property valuation frequency |
| May 2026 | "SMSF Property Valuation Cost in 2026: Complete Guide" | smsf property valuation cost |
| June 2026 | "ATO Crackdown on Static SMSF Valuations: Are You at Risk?" | ato smsf valuation static |
| June 2026 | "Desktop vs Full Valuation for SMSF: Which Do You Need?" | desktop vs full smsf valuation |
| July 2026 | "Division 296 Is Here: What SMSF Trustees Need to Do Now" | division 296 effective date |
| August 2026 | "SMSF Retrospective Property Valuations Explained" | smsf retrospective valuation |

### 5.4 Link Building Opportunities
- [ ] **Accountants Daily** — already have one article; pitch more thought leadership
- [ ] **SMSF Adviser** — contribute expert commentary on valuation topics
- [ ] **SMSF Association** — explore member listing or content contribution
- [ ] **Accounting firm blogs** — offer guest posts on valuation requirements
- [ ] **BGL, Class Super, Simple Fund 360** — SMSF software providers who could list you as a partner
- [ ] **Local business directories** — ensure consistent NAP across all listings

---

## Quick Wins Checklist (Do This Week)

- [ ] Fix `/home-2/` redirect (15 min)
- [ ] Fix `/blog/smsf/transfer-property-into-smsf/` redirect (5 min)
- [ ] Investigate the 403 blocking issue (1 hour)
- [ ] Update city page titles to include "SMSF" (30 min)
- [ ] Start writing Division 296 content (this is time-sensitive)
- [ ] Set up Google Business Profile (1 hour)
