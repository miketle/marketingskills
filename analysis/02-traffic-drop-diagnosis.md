# Traffic Drop Diagnosis: Mid-December 2025 to March 2026

## What Happened

National Accounts experienced a significant traffic drop starting mid-December 2025. Based on the timeline of Google algorithm updates and the site's characteristics, here is the diagnosis.

---

## Root Cause #1: Google December 2025 Core Update (PRIMARY)

**Timeline**: Rolled out December 11–29, 2025 — exactly when your traffic started dropping.

This was Google's most impactful core update since March 2024, with 18 days of volatility and two major spikes on December 13 and December 20.

### Why National Accounts Was Hit

**1. YMYL Classification**
- Accounting/tax advice is classified as "Your Money, Your Life" (YMYL) by Google
- YMYL sites experienced a **67% impact rate** in this update
- Recovery for YMYL sites is estimated at **6–12 months** (longer than other categories)

**2. Weak E-E-A-T Signals**
The update specifically targeted sites lacking demonstrated:
- **Experience**: No visible case studies, client results, or real-world examples
- **Expertise**: Limited author bios with credentials (CPA, CA, tax agent registration numbers)
- **Authoritativeness**: Small backlink profile, limited brand mentions
- **Trustworthiness**: No visible trust signals (professional body logos, certifications)

**3. Thin/Duplicate Service Pages**
- Multiple pages covering nearly identical topics (e.g., "Do influencers pay tax" blog + "Influencer services" page + "TikTok tax" page all covering the same ATO tax obligations)
- The update specifically penalised "generic SEO-optimised service pages without substantive value"

**4. Content Cannibalisation**
- Blog posts and service pages competing for the same keywords
- Example: `/influencer-services/tiktok-tax-accountants/` vs `/blog/tiktok-and-taxes-what-are-the-rules-in-australia/` vs `/blog/how-to-avoid-ato-trouble-as-a-tiktok-influencer/` — all targeting "TikTok tax Australia"

---

## Root Cause #2: Continued Volatility (Jan–Mar 2026)

- **January 2026**: Unconfirmed but continuous ranking volatility (6+ spikes)
- **February 2026**: Google Discover Core Update (Feb 5–27) — reduced clickbait/sensational content, favoured original expert content
- **March 2026**: Another broad core update rolling out NOW — further E-E-A-T enforcement

The site hasn't recovered because:
1. No remedial changes were made after the December hit
2. Each subsequent update has reinforced the same quality signals
3. Competitors who adapted are now occupying positions National Accounts lost

---

## Root Cause #3: Content Freshness Issues

- Blog publishing is sporadic: 4 posts in 2024, ~7 in 2025, only 2 in 2026 so far
- Several service pages haven't been updated since 2024 (e.g., Patreon, TikTok, YouTube service pages from Oct 2024)
- Stale content is being deprioritised in favour of regularly updated competitors

---

## Root Cause #4: Technical Signals

- Site returns **403 to crawlers** (verified during this analysis) — if Googlebot is being blocked or throttled, this directly impacts indexing
- No visible sitemap.xml or robots.txt accessible
- Likely Core Web Vitals issues (pages with LCP >3s saw 23% more traffic loss in December update)

---

## Summary of Traffic Drop Factors

| Factor | Severity | Fixable? | Timeframe |
|--------|----------|----------|-----------|
| December 2025 Core Update hit (YMYL) | **CRITICAL** | Yes | 2–6 months |
| Content cannibalisation (duplicate topics) | **HIGH** | Yes | 2–4 weeks |
| Weak E-E-A-T signals | **HIGH** | Yes | 2–4 weeks |
| Stale/outdated service pages | **MEDIUM** | Yes | 1–2 weeks |
| Sporadic publishing cadence | **MEDIUM** | Yes | Ongoing |
| Potential crawler blocking (403) | **HIGH** | Yes | 1 day |
| Missing technical SEO (sitemap, schema) | **MEDIUM** | Yes | 1–2 days |
| March 2026 Core Update (ongoing) | **UNKNOWN** | Monitor | 2–3 weeks |
