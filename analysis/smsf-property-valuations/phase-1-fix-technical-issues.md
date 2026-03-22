# Phase 1: Fix Technical Issues — Step-by-Step

**Site:** smsfpropertyvaluations.com.au
**Timeline:** Week 1-2
**Priority:** CRITICAL — do this before anything else

---

## Step 1: Diagnose the 403 Blocking Issue

This is the #1 priority. The site is returning 403 Forbidden errors to automated requests, which may include search engine crawlers.

### 1.1 Check Google Search Console

1. Log into Google Search Console for smsfpropertyvaluations.com.au
2. Go to **Pages** (formerly "Coverage")
3. Look for:
   - "Blocked by robots.txt"
   - "Crawled — currently not indexed"
   - "Server error (5xx)"
   - "Soft 404"
4. Go to **Settings** → **Crawl stats** → check for 403 response codes
5. Use **URL Inspection** on your homepage — does Google see the full page?

**What to look for:** If Google shows your pages normally, the 403 may only affect non-Google bots (which is less critical but still hurts Ahrefs/SEMrush tracking). If Google is ALSO blocked, this is an emergency.

### 1.2 Check WordPress Security Plugins

Log into WordPress admin (`/wp-admin/`) and check these common plugins:

**Wordfence:**
- Wordfence → Firewall → Manage Firewall
- Look for "Rate Limiting" settings — if set too aggressively, it blocks crawlers
- Check "Blocked IPs" list for search engine bot IPs
- Whitelist Googlebot user agent

**Sucuri:**
- Sucuri Security → Settings → Scanner
- Check if "Block crawlers" or "Block automated requests" is enabled

**All In One WP Security:**
- WP Security → Firewall → check "5G Firewall" and "6G Firewall" settings
- Check "Block fake Googlebots" setting

**iThemes Security:**
- Security → Settings → check "Bot protection" settings

### 1.3 Check Cloudflare (if used)

1. Log into Cloudflare dashboard
2. Go to **Security** → **WAF** → check for rules blocking bots
3. Check **Security** → **Bots** → disable "Bot Fight Mode" for verified bots
4. Check **Security Events** log for blocked requests from Googlebot
5. Under **Rules** → check for any custom firewall rules blocking user agents

### 1.4 Check Hosting

- Contact your hosting provider (likely visible in cPanel or WordPress admin)
- Ask if they have any server-level bot blocking or WAF rules
- Request access logs to see how Googlebot requests are being handled

### 1.5 Test from Command Line

If you have terminal access, run:
```bash
# Test as a regular browser
curl -I https://smsfpropertyvaluations.com.au

# Test as Googlebot
curl -I -A "Mozilla/5.0 (compatible; Googlebot/2.1; +http://www.google.com/bot.html)" https://smsfpropertyvaluations.com.au

# Test as Ahrefs bot
curl -I -A "Mozilla/5.0 (compatible; AhrefsBot/7.0; +http://ahrefs.com/robot/)" https://smsfpropertyvaluations.com.au
```

If the browser UA returns 200 but the bot UAs return 403, you've found the problem.

---

## Step 2: Fix Robots.txt

### 2.1 Check Current robots.txt

Navigate to `https://smsfpropertyvaluations.com.au/robots.txt` in your browser (logged in).

**Ideal robots.txt for this site:**
```
User-agent: *
Allow: /

Sitemap: https://smsfpropertyvaluations.com.au/sitemap_index.xml
```

**Common mistakes to fix:**
- `Disallow: /` — blocks everything (catastrophic)
- `Disallow: /wp-admin/` — this is fine, keep it
- `Disallow: /wp-content/uploads/` — don't block this, Google needs to see PDFs and images
- Missing Sitemap directive

### 2.2 Update in WordPress

If using Yoast SEO:
- Yoast → Tools → File Editor → robots.txt

If using Rank Math:
- Rank Math → General Settings → Edit robots.txt

---

## Step 3: Fix XML Sitemap

### 3.1 Check if Sitemap Exists

Try these URLs in your browser:
- `https://smsfpropertyvaluations.com.au/sitemap.xml`
- `https://smsfpropertyvaluations.com.au/sitemap_index.xml`
- `https://smsfpropertyvaluations.com.au/wp-sitemap.xml` (WordPress default)

### 3.2 Enable/Generate Sitemap

**If using Yoast:**
- Yoast → General → Features → XML Sitemaps → Toggle ON

**If using Rank Math:**
- Rank Math → Sitemap Settings → Toggle ON

**If no SEO plugin:**
- Install Rank Math or Yoast SEO (recommended: Rank Math for this site)
- Enable XML Sitemaps

### 3.3 Submit to Google Search Console

1. Google Search Console → Sitemaps
2. Enter sitemap URL
3. Click Submit
4. Verify it shows "Success" status

---

## Step 4: Fix Duplicate Homepage

### 4.1 Check WordPress Settings

1. WordPress Admin → Settings → Reading
2. Verify "Your homepage displays" = "A static page"
3. Verify the correct page is selected as Homepage
4. Check if `/home-2/` is a separate WordPress page — if so, move it to Trash

### 4.2 Create 301 Redirect

**Using Rank Math:**
1. Rank Math → Redirections → Add New
2. Source URL: `/home-2/`
3. Destination URL: `/`
4. Redirect Type: 301 (Permanent)
5. Save

**Using Yoast Premium:**
1. Yoast → Redirects → Add Redirect
2. Old URL: `/home-2/`
3. New URL: `/`
4. Type: 301

**Using Redirection Plugin (free):**
1. Install "Redirection" plugin by John Godley
2. Tools → Redirection → Add New
3. Source: `/home-2/`
4. Target: `/`
5. Match: URL only
6. Action: Redirect to URL (301)

### 4.3 Verify

- Visit `https://smsfpropertyvaluations.com.au/home-2/`
- Confirm it redirects to `https://smsfpropertyvaluations.com.au/`
- Check with a redirect checker tool to verify it's a 301 (not 302)

---

## Step 5: Fix Broken Blog URL

### 5.1 Create 301 Redirect

Source: `/blog/smsf/transfer-property-into-smsf/`
Destination: `/transfer-property-into-smsf/`

Use the same redirect method as Step 4.2.

### 5.2 Check for Other 404s

1. Google Search Console → Pages → "Not found (404)"
2. Create 301 redirects for any pages that have a current equivalent
3. For pages with no equivalent, redirect to the most relevant page or homepage

---

## Step 6: Verify Canonical Tags

### 6.1 Check Each Major Page

For each important page, view source and look for:
```html
<link rel="canonical" href="https://smsfpropertyvaluations.com.au/page-slug/" />
```

**Every page should have a canonical tag pointing to itself** (unless it's intentionally canonicalised to another page).

### 6.2 Common WordPress Issues

- Some themes add canonical tags that conflict with SEO plugin canonicals (check for duplicates)
- Verify HTTP vs HTTPS in canonical URLs (should be HTTPS)
- Verify www vs non-www consistency (choose one, redirect the other)

---

## Step 7: Check HTTPS & Redirects

### 7.1 Verify HTTPS

- Visit `http://smsfpropertyvaluations.com.au` — should redirect to `https://`
- Visit `http://www.smsfpropertyvaluations.com.au` — should redirect to `https://smsfpropertyvaluations.com.au`
- Visit `https://www.smsfpropertyvaluations.com.au` — should redirect to `https://smsfpropertyvaluations.com.au`

All four variations should end at the same canonical URL.

### 7.2 WordPress Settings

- Settings → General → WordPress Address (URL) should be `https://smsfpropertyvaluations.com.au`
- Settings → General → Site Address (URL) should be `https://smsfpropertyvaluations.com.au`

---

## Step 8: Install/Configure SEO Plugin (if not already done)

### Recommended: Rank Math (Free)

1. Install Rank Math from WordPress plugin repository
2. Run the Setup Wizard
3. Configure:
   - Site type: Small Business
   - Business type: Professional Service
   - Business name: SMSF Property Valuations
   - Enable: Sitemap, Schema, Redirections, 404 Monitor
4. Set default schema to "ProfessionalService"

### Per-Page Settings

For each page, verify:
- Custom title tag (not auto-generated)
- Custom meta description
- Focus keyword set
- Schema type appropriate

---

## Phase 1 Completion Checklist

- [ ] 403 issue diagnosed and resolved (or confirmed Google is not affected)
- [ ] robots.txt is clean and allows crawling
- [ ] XML sitemap is accessible and submitted to Search Console
- [ ] `/home-2/` redirects to `/`
- [ ] `/blog/smsf/transfer-property-into-smsf/` redirects to `/transfer-property-into-smsf/`
- [ ] All pages have correct canonical tags
- [ ] HTTPS works correctly with proper redirects
- [ ] SEO plugin installed and configured
- [ ] Google Search Console shows no critical errors

**Do not proceed to Phase 2 until these are all done.** Technical issues undermine every other SEO effort.
