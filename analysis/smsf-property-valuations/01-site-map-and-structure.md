# Site Map & Structure Analysis

**Site:** smsfpropertyvaluations.com.au
**Platform:** WordPress (evidenced by `/wp-content/uploads/` paths)

---

## Indexed Pages (Discovered via Google)

### Core Service Pages
| URL | Title | Notes |
|---|---|---|
| `/` | SMSF Property Valuations - ATO Compliant Reports from $245 Online | Homepage |
| `/home-2/` | SMSF Property Valuations - ATO Compliant - Australia | **DUPLICATE HOMEPAGE — must fix** |
| `/best-commercial-property-valuations/` | SMSF Commercial Property Valuations \| ATO & Auditor Approved | Commercial service page |
| `/commercial-property-valuations/` | Comprehensive Property Valuations | **Potential cannibalisation with above** |
| `/transfer-property-into-smsf/` | Transfer Property into SMSF | Niche use case page |
| `/smsf-property-valuation-divorce/` | SMSF Property Valuation and Divorce | Niche use case page |
| `/smsf-property-valuation-methods-explained/` | Valuation Methods Explained | Educational content |

### City/Location Pages
| URL | Title | Status |
|---|---|---|
| `/property-valuation-sydney/` | Property Valuation Sydney | ✅ Exists |
| `/property-valuation-melbourne/` | Property Valuation Melbourne | ✅ Exists |
| `/property-valuation-brisbane/` | Property Valuation Brisbane | ✅ Exists |
| `/property-valuation-perth/` | — | ❌ Missing |
| `/property-valuation-adelaide/` | — | ❌ Missing |
| `/property-valuation-hobart/` | — | ❌ Missing |
| `/property-valuation-canberra/` | — | ❌ Missing |
| `/property-valuation-darwin/` | — | ❌ Missing |
| `/property-valuation-gold-coast/` | — | ❌ Missing |

### Blog/Content Pages
| URL | Title | Focus |
|---|---|---|
| `/commercial-property-value/` | Commercial Property Value Guide | Generic commercial info |
| `/commercial-property-values-2/` | Commercial Property Values: A Practical Guide | **Near-duplicate of above** |
| `/commercial-property-valuation-calculator/` | Commercial Property Valuation Calculator | Calculator tool |
| `/free-commercial-property-valuation-calculator/` | Free Commercial Property Valuation Calculator | **Near-duplicate of above** |
| `/commercial-property-valuation-free/` | Comprehensive Guide to Commercial Property Valuation | **Third near-duplicate** |
| `/commercial-building-valuation/` | Commercial Building Valuation: Expert Guide | Commercial content |
| `/commercial-property-valuer-sydney/` | Commercial Property Valuer Sydney | City + commercial |
| `/commercial-property-insurance/` | Commercial Property Insurance | Tangential topic |
| `/bank-property-valuation-confirm-the-propertys-market-value/` | Bank Property Valuation | Tangential topic |
| `/ground-property-group/` | Ground Property Group Insights | External brand reference |

### Known Broken URLs
| URL | Status |
|---|---|
| `/blog/smsf/transfer-property-into-smsf/` | **404 Error** — old blog URL structure |

---

## Structural Issues

### 1. Duplicate Homepage (`/home-2/`)
Two versions of the homepage exist. This splits link equity and confuses search engines. The `/home-2/` page should 301 redirect to `/`.

### 2. Commercial Content Cannibalisation
At least **6 pages** target variations of "commercial property valuation":
- `/best-commercial-property-valuations/`
- `/commercial-property-valuations/`
- `/commercial-property-value/`
- `/commercial-property-values-2/`
- `/commercial-property-valuation-calculator/`
- `/free-commercial-property-valuation-calculator/`
- `/commercial-property-valuation-free/`
- `/commercial-building-valuation/`

Google doesn't know which page to rank. These need to be consolidated or clearly differentiated with distinct keyword targets.

### 3. Missing Sitemap (Unconfirmed)
The sitemap at `/sitemap.xml` returned a 403 error. If the sitemap is blocked, Google may not discover all pages.

### 4. URL Structure Inconsistency
- Some URLs use descriptive slugs: `/transfer-property-into-smsf/`
- Others use awkward suffixes: `/commercial-property-values-2/`
- Blog content lives at root level (no `/blog/` prefix), mixing service and content pages

---

## Recommended Site Architecture

```
/ (Homepage)
├── /residential-property-valuations/          ← NEW dedicated page
├── /commercial-property-valuations/           ← Consolidate all commercial pages here
├── /smsf-property-valuation-calculator/       ← Single calculator page
├── /transfer-property-into-smsf/
├── /smsf-property-valuation-divorce/
├── /smsf-valuation-methods-explained/
├── /division-296-smsf-valuations/             ← NEW — high-priority
│
├── /locations/
│   ├── /property-valuation-sydney/
│   ├── /property-valuation-melbourne/
│   ├── /property-valuation-brisbane/
│   ├── /property-valuation-perth/             ← NEW
│   ├── /property-valuation-adelaide/          ← NEW
│   ├── /property-valuation-hobart/            ← NEW
│   ├── /property-valuation-canberra/          ← NEW
│   └── /property-valuation-gold-coast/        ← NEW
│
├── /blog/
│   ├── /smsf-valuation-ato-requirements/      ← NEW
│   ├── /smsf-valuation-30-june/               ← NEW
│   ├── /division-296-property-valuation-guide/ ← NEW
│   ├── /smsf-valuation-related-party/         ← NEW
│   └── /smsf-auditor-valuation-compliance/    ← NEW
│
├── /sample-report/
├── /for-accountants/                          ← NEW
├── /about/
├── /contact/
└── /order/
```
