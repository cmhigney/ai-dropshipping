# Unit Economics

The purpose of this document is to make one number defensible: **the ROAS we must hit to
not lose money.** Everything else here exists to derive it.

Most dropshipping plans pick a target ROAS because it sounds achievable — "we'll aim for
3x." That is backwards. Target ROAS is an *output* of the margin structure, not an input.
A 68% contribution margin breaks even at 1.47x. A 40% contribution margin breaks even at
2.50x. Same ad account, same creative, completely different business.

> **Source discipline.** Every number below is tagged. **[CONFIRMED]** = read from a
> primary source, with URL and date. **[BENCHMARK]** = a real published study with a
> disclosed sample. **[ASSUMPTION]** = our estimate, must be replaced with our own data
> once we have it. Do not let an assumption graduate to a fact just because it has been
> sitting in the document for a month.

---

## 1. Definitions

| Symbol | Meaning |
|---|---|
| `R` | Revenue per order (AOV), before any deduction |
| `C` | **Landed** cost of goods per order — see the worksheet in §2 |
| `p` | Payment processing percentage rate |
| `f` | Payment processing fixed fee per transaction |
| `r` | Refund rate (fraction of orders refunded) |
| `b` | Chargeback rate (fraction of orders disputed) |
| `s` | Per-order software/support cost |
| `CM` | Contribution margin per order, **in dollars, before ad spend** |
| `cm` | Contribution margin **ratio** = `CM / R` |
| `F` | Fixed monthly costs (platform, apps, subscriptions) |

---

## 2. Landed cost worksheet

`C` is **not** the supplier's sticker price. Fill this in per product, per fulfilment
route, before the product is allowed through gate G8 in the
[scorecard](../research/product-scorecard.md).

| Line | Direct parcel (China → customer) | Bulk import → US 3PL |
|---|---|---|
| Supplier unit price | | (lower — MOQ pricing) |
| Inbound freight per unit | included in parcel rate | ocean/air ÷ units |
| **Customs duty per unit** | see PLAN.md Phase 2 | see PLAN.md Phase 2 |
| Customs brokerage / disbursement fee | per parcel | amortised per unit |
| Outbound shipping to customer | included | domestic postage |
| 3PL pick & pack | n/a | per order |
| Inventory storage per unit-month | n/a | |
| Packaging / insert | | |
| **= `C`, landed cost per unit** | | |

Two rules:

1. **Duty is a line item, not a rounding error.** The 2025–26 changes to US de minimis
   treatment moved duty from "ignore it" to "it may exceed the supplier's unit price."
   PLAN.md Phase 2 carries the current rates and the sourcing decision that follows.
2. **Compute both columns for every serious candidate.** The direct-parcel and bulk-import
   routes have different break-evens, and which one wins is a function of volume. Deciding
   the route without doing both columns is guessing.

---

## 3. The core formulas

### 3.1 Contribution margin per order

Refunds and chargebacks are modelled as *expected* costs across all gross orders, because
that is how they actually hit the P&L.

```
CM = R·(1 − r)                 ← revenue we keep after refunds
     − C                        ← goods, incurred on every order incl. refunded ones
     − (p·R + f)                ← processing, incurred on every order
     − b·(R + K)                ← chargebacks: lost revenue + per-dispute fee K
     − s                        ← support / apps / per-order software
```

Three modelling choices worth stating explicitly, because getting them wrong flatters the
model:

- **COGS is subtracted on gross orders, not net.** When a customer refunds a $12 item
  shipped from overseas, we do not get the item back. The goods are gone. Deducting COGS
  only on kept orders overstates margin.
- **Processing fees are subtracted on gross orders.** Refunding an order does not
  automatically return the processing fee. *[ASSUMPTION — verify against Shopify Payments'
  current refund-fee behaviour before relying on it; if fees are returned, this is
  conservative by ~`r·(p·R+f)`.]*
- **Chargebacks cost more than the order.** You lose the revenue, the goods, *and* pay a
  dispute fee. They also feed the VAMP ratio in §6, which is the part that can end the
  business.

### 3.2 Contribution margin ratio

```
cm = CM / R
```

### 3.3 Break-even ROAS — the number this document exists for

At break-even, all contribution margin is spent on ads:

```
                    R          1
Break-even ROAS = ──────  =  ────
                    CM         cm
```

**Break-even ROAS is simply the reciprocal of the contribution margin ratio.** Nothing
else. If someone quotes you a target ROAS without telling you the margin ratio it came
from, they made it up.

### 3.4 Target ROAS for a desired net margin

To keep `m` (net margin as a fraction of revenue, before fixed costs):

```
                    1
Target ROAS = ────────────
                 cm − m
```

Note the shape of this: as `m` approaches `cm`, the required ROAS goes to infinity. A
business with a 40% contribution margin cannot target a 35% net margin at any achievable
ROAS. The formula tells you when your goal is arithmetically impossible.

### 3.5 CAC ceiling

```
Max CPA (break-even)  = CM
Target CPA            = CM − m·R
```

This is the more useful operational number. Media buyers act on a dollar CPA, not a ratio.

### 3.6 Blended MER, including fixed costs

ROAS measures a campaign. **MER** (Marketing Efficiency Ratio = total revenue ÷ total ad
spend) measures the business, and it is the one that determines whether we are actually
profitable. Including fixed costs `F` over a period with revenue `V`:

```
                        V
Break-even MER = ───────────────
                   V·cm − F
```

Break-even MER is always **worse** than break-even ROAS, and the gap closes as revenue
grows. This is why an early store can hit "profitable ROAS" every day and still lose money
every month.

---

## 4. Worked example — base case

**All inputs below are [ASSUMPTION] except where tagged.** This is the model, not a
forecast. Replace each input with measured data as it arrives.

| Input | Value | Basis |
|---|---|---|
| `R` — AOV | $49.00 | [ASSUMPTION] mid-point of our $25–70 target band |
| `C` — landed cost | $11.40 | [ASSUMPTION] from §2 worksheet; must include duty |
| `p` — processing % | 2.9% | **[CONFIRMED]** Shopify Payments US online card rate, Basic plan — shopify.com/pricing, fetched 2026-08-20 |
| `f` — processing fixed | $0.30 | **[CONFIRMED]** same source |
| `r` — refund rate | 5.0% | [ASSUMPTION] |
| `b` — chargeback rate | 0.5% | [ASSUMPTION] |
| `K` — chargeback fee | $15.00 | [ASSUMPTION — verify Shopify Payments' current dispute fee] |
| `s` — per-order software | $0.40 | [ASSUMPTION] |

### Step by step

```
Revenue kept          R·(1−r)      = 49.00 × 0.95        =  46.55
Goods                 C            =                        −11.40
Processing            p·R + f      = (0.029×49) + 0.30   =   −1.72
Chargebacks           b·(R+K)      = 0.005 × (49+15)     =   −0.32
Software/support      s            =                        −0.40
                                                            ───────
Contribution margin   CM                                  =  32.71
```

```
cm              = 32.71 / 49.00           = 0.6676  →  66.8%
Break-even ROAS = 1 / 0.6676              = 1.50x
Max CPA         = CM                      = $32.71
```

**At a 20% net margin target (`m` = 0.20):**

```
Target ROAS = 1 / (0.6676 − 0.20) = 1 / 0.4676 = 2.14x
Target CPA  = 32.71 − (0.20 × 49) = 32.71 − 9.80 = $22.91
```

So: **break even at 1.50x, make real money at 2.14x, and the media buyer's job is to
acquire a customer for under $22.91.**

### Sensitivity — why the margin gate is set at 3x landed cost

Holding everything else constant and varying only landed cost:

| Landed cost `C` | Multiple | `cm` | Break-even ROAS | Max CPA | Target CPA @20% |
|---:|---:|---:|---:|---:|---:|
| $7.00 | 7.0x | 75.7% | 1.32x | $37.11 | $27.31 |
| $9.80 | 5.0x | 70.0% | 1.43x | $34.31 | $24.51 |
| $11.40 | 4.3x | 66.8% | 1.50x | $32.71 | $22.91 |
| $12.25 | 4.0x | 65.0% | 1.54x | $31.86 | $22.06 |
| $16.33 | 3.0x | 56.7% | 1.76x | $27.78 | $17.98 |
| $19.60 | 2.5x | 50.0% | 2.00x | $24.51 | $14.71 |
| $24.50 | 2.0x | 40.0% | 2.50x | $19.61 | $9.81 |

Read the last two rows. At a 2.0x product, the media buyer must acquire a customer for
**$9.81** to make a 20% margin. Against a market where the median DTC first-purchase CPA
runs $17–39 (§5), that is not a hard target — it is an impossible one. **This is the
entire justification for the 3x hard gate**: below 3x, no realistic CPA produces a
business.

### Upside case — the AOV lever

The fastest way to fix break-even ROAS is not cheaper ads, it is a higher AOV. Same
product, with a 2-for-1 bundle attaching on 25% of orders at +$18 revenue / +$8.60 cost:

```
R = 49.00 + (0.25 × 18.00)  = $53.50
C = 11.40 + (0.25 × 8.60)   = $13.55

CM = (53.50 × 0.95) − 13.55 − ((0.029×53.50)+0.30) − (0.005×(53.50+15)) − 0.40
   = 50.83 − 13.55 − 1.85 − 0.34 − 0.40
   = $34.68

cm = 34.68 / 53.50 = 64.8%   →  Break-even ROAS 1.54x   →  Max CPA $34.68
```

Note carefully what happened: the contribution *ratio* got slightly **worse** (66.8% →
64.8%), so break-even ROAS rose from 1.50x to 1.54x — but the **CAC ceiling rose from
$32.71 to $34.68**. That is the trade that matters. We can pay ~$2 more per customer,
which in a CPA-constrained auction is the difference between a campaign that scales and
one that does not.

**Lesson: optimise for the CAC ceiling in dollars, not for the ROAS ratio.** A bundle that
lowers your margin percentage but raises your dollar contribution is a good trade, and a
ROAS-only dashboard will tell you it is a bad one.

---

## 5. Benchmarks to calibrate against

Use these as **priors to sanity-check our targets**, not as forecasts. Where two sources
disagree, that disagreement is itself information.

### Paid social — e-commerce

| Metric | Meta | TikTok | Source |
|---|---|---|---|
| CPM (median) | **$15.06** (+13.2% YoY) | **$4.08** (−24.5% YoY) | [BENCHMARK] Triple Whale, 40,000+ / 5,900+ ecommerce brands, Aug 2025–Jul 2026 |
| CTR | 2.39% *(all-clicks)* | 0.61% | same |
| CVR | 1.53% | 1.56% | same |
| **CPA** | **$38.99** | **$17.07** | same |
| ROAS | 1.88 | 1.51 | same |
| AOV | $73.36 | $50.32 | same |
| **Link** CTR | 1.59–1.77% | 0.95–0.97% | [BENCHMARK] Gupta Media CPM Tracker, Sep/Oct 2025 vintage |
| Cost per link click | $0.37–$0.53 | $0.49–$0.54 | same |

Two warnings on the table above:

- **Meta's 2.39% CTR is almost certainly all-clicks, not link clicks.** Triple Whale does
  not define it. Gupta Media, which does define it, measures link CTR at 1.59–1.77%. When
  we set a creative kill threshold in PLAN.md Phase 5, use the **link** CTR figure. Killing
  ads against an all-clicks benchmark would cut winners.
- **TikTok's numbers are contested.** A second source with a disclosed sample (AdLiftr,
  3,127 campaigns / $18.7M spend, Feb–May 2026) reports conversion-objective CPM at
  **$16.20** and CPA at **$15.80** — a 4x gap on CPM against Triple Whale's $4.08, likely
  an objective-mix difference (Triple Whale's blends cheap reach inventory). **Plan against
  $16.20 CPM for conversion campaigns.** The optimistic number will not be what we buy.

Also from AdLiftr, and directly actionable: **Spark Ads posted 1.62% CTR vs 0.84% for
standard in-feed, with 28% lower CPA.** That is a strong argument for running creative
through a real creator handle rather than as a plain in-feed ad.

### Reality check on platform-reported ROAS

[BENCHMARK] Common Thread Collective Q1 2026 Channel Mix (299 DTC brands, $231M spend,
Jan–Mar 2026) compared platform-reported to **incrementality-tested** ROAS:

| Channel | Platform-reported | Incremental | Gap |
|---|---:|---:|---|
| Meta prospecting | 1.83x | **2.07x** | Meta *under*-reports |
| Meta retargeting | 5.88x | **3.53x** | Meta *over*-reports by 0.60x |
| TikTok | 4.50x | **3.60x** | over-reports by 0.80x |

The retargeting gap is the one to internalise: **retargeting ROAS is systematically
inflated** because it claims credit for purchases that would have happened anyway. When we
report blended performance in Phase 6, MER is the honest number.

### Site conversion rate

[BENCHMARK, but dated] Littledata, n=2,800 Shopify stores — **median 1.4%**, top 20%
≥3.2%, top 10% ≥4.7%; **mobile 1.2% vs desktop 1.9%**. ⚠️ **The source page is dated 2023**
despite being widely recirculated as current. Cite it as 2023 data.

The mobile/desktop split is the operationally useful part: paid social traffic is
overwhelmingly mobile, and mobile converts at roughly **63% of desktop**. Any CVR
assumption we make for cold paid-social traffic should start from the mobile figure, not
the blended one.

> **Known gap — the biggest one in this document.** We could not find a defensible,
> disclosed-sample figure for **cold paid-social traffic CVR** specifically. It is the
> single most load-bearing input in the whole model. Our planning assumption is **1.0–1.5%**
> [ASSUMPTION], reasoned from the 1.2% mobile median discounted for cold traffic. Replace it
> with our own measured number as soon as we have 100+ sessions, and re-run every table in
> this document when we do.

---

## 6. Constraints that override the math

Two thresholds can end the business regardless of how good the ROAS is.

### 6.1 Dispute ratios — Visa VAMP

**[CONFIRMED]** Merchant Risk Council, published 2026-04-01:

- **Merchant "Excessive" threshold: 1.5%**, effective **2026-04-01** — reduced from 2.2%.
  Any source still citing 2.2% for a US merchant is stale.
- Ratio = **(TC40 fraud reports + TC15 disputes) ÷ total settled transactions**,
  card-not-present only.
- **$8 enforcement fee** per fraudulent or disputed transaction.
- First violation in a rolling 12 months gets a **3-month grace period**.
- [MODERATE] A floor of ~**1,500 combined monthly events** must be exceeded before
  enforcement applies — which protects a low-volume new store. **The risk arrives at
  scale**, precisely when we have the most to lose.

Note the numerator includes fraud reports *plus all disputes*. A model with long overseas
delivery times generates item-not-received disputes, so this ratio climbs faster for us
than for a domestic retailer.

[MODERATE] **Mastercard ECM**: 100–299 chargebacks *and* 1.5–2.99% ratio. **HECM**: ≥300
*and* ≥3%. Exit requires three consecutive months below threshold. A new
**Scam Merchant Monitoring Program (SMMP)** took effect 2026-07-24; its thresholds are
**[NOT VERIFIED]** and should be run down before we scale.

**Our internal ceiling: 0.6% disputes.** Set deliberately below every network threshold,
because by the time you are at 1.5% you are already in a program.

### 6.2 Payment processor reserves — the cash-flow killer

**[CONFIRMED]** help.shopify.com/manual/payments/shopify-payments/reserves, fetched
2026-08-20. Shopify can apply either a **fixed-amount reserve** (their example: $1,000 held
120 days) or a **percentage reserve** (their example: 10% held 120 days).

Documented triggers, verbatim-adjacent: extended billing cycles, elevated chargeback
activity, increased refund rates, **industries with long delivery timelines**, and
significant volume surges.

**Read that fourth trigger again.** Long delivery timelines are named directly in
Shopify's own risk criteria. That is not a generic warning — it is a description of the
dropshipping model. This is the strongest single argument in this repo for solving
fulfilment speed (PLAN.md Phase 2) *before* spending on ads.

[UNCERTAIN / anecdotal] Merchant reports describe 20% reserves for up to 120 days on
dropshipping-flagged accounts, and Stripe rolling reserves of 5–15% for 90–180 days.
Treat as assumptions, but plan cash as if a reserve **will** happen.

**Planning implication:** model working capital assuming **20% of revenue is withheld for
120 days** starting the day volume becomes interesting. If that scenario makes us
insolvent, we are undercapitalised — regardless of ROAS.

---

## 7. Cash flow — why profitable businesses die

Ad spend leads revenue. Revenue lags into a payout schedule. Goods must be paid for
up front. The gap is real money.

```
Day 0    Pay supplier / pay for ads
Day 0-2  Customer pays          → held by processor
Day 2-7  First payout           → longer for new accounts [ASSUMPTION]
Day 0-N  Reserve withheld       → up to 120 days [CONFIRMED as a documented mechanism]
```

**Peak cash requirement ≈ (daily ad spend + daily COGS) × days-to-payout, plus the reserve
balance.** At $200/day spend with a 7-day payout and a 20% reserve, that is roughly
$1,400–2,000 of permanently deployed working capital before any growth. Scaling ad spend
scales this requirement linearly — **growth consumes cash even when every order is
profitable.**

---

## 8. Fixed costs

| Item | Monthly | Basis |
|---|---:|---|
| Shopify Basic | **$39** ($29 if annual) | **[CONFIRMED]** shopify.com/pricing 2026-08-20 |
| Domain | ~$1.25 | [ASSUMPTION] |
| Apps (reviews, upsell, analytics) | $30–80 | [ASSUMPTION] |
| AI creative tooling | $40–150 | [ASSUMPTION] — see PLAN.md Phase 4 |
| **Total `F`** | **~$110–270** | |

[CONFIRMED] Shopify's current promo is "3 days free, then $1/month for 3 months," which
covers the entire test window. Also confirmed: leaving Shopify Payments for a third-party
gateway costs **2% per transaction on Basic** — that penalty is larger than the difference
between plan tiers, and it is what makes getting dropped by Shopify Payments so expensive.

At `F` = $200/mo and `cm` = 66.8%, fixed costs alone require **$300/mo in revenue** before
the first dollar of ad spend is justified. Trivial at scale; not trivial in month one.

---

## 9. What to re-run, and when

This document is wrong the moment we have real data. Re-derive every table when:

- [ ] First 100 orders land → replace `r`, `b`, AOV, and CVR with measured values
- [ ] Landed cost changes (supplier renegotiation, duty change, route switch China→3PL)
- [ ] We add a bundle or upsell → recompute the CAC ceiling, not just the ratio
- [ ] Any processor reserve is applied → rebuild §7 with actual payout timing
- [ ] Monthly, regardless — recompute break-even **MER** including actual fixed costs

**The one-line summary to carry around:** at our base case, we break even at **1.50x ROAS**
and must acquire customers below **$22.91** to make a 20% margin. Both numbers move the
moment landed cost moves, which is why duty is a line item and not an afterthought.
