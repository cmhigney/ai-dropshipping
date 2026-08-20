# Product Scorecard — Template & Rubric

Purpose: rank 20+ candidates objectively so we pick on evidence, not on which product
we happened to see last. Copy the [blank template](#blank-template) into
[candidates.md](candidates.md) once per candidate.

Two-stage process:

1. **Hard gates** — binary. Any single failure kills the candidate. No score is computed.
   This exists so a high score on "creative potential" can never rescue a product that is
   going to get us sued or banned.
2. **Weighted score** — 10 criteria, each scored 1–5, weighted to a total out of 5.00.

---

## Stage 1 — Hard gates (any FAIL = reject, do not score)

| # | Gate | Fails if |
|---|------|----------|
| G1 | **Ingestible / topical** | Supplements, vitamins, skincare with active claims, food, anything applied to skin with an efficacy claim. FDA exposure + ad-platform prohibition. Non-negotiable. |
| G2 | **Lithium batteries / powered electronics** | Contains a lithium cell, plugs into mains, or emits RF. Triggers hazmat shipping, FCC/UL exposure, and a return rate that eats the margin. |
| G3 | **Kids / infants / toys** | Marketed to or usable by under-12s. CPSIA testing, CPSC recall exposure, choking-hazard liability. |
| G4 | **Patent / trademark** | Design or utility patent found on the exact form factor, or the product is a knockoff of a branded item. Search USPTO + Google Patents on the *form*, not the name. |
| G5 | **Regulated category** | Medical device claims (incl. "Class I exempt" — the claim is what regulates you), lasers, weapons, vape, CBD, automotive safety parts. |
| G6 | **Restricted by ad platforms** | Appears on Meta or TikTok prohibited/restricted product lists. Check before, not after, the account is banned. |
| G7 | **Fragile or oversized** | Glass/ceramic, or >2 lb / longest dimension >18 in. Breakage and dimensional-weight surcharges. |
| G8 | **Margin floor** | Sell price ÷ **landed** cost < 3.0x. See [unit-economics.md](../docs/unit-economics.md) — landed cost includes duty and tariff, not just the supplier's unit price. |

> Gate G8 uses landed cost, and landed cost is not the AliExpress sticker price. Compute it
> properly before you gate on it — see the landed-cost worksheet in `docs/unit-economics.md`.

---

## Stage 2 — Weighted scoring

| # | Criterion | Weight |
|---|-----------|-------:|
| C1 | Margin multiple (sell price ÷ landed cost) | 20 |
| C2 | Demand signal strength | 15 |
| C3 | Creative potential / demo-ability | 13 |
| C4 | Competitive saturation *(inverse)* | 12 |
| C5 | Legal, IP & platform risk *(inverse — residual, after gates)* | 10 |
| C6 | Fulfillment depth | 8 |
| C7 | Shipping & handling profile | 8 |
| C8 | Price band fit | 7 |
| C9 | AOV expansion potential | 4 |
| C10 | Seasonality *(inverse)* | 3 |
| | **Total** | **100** |

**Weighted score** = Σ(score × weight) ÷ 100 → a number from 1.00 to 5.00.

### Why these weights

Margin is 20 because it is the only criterion that sets the ceiling on everything
downstream — break-even ROAS is a direct function of it, and no amount of good creative
fixes a 2x product. Demand (15) and creative potential (13) are next because on paid
social the creative *is* the product-market fit test. Saturation is 12 rather than higher
because a crowded market proves demand exists; it only kills you if the incumbents have
locked up the angles *and* the supply. Seasonality is only 3 — it is a gate-like concern
that we mostly handle by rejecting obvious Q4-only products at intake.

---

### Scoring anchors

Score only 1, 3, or 5 unless you have a specific reason to use 2 or 4. Forcing the
anchors prevents everything drifting to a mushy 3.5.

#### C1 — Margin multiple (weight 20)
Sell price ÷ landed cost (landed = unit + inbound freight + duty/tariff + per-parcel fees).

| Score | Anchor |
|---|---|
| 5 | ≥ 5.0x |
| 4 | 4.0–4.9x |
| 3 | 3.5–3.9x |
| 2 | 3.0–3.4x |
| 1 | < 3.0x → **gate failure G8, reject** |

#### C2 — Demand signal strength (weight 15)
Evidence that people already want this, from the sources in PLAN.md Phase 1.

| Score | Anchor |
|---|---|
| 5 | Multiple independent signals: ≥3 TikTok organic videos >1M views in last 90 days, AND a Google Trends line that is flat-or-rising over 24 months, AND ≥1,000/mo US search volume on a buying-intent keyword. |
| 3 | One strong signal plus one weak. E.g. viral TikTok traction but thin search volume (normal for genuinely new products — not disqualifying). |
| 1 | Only signal is that a dropshipping YouTube video or product-research tool told you it was "winning." That is not a signal. |

#### C3 — Creative potential / demo-ability (weight 13)
Can it be *shown* solving a problem in the first 3 seconds of a vertical video?

| Score | Anchor |
|---|---|
| 5 | Visual before/after or a satisfying mechanical demo. The product's value is legible with sound off. ≥5 distinct ad angles brainstormable. |
| 3 | Demo-able but needs explanation; value is real but not instantly visual. |
| 1 | Nothing to show. Value is aesthetic-only or purely claimed. These die on paid social regardless of price. |

#### C4 — Competitive saturation, inverse (weight 12)

| Score | Anchor |
|---|---|
| 5 | <5 active advertisers in Meta Ad Library on the core angle; no established brand owns the term. |
| 3 | 5–20 advertisers, but the dominant creative is weak/dated, or an entire positioning angle is unclaimed. |
| 1 | >20 advertisers, several running the same creative >6 months (proven, funded, and iterating faster than we can), or a real brand owns the category. |

#### C5 — Legal / IP / platform risk, inverse (weight 10)
Residual risk *after* the hard gates. Gates catch the obvious; this catches the rest.

| Score | Anchor |
|---|---|
| 5 | Generic commodity form factor, no claims needed beyond descriptive, no lookalike risk. |
| 3 | Requires a performance claim we can substantiate with documentation we actually possess. |
| 1 | Requires a health/efficacy/outcome claim, or the winning angle is one we cannot make legally. **Treat as reject even though it scores.** |

#### C6 — Fulfillment depth (weight 8)

| Score | Anchor |
|---|---|
| 5 | ≥3 suppliers with the same SKU, ≥1 with US warehouse stock, all with verifiable order history and >95% positive. |
| 3 | 2 suppliers, China-only dispatch, credible history. |
| 1 | Single supplier, no track record, or a listing that looks like a reseller of a reseller. Single-supplier = single point of business failure. |

#### C7 — Shipping & handling profile (weight 8)

| Score | Anchor |
|---|---|
| 5 | <8 oz, fits a padded mailer, non-fragile, no batteries/liquids, no assembly. |
| 3 | 8 oz–1.5 lb, small box, mildly fragile or needs protective packing. |
| 1 | >1.5 lb or bulky (dimensional weight bites), fragile, liquid, or hazmat-adjacent. |

#### C8 — Price band fit (weight 7)
Target $25–$70. Below $25, CPA math almost never closes on cold paid social. Above ~$70,
impulse purchase breaks down and you need consideration-cycle marketing we're not set up for.

| Score | Anchor |
|---|---|
| 5 | $35–$60 |
| 4 | $25–$34 or $61–$70 |
| 2 | $70–$95 (needs a strong offer/guarantee to work) |
| 1 | <$25 or >$95 |

#### C9 — AOV expansion potential (weight 4)

| Score | Anchor |
|---|---|
| 5 | Natural multi-pack, consumable refill, or an obvious complementary accessory to bundle. |
| 3 | Bundle is plausible but slightly forced. |
| 1 | Strictly one-per-household, no accessory, no repeat purchase. |

#### C10 — Seasonality, inverse (weight 3)

| Score | Anchor |
|---|---|
| 5 | Flat 12-month Google Trends; demand is not weather-, holiday-, or event-linked. |
| 3 | Mild seasonal skew (±30% peak to trough). |
| 1 | Sharp single-season or holiday-only peak. |

---

## Decision thresholds

| Weighted score | Decision |
|---|---|
| **≥ 4.00** | Advance to Phase 2 — order samples immediately. |
| **3.50 – 3.99** | Shortlist. Advance only if it is top-2 and nothing scores ≥4.00. |
| **3.00 – 3.49** | Hold. Re-examine only if the top of the list dies at sample QC. |
| **< 3.00** | Reject. Do not revisit. |

Additional rule: **no candidate advances on score alone if C1 < 3 or C2 < 3.** A product
that is cheap-to-acquire but thin-margin, or high-margin but unwanted, is a trap that a
weighted average will happily hide.

Target: score **at least 20 candidates** before advancing any. The rubric only produces a
good decision if it has a real distribution to rank across. Scoring three products and
picking the best of three is just picking.

---

## Blank template

```markdown
### [Candidate name]

- **Date scored:** YYYY-MM-DD
- **Source of idea:** (TikTok Creative Center / Ad Library / Amazon M&S / forum / other)
- **Supplier links:** (2–3)
- **Proposed sell price:** $
- **Landed cost:** $  ← from the worksheet in docs/unit-economics.md, incl. duty/tariff
- **Margin multiple:** __x

**Hard gates**

| G1 ingest | G2 battery | G3 kids | G4 patent | G5 regulated | G6 ad-platform | G7 fragile/size | G8 margin ≥3x |
|---|---|---|---|---|---|---|---|
| PASS/FAIL | | | | | | | |

*(If any FAIL: stop here. Record the reason and move on.)*

**Weighted score**

| # | Criterion | Wt | Score (1–5) | Weighted | Evidence / note |
|---|-----------|---:|---:|---:|---|
| C1 | Margin multiple | 20 | | | |
| C2 | Demand signal | 15 | | | |
| C3 | Creative potential | 13 | | | |
| C4 | Saturation (inv) | 12 | | | |
| C5 | Legal/platform risk (inv) | 10 | | | |
| C6 | Fulfillment depth | 8 | | | |
| C7 | Shipping profile | 8 | | | |
| C8 | Price band fit | 7 | | | |
| C9 | AOV expansion | 4 | | | |
| C10 | Seasonality (inv) | 3 | | | |
| | **TOTAL** | 100 | | **_.__ / 5.00** | |

**Top 3 ad angles:**
1.
2.
3.

**Biggest unknown:**

**Decision:** ADVANCE / SHORTLIST / HOLD / REJECT
```

---

## Worked example (illustrative only — not a real recommendation)

Shown so the anchors are unambiguous. The numbers are invented to demonstrate arithmetic,
**not** a product endorsement.

### Example: magnetic under-desk cable tray

- Sell price $44 · landed cost $9.80 · **4.5x**

| # | Criterion | Wt | Score | Weighted | Note |
|---|-----------|---:|---:|---:|---|
| C1 | Margin multiple | 20 | 4 | 0.80 | 4.5x |
| C2 | Demand signal | 15 | 3 | 0.45 | Strong desk-setup search volume, no viral video |
| C3 | Creative potential | 13 | 5 | 0.65 | Messy→clean before/after, sound-off legible |
| C4 | Saturation (inv) | 12 | 3 | 0.36 | ~12 advertisers, all using flat product-on-white |
| C5 | Legal risk (inv) | 10 | 5 | 0.50 | Commodity, descriptive claims only |
| C6 | Fulfillment depth | 8 | 3 | 0.24 | Two suppliers, China dispatch only |
| C7 | Shipping profile | 8 | 5 | 0.40 | 6 oz, flat, unbreakable |
| C8 | Price band fit | 7 | 5 | 0.35 | $44 |
| C9 | AOV expansion | 4 | 5 | 0.20 | 2-pack + cable clip bundle |
| C10 | Seasonality (inv) | 3 | 5 | 0.15 | Flat |
| | **TOTAL** | 100 | | **4.10** | **ADVANCE** |

Arithmetic check: 0.80+0.45+0.65+0.36+0.50+0.24+0.40+0.35+0.20+0.15 = **4.10** → ≥4.00,
and both C1 and C2 are ≥3 → advances to sample ordering.
