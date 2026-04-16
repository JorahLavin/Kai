---
type: knowledge-base
effort: rushbrook-production-and-business
last_updated: 2026-04-07
---

# Rushbrook Soap — Accumulated Knowledge Base

## 1. The Business

**Rushbrook Soap / Madstone Artisans LLC** — cold-process soapmaking operation run by Jorah and Myrriah (Myr). Framed explicitly as a community engagement framework for retirement, not a revenue-critical business. Approximately 20 craft shows of experience. Batch numbers currently around #144+.

**Myr's role:** Co-operator, perfumer, handles batch data entry into Inventora, manages labeling. Currently working from a growing backlog.

**Sales channels:** WooCommerce storefront at rushbrooksoap.com, hosted on Clearlight Communications (Don Crock, personal relationship since ~1998). In-person at craft markets.

**Legal entity:** Madstone Artisans LLC (set up via ZenBusiness, ~3 years ago; ZenBusiness subscription subsequently cancelled).

---

## 2. Product Lines — Established Recipes

All profiles now mixed at approximately **90°F** (down from former 115–130°F). Lower temperature driven originally by goat milk scorching risk in GMT, but has improved all profiles: no gel phase or gel circles, wider working window before trace, better particle dispersion.

### GMT (Goat Milk & Tallow)
| Parameter | Value |
|---|---|
| Superfat | 7% |
| Water:Lye ratio | 2.2:1 |
| Liquid structure | Half frozen goat milk, half water (total = lye × 2.2) |
| Default total oils | ~990g |
| Cure | 8 weeks |
| Variants | Scented and unscented |
| Batch size | 10-bar runs |

**Standard additives (% of total oils):** Kaolin clay 2.0%, Sodium Lactate 1.1%, Sodium Citrate 2.5%, EDTA 0.3%, Colorant ~0.15–0.2%, Scent 6.0%.

**Note:** Additive slot positions have varied between batches — template should use named rows, not positional slots.

---

### Basic
| Parameter | Value |
|---|---|
| Superfat | 5% |
| Water:Lye ratio | 2:1 |
| Default total oils | 990g |
| Cure | 8 weeks |
| Mold | Silicone-lined wooden boxes |
| Visual | Two-toned — Titanium Dioxide base, mica top |

**Oil profile:**
| Oil | % | SAP (NaOH) |
|---|---|---|
| Coconut Oil | 32% | 0.190 |
| Sunflower Oil | 32% | 0.135 |
| Palm Oil | 32% | 0.141 |
| Castor Oil | 4% | 0.128 |

**Standard additives:** Scent 6.0%, Sodium Lactate 1.1%, Sodium Citrate 2.5%, EDTA 0.3%, Colorant 1 (variable) 0.1%, Titanium Dioxide 0.3%.

**⚠️ Standing flag:** Honey is an intended ingredient that keeps getting skipped — remember to include in next batch.

**Note on water:** Batch 140 shows Water (+34g) as a fixed add-on. Needs to be an explicit labeled field; confirm with Jorah whether always 34g or batch-dependent.

---

### Salt Bars
| Parameter | Value |
|---|---|
| Superfat | 20% |
| Water:Lye ratio | 2:1 |
| Default total oils | 1,400g |
| Cure | 8 weeks |
| Mold | Flat 9-bar acrylic |
| Oil profile | Coconut Oil 100% (SAP 0.190) |

**Salt — defining characteristic:** Hawaiian Red Alaea Salt = 80% of total oil weight. Fixed, not user-adjustable.

**Standard additives:** Hawaiian Red Alaea Salt (80% of oils), Sodium Citrate 2.5%, Sodium Gluconate 0.5%, Scent 6.0%. No EDTA — Sodium Gluconate serves as second chelator.

---

### Mechanics / Gardeners
| Parameter | Value |
|---|---|
| Superfat | 3% |
| Water:Lye ratio | 1.75:1 |
| Default total oils | 2,200g |
| Cure | 6 weeks |
| Mold | W&W 20-bar silicone |
| Unmold | 48–72 hours |

**Oil profile:**
| Oil | % | SAP (NaOH) |
|---|---|---|
| Lard | 40% | 0.138 |
| Canola | 25% | 0.124 |
| Coconut Oil | 25% | 0.190 |
| Castor | 10% | 0.128 |

**Standard additives (% of total oils):** Pumice 3.0%, Sodium Citrate 1.5%, Charcoal 1.0%. Currently unscented by design.

**Process notes:**
- Disperse charcoal in castor oil before adding to batch — NOT in water
- Hand-mix pumice only — no stick blender after pumice addition (accelerates wear)
- Sold in 5-bar brick packages at a discount; unscented is a feature (price point + no scent fade in storage)

---

## 3. Luxe Line — In Development

### Shea-Forward Conditioning Bar (Test batch completed ~April 2026)
| Oil | % | Grams (400g batch) |
|---|---|---|
| Beef tallow | 35% | 140g |
| Coconut oil | 25% | 100g |
| Shea butter | 20% | 80g |
| Sweet almond oil | 12% | 48g |
| Castor oil | 5% | 20g |
| Jojoba | 3% | 12g |

Superfat: 7–8% | Water:lye: 2.2:1

Test split at trace (~200g per half):
- **Scent A:** Blueberry FO → June u-pick blueberry show, Rock Hill SC ⚠️ check for trace acceleration
- **Scent B:** "The Lullaby" by Black Tie Barn FO → IOLI lace convention, July ⚠️ confirm vendor usage rate

**Production deadline:** Blueberry bar must be batched by ~April 12 (8-week cure for June show).

### Luxe Pipeline (upcoming)
1. **Golden Hearth** — mango butter + cocoa butter + tallow + canola; warm vanilla/cardamom/orange scent
2. **Mineral Grove** — bentonite clay + sea salt + palm kernel; pending inventory check on clay

---

## 4. Lye Calculation — Master Formula

```
WeightedSAP = SUMPRODUCT(OilPercents, SAPValues)
LyeGrams    = TotalOils × (1 - Superfat%) × WeightedSAP
WaterGrams  = LyeGrams × WaterRatio
```

SAP values are fixed constants. Lye calculation belongs in the Excel workbook — LyeCalc.com is being eliminated. This is the highest-return workflow intervention identified.

---

## 5. Current Tools & Status

| Tool | Purpose | Status |
|---|---|---|
| Excel workbook | Recipe building, oil weights | Active — lye calc not yet integrated |
| LyeCalc.com | Lye/water cross-check | Being eliminated — awkward UI, unreliable persistence |
| SoapCalc | Former source of truth | Abandoned — unreliable loading |
| Inventora (~$228/yr) | Batch/inventory/COGS tracking | Active — Myr has growing backlog; replacement in scope |
| WooCommerce/WordPress | Storefront (rushbrooksoap.com) | Active, hosted on Clearlight |
| Clearlight Communications | Web hosting (Don Crock) | Active since ~1998 |
| Bramble Berry scent descriptions | Seed material for product copy | Available as raw input |
| Word process diary | Batch notes | Being replaced by database diary module |
| Mal workspace (GitHub: JorahLavin/Mal) | MT-based AI project workspace | Active on Windows machine |

---

## 6. The Workflow Problem

A classic double-entry trap across multiple handoff points:

```
Jorah builds recipe in Excel
        ↓
Cross-checks lye in LyeCalc.com          ← FRICTION / ERROR RISK
        ↓
Prints recipe sheet
        ↓
Myr re-keys values into Inventora        ← BACKLOG / ERROR RISK
        ↓
Jorah writes product description         ← DEFERRED INDEFINITELY
        ↓
Jorah extracts ingredients list          ← RE-KEYING
        ↓
Photos taken, matched to product         ← MEMORY-DEPENDENT
        ↓
WooCommerce product entry                ← MANUAL, SLOW
```

**Target state:** Recipe workbook is single source of truth. Lye calc lives in the sheet. Batch logging reads from the recipe. WooCommerce inputs flow from structured data.

---

## 7. Flask/MySQL Database — Architecture Decisions

### Confirmed infrastructure (Clearlight / Don Crock)
- PHP (version-selectable), MySQL (no database limit), Python, SSH, cron jobs, SSL, automatic backups
- **Flask confirmed as first-class** via Phusion Passenger (persistent WSGI — not CGI). This resolved the PHP vs. Python question in Flask's favor.
- SQLite accessible from terminal — good for local dev before MySQL deploy

### Key architectural decisions
1. **Build on Clearlight** — PocketBase, VPS, Supabase all considered and set aside
2. **"The workbook is the working surface. The database is the record"** — Excel stays as working environment; MySQL is system of record; no overwriting, each batch logged
3. **Flask/Python chosen** — Phusion Passenger confirmed makes it clean first-class deployment
4. **Local SQLite → Clearlight MySQL migration path** — build and test locally, deploy when ready
5. **Inventora replacement in scope but not urgent** — natural cancellation point once database is stable
6. **Batch diary is a first-class database feature** — Word-based diary not carried forward

### Intended database scope (long-term)
- Batch tracking (ingredients, weights, dates, notes, diary)
- Ingredient stock and cost tracking
- Inventory counts
- Sales and event tracking
- Curing calendars
- Income/expense summaries for tax time
- WooCommerce publishing inputs

### Architectural guardrails
- No 9-tab spreadsheet hydra
- No over-automation — build what removes re-keying, not what takes longer than the work itself
- No third-party SaaS dependency for core workflow
- Decade-durable — boring and reliable beats trendy

---

## 8. Product Copy Workflow

**Voice and style:** Warm, conversational, maker-centered, grounded, sensory. Forbidden words/punctuation: "indulge," "elegant," "gentle cleansing," em-dashes, en-dashes. Max 20% of sentences over 19 words.

**Style reference:** Hawaiian Red Salt Bar description (on file) is the primary voice sample.

**Reusable description prompt outputs:** product description (1–2 paragraphs), Yoast keyphrase, URL slug, meta description (~160 chars), short product description (1–2 sentences).

**Ingredient extraction format:** Descending by percentage, sentence case, proper nouns capitalized, bracketed comma-separated list. Include: oils, liquids, additives, chelators, colorants, fragrance, lye. Exclude: batch weight, mold type, cure dates, vendor names.

**AI-assisted, not automated:** Claude or Copilot generates drafts given recipe output + Bramble Berry scent descriptions as seeds + writing style samples. Human review required.

Both prompts to be stored in the database and surfaced in the product publishing workflow.

---

## 9. WooCommerce / WordPress — Site Notes

- **rushbrooksoap.com** on Clearlight (WordPress + WooCommerce)
- PayPal Payments plugin active; reCAPTCHA v3 issue resolved (plugin update + confirmed correct plugin was sourcing keys)
- WooCommerce product reviews enabled (verified purchasers only) — Myr wanted blog comments, WooCommerce reviews are the right mechanism instead
- Comment spam: registration required + moderation queue approach adopted (no Akismet subscription)
- Square used only at in-person markets (card reader); WooCommerce/PayPal handles online
- Virtual gift card feature: active consideration, not yet implemented
- Site has been neglected through winter 2025–2026; update sprint planned April 13–27 (product photography + descriptions)

---

## 10. Financial / Business Admin

- **ZenBusiness:** Cancelled; registered agent function absorbed (home address used)
- **Thread Bank:** Closed (was tied to ZenBusiness)
- **Inventora:** ~$228/yr Starter plan; replacement in scope, not urgent
- **Square:** In-person markets only; ~half of market payments now wallet/QR — Square reader use declining
- **Tax filing:** 2025 extension filed; spending/earning reports partially completed; not urgent
- **Clover/First Data merchant account:** Was dormant; PCI compliance obligations were an active question (resolved or deferred — confirm status)

---

## 11. Oils & Fats Inventory (Aging Stock — Pending)

Use-up oils to work through (as of early April 2026):
- Shea butter: ~9 lbs
- Sweet almond oil: 1.2 gal
- Palm kernel flakes: 9 lbs
- Mango butter: 2.5 lbs
- Cocoa butter: 40 oz total
- Lard: 0.8 gal
- Canola: 1 gal
- Jojoba: 1 pint
- Stearic acid: 3 lbs (reserved for hot-process experiment — not part of luxe pipeline)

**Full fats/oils inventory from Myr's machine: pending — needed for recipe development sessions.**

---

## 12. Molds

Moving nearly all production to **Winston & Walter (W&W) silicone molds** to standardize batter weight across batch sizes.

| Line | Mold |
|---|---|
| GMT | W&W silicone (10-bar) |
| Basic | Silicone-lined wooden boxes (multi-mold) |
| Salt Bars | Flat 9-bar acrylic |
| Mechanics | W&W 20-bar silicone |

---

## 13. Process Notes — Charcoal

- Functional sweet spot: **1.0%** of total oil weight for a black bar with manageable staining risk
- Range: 0.5% (dark gray, minimal staining) → 1.5% (deep black, moderate staining risk)
- **Disperse in castor oil** before adding to batch — not water (charcoal is hydrophobic; water dispersion causes re-agglomeration)
- Current Mechanics spec: 1.0%
