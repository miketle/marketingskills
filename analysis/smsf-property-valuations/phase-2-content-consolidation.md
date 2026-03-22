# Phase 2: Content Consolidation — Step-by-Step

**Site:** smsfpropertyvaluations.com.au
**Timeline:** Week 2-3
**Prerequisite:** Phase 1 technical fixes complete

---

## Why Consolidation Matters

The site has 8+ pages competing for variations of "commercial property valuation." When multiple pages target the same keyword, Google doesn't know which to rank — and often ranks none of them well. This is called **keyword cannibalisation**.

By merging weak pages into strong ones and redirecting, you:
- Consolidate link equity (any backlinks to old pages flow to the new one)
- Give Google a clear signal about which page to rank
- Reduce crawl waste
- Improve user experience

---

## Consolidation Plan

### Group 1: Commercial Service Pages

**Keep:** `/best-commercial-property-valuations/`
**Redirect to it:**
- `/commercial-property-valuations/` → 301 → `/best-commercial-property-valuations/`

**Before redirecting:**
1. Open both pages side by side
2. Copy any unique content from `/commercial-property-valuations/` that isn't in the target page
3. Add that content to `/best-commercial-property-valuations/`
4. Make sure the surviving page covers:
   - What SMSF commercial property valuations are
   - Property types covered (office, retail, industrial, warehouse, land)
   - What's included in the report (8-12 pages)
   - Pricing ($550+)
   - Turnaround (48 hours)
   - ATO compliance details
   - Ordering CTA
5. Create the 301 redirect
6. Update any internal links pointing to the old URL

---

### Group 2: Commercial Property Value Guides

**Keep:** `/commercial-property-value/`
**Redirect to it:**
- `/commercial-property-values-2/` → 301 → `/commercial-property-value/`

**Before redirecting:**
1. Merge unique content from `/commercial-property-values-2/` into `/commercial-property-value/`
2. Update the title: "Commercial Property Value Guide for SMSF Trustees"
3. Add SMSF-specific angle (currently too generic)
4. Include valuation methods (income approach, comparable sales, replacement cost)
5. Link to the service pages and calculator
6. Create the 301 redirect

---

### Group 3: Calculator Pages

**Keep:** `/commercial-property-valuation-calculator/`
**Redirect to it:**
- `/free-commercial-property-valuation-calculator/` → 301 → `/commercial-property-valuation-calculator/`
- `/commercial-property-valuation-free/` → 301 → `/commercial-property-valuation-calculator/`

**Before redirecting:**
1. Merge the best content from all three pages into the surviving page
2. Make sure the calculator tool/widget is on the surviving page
3. Update the title: "SMSF Commercial Property Valuation Calculator | Free Estimate"
4. Add context: "This calculator gives you a rough estimate. For an ATO-compliant valuation report, order here →"
5. Clear CTA linking to the service/order page
6. Create both 301 redirects

---

### Group 4: Off-Topic Pages

**Action:** Noindex or redirect

| Page | Recommended Action |
|---|---|
| `/commercial-property-insurance/` | Add `noindex` meta tag via SEO plugin. Don't delete yet in case it has internal links. |
| `/bank-property-valuation-confirm-the-propertys-market-value/` | Add `noindex` meta tag. Or redirect to homepage if it has backlinks. |
| `/ground-property-group/` | Review purpose. If no clear value, `noindex`. |
| `/commercial-property-valuer-sydney/` | Redirect to `/property-valuation-sydney/` after rewriting Sydney page (Phase 4). |

**How to noindex a page in Rank Math:**
1. Edit the page in WordPress
2. Rank Math meta box → Advanced tab
3. Set "Robots Meta" to "noindex"
4. Update the page

**How to noindex in Yoast:**
1. Edit the page
2. Yoast meta box → Advanced tab
3. "Allow search engines to show this page?" → No
4. Update

---

## Redirect Implementation Guide

### Using Rank Math (Recommended)

1. Go to Rank Math → Redirections
2. Click "Add New"
3. Fill in:
   - **Source URL:** `/old-page-slug/` (the page being redirected)
   - **Destination URL:** `/new-page-slug/` (the page you're keeping)
   - **Redirection Type:** 301 Permanent Redirect
4. Click "Add Redirection"

### Using .htaccess (Alternative)

If you prefer server-level redirects, add to `.htaccess`:

```apache
# Commercial service page consolidation
Redirect 301 /commercial-property-valuations/ /best-commercial-property-valuations/

# Commercial value guide consolidation
Redirect 301 /commercial-property-values-2/ /commercial-property-value/

# Calculator consolidation
Redirect 301 /free-commercial-property-valuation-calculator/ /commercial-property-valuation-calculator/
Redirect 301 /commercial-property-valuation-free/ /commercial-property-valuation-calculator/

# Duplicate homepage
Redirect 301 /home-2/ /

# Broken blog URL
Redirect 301 /blog/smsf/transfer-property-into-smsf/ /transfer-property-into-smsf/
```

---

## Internal Link Audit

After creating redirects, update internal links to point directly to the new URLs (don't rely on redirect chains).

### How to Find Internal Links to Update

1. In WordPress, search pages/posts for the old URL slug
2. Or use a plugin like "Better Search Replace" to find and replace URLs in the database:
   - Search: `smsfpropertyvaluations.com.au/commercial-property-valuations/`
   - Replace: `smsfpropertyvaluations.com.au/best-commercial-property-valuations/`
   - **Run as dry run first** to see what will change
   - Then run the actual replacement

### Navigation Menu Update

1. WordPress Admin → Appearance → Menus
2. Check if any redirected pages are in the navigation
3. Update menu items to point to the surviving pages
4. Save

---

## Post-Consolidation Verification

After all redirects are in place:

- [ ] Visit each old URL — verify it 301 redirects to the correct page
- [ ] Check no redirect chains (old → old2 → new — should be old → new directly)
- [ ] Verify surviving pages load correctly with merged content
- [ ] Check Google Search Console → Sitemaps → verify old URLs are not in sitemap
- [ ] Re-submit sitemap after changes
- [ ] Wait 1-2 weeks, then check Search Console for any new issues

---

## Summary: Before & After

### Before (Current State)
```
Commercial pages: 8 pages competing with each other
├── /best-commercial-property-valuations/
├── /commercial-property-valuations/
├── /commercial-property-value/
├── /commercial-property-values-2/
├── /commercial-property-valuation-calculator/
├── /free-commercial-property-valuation-calculator/
├── /commercial-property-valuation-free/
└── /commercial-building-valuation/
```

### After (Consolidated)
```
Commercial pages: 3 focused pages with clear roles
├── /best-commercial-property-valuations/    ← Service page (transactional)
├── /commercial-property-value/              ← Guide (informational)
└── /commercial-property-valuation-calculator/ ← Tool (engagement)
+ /commercial-building-valuation/            ← Keep if sufficiently different keyword
```

**Result:** 8 weak pages → 3-4 strong pages, each with a clear keyword target and consolidated link equity.
