# Content Audit — Page-by-Page Review

**Site:** smsfpropertyvaluations.com.au

---

## Page Inventory & Assessment

### Homepage (`/`)
**Title:** SMSF Property Valuations - ATO Compliant Reports from $245 Online
**Grade:** B+

**Strengths:**
- Clear value proposition and pricing upfront
- ATO compliance messaging prominent
- Two service types clearly explained (residential $245, commercial $550)
- Turnaround times communicated

**Issues to Fix:**
- Verify H1 tag contains primary keyword "SMSF Property Valuations"
- Ensure the homepage doesn't compete with `/home-2/` (301 redirect the duplicate)
- Add FAQ schema for common questions
- Add testimonials/review snippets
- Add trust badges (API membership, certifications, money-back guarantee)
- Add a "For Accountants" CTA section

---

### Duplicate Homepage (`/home-2/`)
**Title:** SMSF Property Valuations - ATO Compliant - Australia
**Grade:** F — DELETE / REDIRECT

**Action:** 301 redirect to `/`. This page should not exist.

---

### Commercial Service Page (`/best-commercial-property-valuations/`)
**Title:** SMSF Commercial Property Valuations | ATO & Auditor Approved
**Grade:** B

**Strengths:**
- Good keyword in title
- Covers multiple commercial property types (office, retail, industrial)
- ATO compliance messaging

**Issues:**
- URL slug "best-commercial-property-valuations" uses "best" — a keyword-stuffing signal
- Competes with `/commercial-property-valuations/` for the same keyword
- Should be the ONE canonical commercial page

**Action:** Keep this as the primary commercial page. Redirect `/commercial-property-valuations/` here.

---

### Comprehensive Property Valuations (`/commercial-property-valuations/`)
**Title:** Comprehensive Property Valuations | SMSF Property Valuations
**Grade:** D — REDIRECT

**Issue:** Cannibalises `/best-commercial-property-valuations/`. The title doesn't even include "commercial" prominently.

**Action:** 301 redirect to `/best-commercial-property-valuations/`.

---

### Commercial Property Value Guide (`/commercial-property-value/`)
**Title:** Commercial Property Value Guide | SMSF Property Valuations
**Grade:** C

**Strengths:**
- Informational content that could rank for "commercial property value" queries
- Covers Melbourne valuation, SMSF valuations, CMA methodology

**Issues:**
- Generic commercial content, not SMSF-specific enough
- Competes with `/commercial-property-values-2/`

**Action:** Merge with `/commercial-property-values-2/` → keep this URL, redirect the other.

---

### Commercial Property Values: A Practical Guide (`/commercial-property-values-2/`)
**Title:** Commercial Property Values: A Practical Guide | SMSF
**Grade:** D — REDIRECT

**Issue:** The "-2" suffix screams "I couldn't think of a unique URL." Same topic as `/commercial-property-value/`.

**Action:** 301 redirect to `/commercial-property-value/`.

---

### Commercial Property Valuation Calculator (`/commercial-property-valuation-calculator/`)
**Title:** Commercial Property Valuation Calculator | SMSF Valuations
**Grade:** B-

**Strengths:**
- Interactive tool = good for engagement and time-on-site
- Targets "commercial property valuation calculator" keyword

**Issues:**
- Three separate calculator-related pages exist
- Consider whether the calculator actually works or is just content about calculators

**Action:** Keep as the single calculator page. Redirect `/free-commercial-property-valuation-calculator/` and `/commercial-property-valuation-free/` here.

---

### Free Commercial Property Valuation Calculator (`/free-commercial-property-valuation-calculator/`)
**Grade:** D — REDIRECT

**Action:** 301 redirect to `/commercial-property-valuation-calculator/`.

---

### Comprehensive Guide to Commercial Property Valuation (`/commercial-property-valuation-free/`)
**Grade:** D — REDIRECT

**Action:** 301 redirect to `/commercial-property-valuation-calculator/`.

---

### Transfer Property into SMSF (`/transfer-property-into-smsf/`)
**Title:** Transfer Property into SMSF | SMSF Property Valuations
**Grade:** B+

**Strengths:**
- Excellent niche topic with clear transactional intent
- Covers business real property, contribution/sale value, CGT implications
- Unique content not covered by most competitors

**Issues:**
- Old blog URL (`/blog/smsf/transfer-property-into-smsf/`) returns 404 — needs redirect
- Could be expanded with more detail on in-specie transfers

**Action:** Keep. Fix the 404 redirect. Consider expanding with Division 296 implications.

---

### SMSF Property Valuation and Divorce (`/smsf-property-valuation-divorce/`)
**Title:** SMSF Property Valuation and Divorce: Why Independent Valuation Is Essential
**Grade:** A-

**Strengths:**
- Excellent niche topic — few competitors cover this
- References Family Law Act 1975
- Strong transactional intent (people going through divorce NEED a valuation)
- Good title with emotional and practical appeal

**Issues:**
- Could add more detail on the process (how to order, what's included, timelines)
- Add internal links to main service pages

**Action:** Keep. Minor updates. This is one of the best pages on the site.

---

### Valuation Methods Explained (`/smsf-property-valuation-methods-explained/`)
**Title:** Valuation Methods Explained | SMSF Property Valuations
**Grade:** B

**Strengths:**
- Educational content builds E-E-A-T
- Covers regulatory fundamentals

**Issues:**
- Title could be more keyword-rich: "SMSF Property Valuation Methods Explained: A Trustee's Guide"
- Could link to ATO guidelines for authority

**Action:** Keep. Update title. Add links to ATO source and related pages.

---

### Property Valuation Sydney (`/property-valuation-sydney/`)
**Title:** Property Valuation Sydney - Accurate and Reliable Results
**Grade:** C+

**Issue:** Title is generic ("Property Valuation Sydney") — should be "SMSF Property Valuation Sydney" to match the niche and avoid competing with generic valuation firms.

**Action:** Update title to include "SMSF." Add Sydney-specific content (median prices, suburbs, local market conditions).

---

### Property Valuation Melbourne (`/property-valuation-melbourne/`)
**Title:** Property Valuation Melbourne: Buyer & Seller Guide
**Grade:** C

**Issue:** Same problem — too generic. "Buyer & Seller Guide" doesn't match SMSF intent at all.

**Action:** Rewrite with SMSF focus. Update title to "SMSF Property Valuation Melbourne | From $245."

---

### Property Valuation Brisbane (`/property-valuation-brisbane/`)
**Title:** Property Valuation Brisbane | SMSF Property Valuations
**Grade:** C+

**Issue:** Better than Melbourne/Sydney titles (includes brand name) but still too generic.

**Action:** Update title to "SMSF Property Valuation Brisbane | ATO Compliant Reports."

---

### Commercial Property Valuer Sydney (`/commercial-property-valuer-sydney/`)
**Title:** Best way how to work Commercial Property Valuer Sydney?
**Grade:** D

**Issues:**
- Title is grammatically broken: "Best way how to work Commercial Property Valuer Sydney?"
- This reads like AI-generated content with poor quality control
- Targets a generic keyword ("commercial property valuer sydney") that's off-niche

**Action:** Either rewrite completely with SMSF focus, or redirect to `/property-valuation-sydney/`.

---

### Commercial Property Insurance (`/commercial-property-insurance/`)
**Title:** Commercial Property Insurance | SMSF Property Valuations
**Grade:** D

**Issue:** Completely off-topic. An SMSF valuation firm shouldn't be writing about insurance. This doesn't serve conversion intent and dilutes topical authority.

**Action:** Either remove/noindex, or redirect to a relevant page. This is content bloat.

---

### Bank Property Valuation (`/bank-property-valuation-confirm-the-propertys-market-value/`)
**Title:** Bank Property Valuation: Confirm the Property's Market Value
**Grade:** D

**Issue:** Off-niche. Bank valuations are a different service. This doesn't align with the SMSF focus.

**Action:** Remove or noindex. Redirect if it has any backlinks.

---

### Ground Property Group (`/ground-property-group/`)
**Title:** Ground Property Group Insights | SMSF Property Valuations
**Grade:** D

**Issue:** Unclear purpose. Appears to reference an external brand. May be sponsored content or a partnership page.

**Action:** Review intent. If it's not driving relevant traffic, remove.

---

## Summary Score Card

| Grade | Pages | Action |
|---|---|---|
| **A-** | 1 (divorce page) | Keep, minor updates |
| **B to B+** | 5 (homepage, commercial, calculator, transfer, methods) | Keep, optimise |
| **C to C+** | 4 (city pages, commercial value) | Rewrite/update |
| **D** | 7+ (duplicates, off-topic, broken) | Redirect or remove |
| **F** | 1 (home-2) | Delete immediately |

---

## Content Health Summary

- **25+ indexed pages** but only ~6 are genuinely strong
- **8+ pages** should be consolidated via 301 redirects
- **3 pages** are off-topic and dilute authority
- **1 page** has broken grammar in the title
- **0 pages** cover Division 296 (the biggest SMSF topic of 2026)
- **0 pages** target residential SMSF valuations specifically
- **0 pages** target accountants/auditors as an audience
