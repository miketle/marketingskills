# PHASE 1: URGENT FIXES — Detailed Step-by-Step Guide (Week 1–2)

> Goal: Stop the bleeding. Fix the technical and structural issues causing Google to devalue the site.

---

## Step 1.1: Audit & Fix Crawler Access (Day 1)

### Why This Is Urgent
During our analysis, the site returned **403 Forbidden** to crawlers. If Googlebot gets the same response, your pages literally cannot be indexed or ranked.

### Steps

**A. Check robots.txt**
1. Open your website's CMS (likely WordPress based on URL structure)
2. Navigate to Settings → Reading → check "Discourage search engines from indexing this site" is **NOT checked**
3. Check your `robots.txt` file at `nationalaccounts.com.au/robots.txt`
4. It should contain at minimum:
```
User-agent: *
Allow: /
Sitemap: https://www.nationalaccounts.com.au/sitemap.xml
```
5. If using a security plugin (Wordfence, Sucuri, Cloudflare), check if it's blocking bots
6. If behind Cloudflare: go to Security → Bots → ensure "Definitely Automated" is set to **Allow** for verified bots, not Block

**B. Check for IP-based blocking**
1. In your hosting panel (cPanel, or ask your web host), check if there's an IP block list or firewall rules blocking known crawler IPs
2. Common culprit: Cloudflare "Under Attack" mode left on, or overly aggressive WAF rules

**C. Verify Googlebot access**
1. Go to Google Search Console → URL Inspection
2. Enter your homepage URL
3. Click "Test Live URL"
4. Check if Google can successfully fetch the page
5. If it shows errors, the hosting/security config needs fixing ASAP

**D. Check www vs non-www**
1. Type `nationalaccounts.com.au` (without www) in a browser
2. Then type `www.nationalaccounts.com.au`
3. Both should work, and one should **redirect to the other** (301 redirect)
4. If both serve content without redirecting, you have duplicate site issues
5. Fix: In your CMS or .htaccess, set the canonical domain (likely `www.nationalaccounts.com.au`) and 301 redirect the other

---

## Step 1.2: Submit & Verify XML Sitemap (Day 1)

### Steps

**A. Check if a sitemap exists**
1. Try visiting: `www.nationalaccounts.com.au/sitemap.xml`
2. If it doesn't exist and you're on WordPress, install **Yoast SEO** or **Rank Math** (if not already installed) — both auto-generate sitemaps

**B. Verify sitemap contents**
1. Open your sitemap — it should list EVERY page and blog post on the site
2. Check that it does NOT include:
   - The duplicate URL `/tax-planning/small-business-accountant-adelaide/` (will be redirected)
   - Any draft/private pages
   - Any thank-you/confirmation pages
3. Check that it DOES include all 30+ pages identified in the site map document

**C. Submit to Google Search Console**
1. Log into Google Search Console
2. Go to Sitemaps (left sidebar)
3. Enter your sitemap URL and click Submit
4. Check for any errors reported

**D. Submit to Bing Webmaster Tools**
1. If not already set up, create a Bing Webmaster Tools account
2. Submit the same sitemap

---

## Step 1.3: Fix the Duplicate Page — 301 Redirect (Day 2)

### The Problem
Two pages exist with essentially identical content:
- `/entrepreneur/business-accountants/` (KEEP this one)
- `/tax-planning/small-business-accountant-adelaide/` (REDIRECT this one)

### Steps (WordPress)

**Option A: Using a plugin (easiest)**
1. Install **Redirection** plugin (free) or use Yoast/Rank Math's redirect feature
2. Go to Tools → Redirection (or SEO → Redirects in Rank Math)
3. Add new redirect:
   - Source URL: `/tax-planning/small-business-accountant-adelaide/`
   - Target URL: `/entrepreneur/business-accountants/`
   - Type: **301 (Permanent)**
4. Save
5. Also redirect the entire `/tax-planning/` path if no other pages use it:
   - Source: `/tax-planning/` (with regex or wildcard)
   - Target: `/entrepreneur/`
   - Type: 301

**Option B: Using .htaccess (if comfortable)**
Add to your `.htaccess` file:
```apache
RedirectPermanent /tax-planning/small-business-accountant-adelaide/ /entrepreneur/business-accountants/
```

**After redirecting:**
1. Remove the old page from your sitemap (regenerate it)
2. In Google Search Console → URL Inspection → enter the old URL → Request Indexing (so Google discovers the redirect faster)

---

## Step 1.4: Fix the Orphaned Influencer URL (Day 2)

### The Problem
`/influencer/nobody-talks-about-taxes-as-an-influencer/` uses the path `/influencer/` which conflicts with `/influencer-services/`. This confuses Google's understanding of your site structure.

### Steps
1. Create a new page/post at `/blog/nobody-talks-about-taxes-as-an-influencer/`
2. Copy all content from the old page to the new one
3. Set up a 301 redirect:
   - Source: `/influencer/nobody-talks-about-taxes-as-an-influencer/`
   - Target: `/blog/nobody-talks-about-taxes-as-an-influencer/`
4. Update any internal links pointing to the old URL
5. If no other pages exist under `/influencer/`, redirect that path too:
   - Source: `/influencer/` → Target: `/influencer-services/`

---

## Step 1.5: Add Author Bios to Every Page (Day 3–4)

### Why This Is Critical
Google's December 2025 update specifically targeted YMYL content without demonstrated expertise. Tax advice without visible author credentials is now penalised.

### What Each Author Bio Needs
```
Written by [Full Name], [Qualification]
[Photo]
[Full Name] is a [Chartered Accountant / CPA / Registered Tax Agent]
with [X] years of experience specialising in [area].
[Registration/membership numbers].
Member of [CPA Australia / Chartered Accountants ANZ / Tax Practitioners Board].
```

### Steps for Blog Posts (WordPress)

**A. Create Author Profiles**
1. Go to Users → edit Michael Wilczynski's profile (and any other authors)
2. Fill in:
   - Biographical Info: Full paragraph with qualifications, experience, specialisations
   - Profile photo (professional headshot)
3. If using Yoast: go to SEO → Search Appearance → Archives → enable author archives

**B. Display Author Box on Posts**
1. If your theme doesn't show author bios, add one via:
   - Theme customiser (check if option exists)
   - A plugin like **Simple Author Box** (free)
   - Or ask your developer to add it to the blog post template
2. The author box should appear at the top or bottom of EVERY blog post

**C. Add Credentials to Service Pages**
1. For each service page, add a section like:
   ```
   Meet Your Accountant
   [Photo] [Name], [CA/CPA], Registered Tax Agent [number]
   [2-3 sentences about their specific expertise in this area]
   ```
2. This is especially important on Influencer and Entrepreneur hub pages

---

## Step 1.6: Add Trust Signals to Homepage (Day 4–5)

### What to Add (in order of impact)

**A. Professional Body Logos**
1. Get official logos for:
   - CPA Australia (if member)
   - Chartered Accountants Australia and New Zealand (if member)
   - Tax Practitioners Board (registered tax agent)
   - Xero Partner / Xero Certified Advisor (if applicable)
2. Add these as a logo bar/strip near the top of the homepage (above the fold ideally)
3. Link each logo to your profile on that body's website

**B. Google Reviews**
1. If you have Google reviews, embed them using a widget like **Elfsight** or **Widget for Google Reviews**
2. Display: star rating + number of reviews + 2–3 featured review excerpts
3. Place this prominently on the homepage

**C. Client Testimonials**
1. Add 3–5 real client testimonials with:
   - Client name (or initials + industry)
   - Their platform or business type ("YouTube creator", "Small business owner")
   - Specific result if possible ("Saved $12,000 on my tax return")
2. Add these to the homepage AND to relevant service pages

---

## Step 1.7: Add Schema Markup (Day 5–7)

### What to Add and Where

**A. LocalBusiness Schema (Homepage)**
```json
{
  "@context": "https://schema.org",
  "@type": "AccountingService",
  "name": "National Accounts",
  "image": "[logo URL]",
  "url": "https://www.nationalaccounts.com.au",
  "telephone": "0881666705",
  "email": "info@nationalaccounts.com.au",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "Level 2, 70 Hindmarsh Square",
    "addressLocality": "Adelaide",
    "addressRegion": "SA",
    "postalCode": "5000",
    "addressCountry": "AU"
  },
  "priceRange": "$$",
  "openingHours": "Mo-Fr 09:00-17:00"
}
```

**How to add:**
1. If using Yoast: SEO → Search Appearance → set Organization schema
2. If using Rank Math: it has built-in Local SEO schema
3. Or manually: add the JSON-LD in a `<script type="application/ld+json">` tag in the `<head>` of your homepage (via theme header or a plugin like **Insert Headers and Footers**)

**B. FAQPage Schema (Service Pages + Blog Posts)**
1. Add an FAQ section to each service page (5–8 common questions)
2. Mark up with FAQPage schema — Rank Math and Yoast both have FAQ block support in the WordPress editor
3. This gives you a chance at FAQ rich snippets in search results

**C. Article Schema (Blog Posts)**
1. Yoast/Rank Math automatically add Article schema
2. Verify that the `author` field is populated with name and URL
3. Add `datePublished` and `dateModified` — ensure the "last updated" date is visible on the page

**D. BreadcrumbList Schema (All Pages)**
1. Enable breadcrumbs in Yoast (SEO → Search Appearance → Breadcrumbs → Enable)
2. Or enable in Rank Math (General Settings → Breadcrumbs)
3. Add breadcrumb output to your theme template if not already showing

---

## Step 1.8: Title Tag Overhaul (Day 5–7)

### How to Change Title Tags

**In WordPress with Yoast/Rank Math:**
1. Edit each page/post
2. Scroll to the SEO section (Yoast or Rank Math meta box)
3. Click "Edit snippet" or "Edit SEO title"
4. Enter the new title

### Title Tags to Change

| Page | Current Title | New Title |
|------|--------------|-----------|
| Homepage | National Accounts \| Adelaide's Leading Tax Accountants | Tax Accountants Adelaide \| Influencer & Small Business Accounting — National Accounts |
| Influencer Hub | Accountants & Tax Services for Influencers | Influencer Tax Accountants Australia \| YouTube, OnlyFans, TikTok — National Accounts |
| Entrepreneur Hub | Accounting Services for Entrepreneurs Australia | Entrepreneur Tax Accountants Australia \| Business Structures & Tax Planning — National Accounts |
| OnlyFans | OnlyFans Tax Accountants Australia | OnlyFans Tax Accountant Australia \| Creator Tax Returns & GST — National Accounts |
| YouTube | YouTube Tax Accountants & Services Australia | YouTube Tax Accountant Australia \| AdSense, Sponsorship & GST — National Accounts |
| TikTok | TikTok Tax Return Services Australia | TikTok Tax Accountant Australia \| Creator Tax Returns & BAS — National Accounts |
| Patreon | Patreon Tax Accountants Australia | Patreon Tax Accountant Australia \| Subscription Income & Tax — National Accounts |
| Business Accountants | Small Business Accounting Services | Small Business Accountant Australia \| BAS, Tax Returns & Growth Advice — National Accounts |
| Tax Accountants | Tax Accountant & Structure Planning Adelaide | Business Structure & Tax Planning Adelaide \| Trusts, Companies & SMSF — National Accounts |
| Dropshipping | Dropshipping Tax Accountants Australia | Dropshipping Tax Accountant Australia \| GST, BAS & Ecommerce Tax — National Accounts |
| Property Investing | Property Investment Services Australia | Property Investment Tax Accountant \| Negative Gearing, CGT & Depreciation — National Accounts |
| Bookkeeping | Bookkeeping Services for Businesses | Bookkeeping Services Australia \| Xero, BAS & Payroll — National Accounts |
| Construction | Construction & Trades Tax Accountant | Tradie Tax Accountant Australia \| Construction, Trades & Subcontractor Tax — National Accounts |
| Medical | Tax Accountants for Medical Professionals | Medical Professional Tax Accountant \| Doctors, Dentists & Healthcare — National Accounts |

### Also Update Meta Descriptions
For each page, write a unique meta description (150–160 characters) that:
- Includes the primary keyword
- Mentions "Adelaide" or "Australia" for geo-targeting
- Has a call-to-action ("Book a free consultation", "Get expert tax advice")
- Is NOT duplicated across pages

---

## Step 1.9: Add "Last Updated" Dates (Day 7)

### Why
Google's update rewards freshness signals. Showing "Last updated: March 2026" tells both users and Google the content is current.

### Steps
1. In WordPress, update each page/post (even a small edit triggers a new "modified" date)
2. Ensure your theme displays "Last updated on [date]" (not just "Published on [date]")
3. If your theme doesn't show this, add it via:
   - A plugin like **WP Last Modified Info**
   - Or a small code snippet in your theme's `functions.php`

### Priority Pages to Update First
1. All 5 influencer service pages (last updated Oct 2024)
2. All entrepreneur service pages
3. All blog posts from 2024
4. Homepage

---

## Phase 1 Completion Checklist

- [ ] Googlebot can crawl the site (no 403s)
- [ ] robots.txt allows all important paths
- [ ] XML sitemap exists and is submitted to GSC
- [ ] www vs non-www properly redirects
- [ ] Duplicate small business page redirected (301)
- [ ] Orphaned `/influencer/` page moved to `/blog/`
- [ ] Author bios with credentials on all pages
- [ ] Trust signals (logos, reviews) on homepage
- [ ] LocalBusiness schema on homepage
- [ ] FAQPage schema on service pages
- [ ] Article schema on blog posts
- [ ] Breadcrumbs enabled with schema
- [ ] All title tags updated
- [ ] All meta descriptions unique and optimised
- [ ] "Last updated" dates showing on all pages
- [ ] All changes verified in Google Search Console (Request Indexing on key pages)
