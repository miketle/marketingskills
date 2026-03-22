# Duplicate & Cannibalising Content Audit

## Critical Duplicate Content Issues

### 1. DUPLICATE PAGE — Small Business Accounting
| Page A | Page B |
|--------|--------|
| `/entrepreneur/business-accountants/` | `/tax-planning/small-business-accountant-adelaide/` |
| "Small Business Accounting Services" | "Small Business Accounting Services" |
| Under entrepreneur hub | Orphaned under `/tax-planning/` |

**Action**: 301 redirect `/tax-planning/small-business-accountant-adelaide/` → `/entrepreneur/business-accountants/`. Delete the orphaned page.

---

## Content Cannibalisation Clusters

### 2. TikTok Tax — 3 Pages Competing
| URL | Title | Type |
|-----|-------|------|
| `/influencer-services/tiktok-tax-accountants/` | TikTok Tax Return Services Australia | Service page |
| `/blog/tiktok-and-taxes-what-are-the-rules-in-australia/` | TikTok and Taxes: Australian Tax Rules for Creators | Blog |
| `/blog/how-to-avoid-ato-trouble-as-a-tiktok-influencer/` | How to Avoid ATO Trouble as a TikTok Influencer | Blog |

**Cannibalising keywords**: "TikTok tax Australia", "TikTok influencer tax", "ATO TikTok"

**Action**:
- Keep service page as primary conversion page (commercial intent)
- Merge the two blog posts into ONE comprehensive guide (redirect the weaker one)
- Add internal links from consolidated blog → service page
- Differentiate: service page = "hire us", blog = "educational guide"

### 3. OnlyFans Tax — 5+ Pages Competing
| URL | Title | Type |
|-----|-------|------|
| `/influencer-services/onlyfans-tax-accountants/` | OnlyFans Tax Accountants Australia | Service |
| `/blog/do-you-have-to-pay-onlyfans-tax/` | OnlyFans and Tax: What Creators Need to Know | Blog |
| `/blog/do-you-need-to-charge-clients-gst-for-custom-onlyfans-content/` | Do OnlyFans Creators Need to Charge GST? | Blog |
| `/blog/how-proper-accounting-protects-onlyfans-creators-in-disputes/` | How Proper Accounting Protects OnlyFans Creators | Blog |
| `/blog/key-deadlines-for-onlyfans-tax-filing-in-australia/` | Key Deadlines for OnlyFans Tax Filing | Blog |
| `/blog/how-to-manage-tax-payments-as-a-full-time-onlyfans-creator/` | How to Manage Tax Payments as Full-Time Creator | Blog |

**Issue**: This is the most severe cannibalisation cluster. 6 pages all targeting "OnlyFans tax Australia" variants. Google is likely confused about which page to rank.

**Action**:
- Service page (`/influencer-services/onlyfans-tax-accountants/`) = primary commercial page
- Consolidate the 5 blog posts into 2 distinct articles:
  - **Article 1**: "The Complete OnlyFans Tax Guide for Australian Creators" (merge general tax + deadlines + managing payments)
  - **Article 2**: "GST, Disputes & Legal Protection for OnlyFans Creators" (merge GST + disputes)
- 301 redirect old URLs → new consolidated URLs
- Interlink: blogs → service page as CTA

### 4. Influencer Tax (General) — 3 Pages Competing
| URL | Title | Type |
|-----|-------|------|
| `/influencer-services/` | Accountants & Tax Services for Influencers | Service hub |
| `/blog/do-social-media-influencers-pay-tax/` | Do Influencers Pay Tax on Earnings? | Blog |
| `/influencer/nobody-talks-about-taxes-as-an-influencer/` | Nobody Talks About Taxes as an Influencer | Blog/Page |
| `/blog/legal-risks-and-tax-mistakes-content-creators-should-avoid/` | Legal Risks and Tax Mistakes Creators Should Avoid | Blog |

**Additional issue**: `/influencer/nobody-talks-about-taxes-as-an-influencer/` uses the path `/influencer/` which is different from `/influencer-services/` — this is confusing for site architecture AND Google.

**Action**:
- Move `/influencer/nobody-talks-about-taxes-as-an-influencer/` to `/blog/nobody-talks-about-taxes-as-an-influencer/` (301 redirect old URL)
- Keep "Do Influencers Pay Tax" as the evergreen pillar blog post
- Keep "Legal Risks" as separate (different angle — legal vs tax)
- Merge "Nobody Talks About Taxes" content into the "Do Influencers Pay Tax" post if substantially overlapping

### 5. YouTube Tax — 2 Pages Competing
| URL | Title | Type |
|-----|-------|------|
| `/influencer-services/youtube-tax-accountants/` | YouTube Tax Accountants & Services | Service |
| `/blog/how-gst-works-for-australian-youtubers-monetising-their-content/` | How GST Works for Australian YouTubers | Blog |
| `/blog/do-twitch-streamers-youtubers-pay-taxes/` | Do Twitch Streamers & YouTubers Pay Taxes? | Blog |

**Action**: These are actually reasonably differentiated (service vs GST-specific vs Twitch+YouTube combo). Minor issue. Add clear internal linking between them. The Twitch/YouTube combo post should link to BOTH the YouTube service page and a future Twitch service page.

### 6. Patreon Tax — 2 Pages Competing
| URL | Title | Type |
|-----|-------|------|
| `/influencer-services/patreon-tax-accountants/` | Patreon Tax Accountants Australia | Service |
| `/blog/is-patreon-tax-deductible-australia/` | Paying Taxes as an Artist on Patreon | Blog |

**Action**: These are reasonably differentiated. Strengthen internal linking between them.

---

## Repeated Content Themes Across All Pages

The following messaging appears on nearly every page in near-identical wording:

1. **"The ATO treats influencer income just like any other business income"** — appears on 5+ pages
2. **"$75,000 GST threshold"** — mentioned on 6+ pages with same explanation
3. **"$18,200 tax-free threshold"** — repeated across 4+ pages
4. **"You need a registered tax agent"** — identical CTA language on every page

**Action**: Each page should present this information with unique context, examples, and depth relevant to that specific platform/topic. Avoid copy-pasting the same paragraphs.

---

## Cannibalisation Impact Summary

| Cluster | Pages Competing | Severity | Est. Traffic Lost |
|---------|----------------|----------|-------------------|
| OnlyFans | 6 pages | **CRITICAL** | High |
| TikTok | 3 pages | **HIGH** | Medium-High |
| General Influencer Tax | 4 pages | **HIGH** | Medium |
| Small Business (duplicate) | 2 pages | **HIGH** | Medium |
| YouTube | 3 pages | **LOW** | Low |
| Patreon | 2 pages | **LOW** | Low |
