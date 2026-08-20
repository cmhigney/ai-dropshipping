# Operating Plan — AI Dropshipping

**Version 1.0 · Written 2026-08-20 · Owner: cmhigney**

This plan is deliberately front-loaded with the two things that kill dropshipping
businesses before marketing ever matters: **the landed-cost math and the fulfilment
route.** Research is Phase 1 and fulfilment is Phase 2 because a decision made wrong in
either one cannot be rescued by anything in Phases 3–6.

## How to read this

- **Owner** — `Op` = operator (you: decisions, money, anything needing a legal identity).
  `AI` = Claude (research, scoring, drafting, analysis). `Ext` = external (customs broker,
  UGC creator, CPA).
- **Gates** are hard. Each phase ends in a written go/no-go with a pre-committed criterion.
  If we miss the criterion, we do not lower it.
- **Tags** — **[CONFIRMED]** = primary source, cited inline. **[BENCHMARK]** = published
  study with disclosed sample. **[ASSUMPTION]** = our guess, must be replaced by measured
  data. Nothing untagged is a fact.

---

## The finding that reshapes this plan

Before anything else, the single most important fact established during planning:

> **US de minimis is gone, permanently, for every country — and the per-parcel customs
> overhead now exceeds the product cost on a typical dropshipping item.**

- De minimis was eliminated for China/HK effective **2025-05-02** (EO 14256), then
  suspended for **all countries** effective **2025-08-29** (EO 14324). **[CONFIRMED]**
  — [whitehouse.gov](https://www.whitehouse.gov/presidential-actions/2025/07/suspending-duty-free-de-minimis-treatment-for-all-countries/)
- When the Supreme Court struck down IEEPA tariff authority on **2026-02-20**, the
  suspension **survived** — CBP had re-grounded it in its own regulations via two interim
  final rules published **2026-06-24**. **[CONFIRMED]** —
  [Federal Register 2026-12670](https://www.federalregister.gov/documents/2026/06/24/2026-12670/).
  **Do not assume the SCOTUS ruling restored de minimis. It did not.**
- The OBBBA statutorily repeals de minimis on **2027-07-01**, putting it beyond reversal by
  a future executive order. [UNCERTAIN — secondary source]
- Carrier disbursement fees are now **greater of $17.50 or 2.5%** (FedEx, eff. 2026-07-20)
  and **2% with a $17.00 minimum** (UPS). [UNCERTAIN — three consistent secondary sources,
  not carrier tariff PDFs]

**On a $12 parcel, the percentage never binds — you pay the ~$17.50 floor every time.**
That fee alone is ~145% of the declared value, before duty. Add China Section 301 at an
aggregate **37.5%** (25% legacy + a new 12.5% forced-labor action effective 2026-07-24)
plus MFN, and a $12 item lands at **$35–40**. **[CONFIRMED on rates; arithmetic derived]**

**Consequence: the classic AliExpress-parcel-direct-to-customer model is dead for
US-bound, China-sourced goods.** This plan does not attempt to revive it. Phase 2 is
therefore not an open question about which supplier is nicest — it is a forced move to
US-domestic stock, and the only real decision is how we finance getting there.

---

## Phase overview

| Phase | Window | Gate | Gate date |
|---|---|---|---|
| 1 · Product research | W1–W2 · Aug 24 – Sep 6 | **A** — 20+ scored, one ≥4.00 | Fri **Sep 4** |
| 2 · Fulfilment | W3–W5 · Sep 7 – Sep 27 | **B** — sample QC passed, route costed | Fri **Sep 25** |
| 3 · Store build | W4–W6 · Sep 14 – Oct 4 | **C** — store + tracking verified live | Fri **Oct 9** |
| 4 · AI creative | W6–W7 · Sep 28 – Oct 11 | **C** (shared) — 12+ assets, compliance signed off | Fri **Oct 9** |
| 5 · Paid acquisition | W7–W10 · Oct 5 – Nov 1 | **D** — CPA below ceiling at $1.5k spend | Mon **Nov 2** |
| 6 · Ops & finance | Continuous | **E** — monthly MER review | Monthly |

**Total capital to Gate D: $3,000–4,500.** [ASSUMPTION] Breakdown in Phase 6.

---

# PHASE 1 — Product Research

**W1–W2 · Aug 24 – Sep 6 · Owner: AI (research & scoring), Op (final selection)**

The deepest phase, because it is the cheapest place to be right and the most expensive
place to be wrong. Output is a ranked list of 20+ candidates in
[research/candidates.md](research/candidates.md), scored with
[research/product-scorecard.md](research/product-scorecard.md).

## 1.1 What a winnable product looks like

### Hard gates (any failure = reject, no scoring)

Full definitions in the [scorecard](research/product-scorecard.md#stage-1--hard-gates-any-fail--reject-do-not-score).
Summary: no ingestibles/topicals, no lithium batteries or powered electronics, no
kids'/infant products, no patent or trademark exposure, no regulated categories, nothing
on platform prohibited lists, nothing fragile or oversized, and **nothing below 3x landed
cost**.

These are not preferences. Each one maps to a specific, uninsurable failure mode:
supplements to FDA and ad-platform bans, batteries to hazmat and return rates, kids'
products to CPSIA testing liability, patents to a takedown that vaporises the store
overnight.

### Margin floor — 3x minimum, 4x+ target, on **true landed cost**

Landed cost now means unit + freight + **duty** + brokerage + fulfilment. The
[unit economics sensitivity table](docs/unit-economics.md#sensitivity--why-the-margin-gate-is-set-at-3x-landed-cost)
shows why 3x is the floor and not a round number: at 2.0x, hitting a 20% net margin
requires a **$9.81 CPA**, against a market where median DTC first-purchase CPA runs
**$17–39** [BENCHMARK]. That is not ambitious, it is arithmetically impossible.

### Price band — target $45–70, not $25–70

The $25–70 band is the right outer envelope, but the evidence says **concentrate in the
upper half**, and the reason is channel-specific. Holding our 4.3x margin structure
constant:

| Channel | Median CPA [BENCHMARK] | AOV to break even | AOV for 20% net margin |
|---|---:|---:|---:|
| **TikTok** | $17.07 | **$26** | **$37** |
| **Meta** | $38.99 | **$58** | **$82** |

*Sources: Triple Whale, 40,000+ (Meta) / 5,900+ (TikTok) ecommerce brands, Aug 2025–Jul 2026.
AOV figures derived from our own margin model.*

Read that table carefully — it is the most actionable thing in Phase 1:

- **At a $49 AOV, a median-performing Meta campaign loses money.** Meta's median CPA
  ($38.99) is above our break-even CAC ceiling ($32.71) at that price. We would need to be
  meaningfully better than the median advertiser just to break even.
- **The same $49 product is comfortably profitable at TikTok's median CPA.**
- Therefore: **price at $45–70 and lead with TikTok.** Meta becomes viable once AOV clears
  ~$58 (break-even) and genuinely good above ~$82. Sub-$35 products only work on TikTok and
  only with a bundle that lifts AOV.

### Other criteria

- **Lightweight / non-fragile** — under 1 lb, fits a padded mailer. Directly reduces both
  3PL outbound cost and breakage refunds.
- **Non-seasonal** — flat 12-month Google Trends. We cannot learn a product's economics in
  a window that closes.
- **Not saturated** — but note that *some* competition is a positive signal. The kill
  condition is incumbents running the *same creative* for 6+ months, which means they are
  funded, iterating, and have locked the winning angle.
- **Demo-able in 3 seconds, sound off.** On paid social, creative *is* product-market fit.
  A product with nothing to show cannot be tested cheaply.

## 1.2 Where to hunt for demand signals

Six sources, each with a different bias. Use at least four per candidate — a signal that
appears in only one source is usually an artifact of that source.

| Source | What it actually tells you | Its bias |
|---|---|---|
| **TikTok Creative Center** (Top Ads, free) | What creative is winning *right now*; hooks, formats, hashtag velocity | Shows what's already scaling — you're seeing the peak, not the entry point |
| **Meta Ad Library** | **Ad longevity** — the single best proxy for profitability | Only shows active ads; survivorship |
| **Amazon Movers & Shakers** | Real purchase behaviour, not engagement | Amazon demand ≠ paid-social demand; different buyer intent |
| **Google Trends** (24-month view) | Seasonality and whether interest is structural or a spike | Blind to genuinely new products with no search history |
| **Reddit / niche forums** | Unmet complaints in the customer's own words — the richest source of ad angles | Vocal minority; not representative of purchase intent |
| **AliExpress / CJ order velocity** | Supply-side confirmation and supplier depth | Gameable; inflated by other dropshippers, not end consumers |

**The highest-signal move: Meta Ad Library, filtered by ad start date.** An ad running
unchanged for 3+ months is almost certainly profitable — nobody funds a losing creative
that long. Ad *longevity* beats ad *volume* as an indicator every time.

**The lowest-signal move: product-research SaaS tools and "winning product" YouTube
videos.** By the time a product is on one of those lists, its ad costs reflect everyone
else who saw the same list. The scorecard scores this a 1 on demand signal for exactly
this reason.

## 1.3 Validation before committing

Four checks, in ascending order of cost. Do them in order and stop at the first failure.

1. **Keyword volume** — is there buying-intent search volume, and is Google Trends flat or
   rising over 24 months? *Cost: free. Kill if:* trend is in structural decline.
2. **Competitor ad longevity** — Ad Library, filter by start date. *Kill if:* the top 3
   advertisers have run the same creative >6 months **and** own the obvious angles.
   *Positive signal if:* several advertisers are active but all creative is weak
   (product-on-white, no hook).
3. **Review mining** — pull 200+ reviews of the incumbent product from Amazon/AliExpress
   and cluster the 2- and 3-star complaints. **This is where ad angles come from.** The
   gap between what the product promises and what reviewers say it fails at *is* the
   positioning. *Owner: AI.* *Kill if:* complaints are about the product category itself
   rather than a fixable execution flaw.
4. **Small-budget concept test** — $50–100 on a single TikTok ad driving to a landing page
   with a real add-to-cart, before ordering inventory. Measures whether anyone actually
   wants it. *Kill if:* CTR is below the benchmark floor in Phase 5.

## 1.4 Scoring

Weighted rubric, 10 criteria, out of 5.00. Full anchors in the
[scorecard](research/product-scorecard.md#stage-2--weighted-scoring). Margin is weighted
highest (20) because it sets the ceiling on everything downstream.

**Score at least 20 candidates before advancing any.** Ranking needs a distribution.
Scoring three and picking the best of three is not research, it is picking.

### Deliverables

| # | Deliverable | Owner | Due |
|---|---|---|---|
| 1.1 | 40+ raw ideas in the intake table | AI | Aug 27 |
| 1.2 | Hard-gate pass over all ideas | AI | Aug 28 |
| 1.3 | 20+ fully scored candidates | AI | Sep 2 |
| 1.4 | Landed-cost worksheet for top 5, **both routes** | AI + Op | Sep 3 |
| 1.5 | Review-mining brief + 3 ad angles for top 3 | AI | Sep 3 |
| 1.6 | Final selection | **Op** | Sep 4 |

### 🚪 GATE A — Fri Sep 4

**Advance only if all four hold:**
- [ ] ≥20 candidates fully scored
- [ ] ≥1 candidate scores **≥4.00** with C1 (margin) and C2 (demand) both ≥3
- [ ] Winner's landed cost verified on **both** fulfilment routes, incl. duty
- [ ] Winner passes all 8 hard gates

**If no candidate clears 4.00:** do not advance the best of a weak field. Run a second
research sprint. The cost of another week is trivial against the cost of a full build on a
product that was never going to work.

---

# PHASE 2 — Fulfilment

**W3–W5 · Sep 7 – Sep 27 · Owner: Op (supplier relationships), AI (cost modelling)**

**This must be solved before a dollar goes to ads.** Not because it is tidy sequencing,
but because Shopify names *"industries with long delivery timelines"* directly in its own
documented criteria for imposing a payment reserve **[CONFIRMED]** —
[help.shopify.com](https://help.shopify.com/en/manual/payments/shopify-payments/reserves).
Slow fulfilment does not just produce refunds; it produces a **20% hold on revenue for 120
days**, which is an extinction-level cash event for an undercapitalised store.

## 2.1 The route decision — already made by the tariff math

| Route | Per-unit customs overhead | Delivery to US | Verdict |
|---|---|---|---|
| **AliExpress direct parcel** | ~$17.50 disbursement + ~41% duty, **per order** | 15–30 days | ❌ **Dead.** Overhead exceeds COGS |
| **CJ / Zendrop China warehouse** | Same per-parcel overhead | 7–15 business days | ❌ Same problem |
| **CJ / Zendrop US warehouse** | Already imported; none at our end | **2–5 days** | ✅ **Validation phase** |
| **Alibaba supplier → US 3PL** | One entry, amortised across shipment | **2–5 days** | ✅ **Scale phase** |

**The decision: test on US-warehouse stock, scale on bulk import.**

This is a two-step because of a genuine bootstrapping problem — you cannot justify a
500-unit import before validating demand, and you cannot validate demand on a fulfilment
route whose economics don't work. The resolution is to **accept worse unit economics
during validation** (US-warehouse dropship carries a supplier markup) and switch to bulk
import the moment the product proves out.

Model both in the [landed cost worksheet](docs/unit-economics.md#2-landed-cost-worksheet).
The validation-phase margin will be thinner; the gate is that it must **still clear 3x**,
or the product is too thin to survive the transition.

⚠️ **[CONFIRMED caveat]** Only a small fraction of CJ's catalogue is genuinely pre-stocked
in US warehouses. Unless you explicitly filter for "US Warehouse," your order ships from
China regardless of what the listing implies. **Verify US stock on the specific SKU, not
the supplier.**

## 2.2 Duty — get the HTS code right

| Layer | Rate | Note |
|---|---|---|
| MFN / column 1 | ~0–10% (avg 3.3%) | HTS-specific |
| Section 301 Lists 1–3 | **25%** | Most consumer goods |
| Section 301 List 4A | **7.5%** | Check your code |
| Forced-labor action (eff. 2026-07-24) | **+12.5%** | New; no expiration; stacks |
| **Aggregate, China, Lists 1–3** | **~41% incl. MFN** | **[CONFIRMED]** |
| **Aggregate, China, List 4A** | **~23% incl. MFN** | **[CONFIRMED]** |

**Determining our 10-digit HTS code is worth ~$2/unit on a $12 item** — the difference
between List 1–3 and List 4A. This is a Phase 2 deliverable, not an afterthought.

Note: Penn Wharton puts China's *realized* effective rate at **23.2%** trade-weighted
(2026-08-10), lower than headline because of exclusions and product mix. Our specific code
governs, not the average.

**Also dead:** the "China Post handles customs" model. Under the postal rule effective
2026-07-24, only the owner, purchaser, or a **licensed customs broker** may file, a customs
bond must be on file in ACE eBond *before* filing, and foreign postal operators are no
longer eligible filers. **[CONFIRMED]**

## 2.3 Sample ordering & QC

Order samples from **3 suppliers minimum**, shipped to the operator, before any commitment.
Never evaluate a supplier on listing photos — they are frequently stolen from the original
manufacturer.

**QC checklist** (score each sample, keep the sheet):

- [ ] Matches listing photos in material, colour, dimensions
- [ ] Functions as described — test the specific thing the ad will claim
- [ ] Survives a drop test from counter height in its shipping packaging
- [ ] Packaging is presentable, or can be replaced cheaply
- [ ] No supplier branding, no third-party logos, no foreign-language-only instructions
- [ ] No visible safety hazard (sharp edges, small detachable parts)
- [ ] Weight and packed dimensions measured — feeds 3PL and postage cost
- [ ] Photographed and filmed for creative *(kills two birds — see Phase 4)*
- [ ] Actual transit time recorded vs. supplier's promise

**Shipping-time target: under 10 days to US, door to door.** Both viable routes deliver
2–5 days, so this is achievable — treat >10 days as a route failure, not a supplier excuse.

## 2.4 Returns & refunds — who eats the loss

Policy: **30-day returns, customer pays return shipping, refund on receipt.** Defective or
not-as-described: we pay return shipping and refund in full.

The economics of returns for imported goods are asymmetric and worth stating plainly:
**we do not get the goods back in any useful sense.** A $12 item returned to a US 3PL costs
more to inspect and restock than it's worth; returned to China, more than it cost. So:

- **Under ~$20 landed:** authorise the refund, **do not request the item back.** Cheaper,
  and it converts an angry customer into a neutral one.
- **Over ~$20 landed:** request return to the 3PL, restock if saleable.
- **Never** make the customer fight for a refund. A refund costs us the contribution
  margin; a chargeback costs us the revenue, the goods, a **$15 fee**, *and* a tick toward
  the VAMP ratio that can end our ability to process payments at all.

Modelled at **5% refund rate** and **0.5% chargeback rate** [ASSUMPTION] — replace with
measured data after 100 orders.

## 2.5 Payment processor risk

The most underrated existential risk in this business. See
[unit-economics §6.2](docs/unit-economics.md#62-payment-processor-reserves--the-cash-flow-killer).

**[CONFIRMED]** Shopify may apply a fixed reserve (their example: $1,000 held 120 days) or
a percentage reserve (their example: 10% held 120 days). Documented triggers include
elevated chargebacks, increased refunds, volume surges, and **long delivery timelines**.

**[CONFIRMED]** Visa VAMP merchant "excessive" threshold dropped to **1.5%** effective
**2026-04-01** (from 2.2%), calculated as *(TC40 fraud reports + TC15 disputes) ÷ settled
CNP transactions*, with an **$8 fee** per disputed transaction. Any guidance still citing
2.2% is stale.

**Our mitigations:**
- **Internal dispute ceiling of 0.6%** — well below every network threshold, because by the
  time you hit 1.5% you are already enrolled in a program.
- Ship fast (Phase 2 route decision), send tracking immediately, respond to support within
  24h. Most disputes are item-not-received, which is a fulfilment problem wearing a
  payments costume.
- **Plan cash assuming a 20% reserve for 120 days will happen.** If that scenario makes us
  insolvent, we are undercapitalised regardless of ROAS.
- Do not leave Shopify Payments casually — the third-party gateway penalty is **2% per
  transaction on Basic** [CONFIRMED], larger than the gap between plan tiers.

### Deliverables

| # | Deliverable | Owner | Due |
|---|---|---|---|
| 2.1 | 3 suppliers contacted, US stock verified per SKU | Op | Sep 9 |
| 2.2 | Samples ordered from 3 suppliers | Op | Sep 10 |
| 2.3 | 10-digit HTS code determined | AI + Ext (broker) | Sep 11 |
| 2.4 | Customs broker quote for bulk-import entry | Op + Ext | Sep 16 |
| 2.5 | Landed cost, both routes, incl. duty & brokerage | AI | Sep 18 |
| 2.6 | Samples received, QC scored, transit time logged | Op | Sep 24 |
| 2.7 | Returns policy written | AI | Sep 24 |

### 🚪 GATE B — Fri Sep 25

- [ ] ≥1 sample passes every QC line item
- [ ] Verified transit time **under 10 days**
- [ ] Landed cost confirms **≥3x** on the validation route
- [ ] Backup supplier identified for the same SKU
- [ ] Broker quote obtained for the scale route

**If no sample passes QC:** return to the Gate A shortlist. Do not proceed with a product
you would not personally be happy to receive — every QC defect becomes a refund, a dispute,
and a step toward a payment reserve.

---

# PHASE 3 — Store Build

**W4–W6 · Sep 14 – Oct 4 · Owner: Op (build), AI (copy, config)**

## 3.1 Platform & structure

**Shopify Basic.** [CONFIRMED] $39/mo ($29 annual), 2.9% + 30¢ US online card rate.
Current promo: 3 days free then **$1/month for 3 months** — which covers the entire test
window. This is not a close call: Shopify's payment stack, app ecosystem, and checkout
conversion are worth more than the fee, and WooCommerce's "free" is paid in operator hours.

**Single-product store, niche-branded.** Build the store as if it were a real one-product
brand, with a name and domain that would still make sense if we added three more SKUs. A
general store cannot build a coherent offer and gets scrutinised harder by both payment
risk teams and customers; a bare single-product page with no brand context converts worse
and reads as disposable.

**Theme: Shopify Dawn**, customised. Free, fast, well-maintained. Paid themes mostly sell
sections we can build. **Page speed is a conversion input** — mobile converts at ~63% of
desktop [BENCHMARK, Littledata 2023] and paid-social traffic is overwhelmingly mobile, so
every optimisation should be judged on mobile first.

## 3.2 Offer construction

The offer, not the product, is what converts. Structure:

- **Anchor price + genuine discount.** Not a fake compare-at price — that is exactly the
  kind of deceptive pricing claim the FTC pursues, and Shopify will flag it.
- **Bundle for AOV.** From [unit economics](docs/unit-economics.md#upside-case--the-aov-lever):
  a 2-for-1 bundle attaching at 25% raises the **CAC ceiling from $32.71 to $34.68**, even
  though it slightly *lowers* the margin percentage. **Optimise for the dollar ceiling, not
  the ratio** — a ROAS-only dashboard will call this a bad trade and it is wrong.
- **Free shipping over a threshold** set just above single-unit price, to pull orders into
  the bundle.
- **Post-purchase upsell** (one click, no re-entered payment) — highest-leverage AOV lever
  because it cannot depress front-end conversion.

**Trust elements** — these matter more for an unknown brand than any copy tweak:
- Real reviews only. **Never** seeded, incentivised, or AI-generated — see Phase 4; this is
  a $53,088-per-violation issue, not a best practice.
- Visible contact route (email minimum), real returns policy, plain shipping timeline.
- **Do not fake urgency.** Countdown timers that reset are a deceptive-practice claim.

## 3.3 Analytics & tracking

Getting this wrong means Phase 5 optimises on noise. Set up **before** the first ad dollar.

| Tool | Config | Why |
|---|---|---|
| **GA4** | Enhanced ecommerce, purchase + add-to-cart events | Source of truth for on-site behaviour |
| **Meta pixel + CAPI** | Server-side via Shopify's native integration | Browser-only pixel loses 20–40% of events to ITP/blockers [ASSUMPTION] |
| **TikTok pixel + Events API** | Same — server-side | Same reason |
| **UTMs** | Rigid convention, below | Platform reporting will disagree with GA4; UTMs are the tiebreak |

**UTM convention** — lowercase, no spaces, never deviate:

```
utm_source   = tiktok | meta | google
utm_medium   = paid-social | paid-search | email | organic
utm_campaign = {product}-{objective}-{yyyymm}     e.g. cabletray-conv-202610
utm_content  = {creative-id}-{angle}-{hook}       e.g. c014-declutter-messydesk
utm_term     = {audience}                          e.g. broad | lal1 | int-desksetup
```

`utm_content` carries the creative ID, angle, and hook separately **on purpose** — it is
what makes "which *hook* is working, across all creatives" answerable in Phase 5. Without
it you can only see which individual ad won, which teaches you nothing transferable.

**Reality check on attribution:** platform-reported ROAS is systematically wrong, and
wrong in *different directions* by channel. [BENCHMARK — Common Thread Collective Q1 2026,
299 DTC brands, $231M spend]:

| Channel | Platform-reported | Incrementality-tested | Gap |
|---|---:|---:|---|
| Meta prospecting | 1.83x | 2.07x | Meta **under**-reports |
| Meta retargeting | 5.88x | 3.53x | **over**-reports by 0.60x |
| TikTok | 4.50x | 3.60x | **over**-reports by 0.80x |

Retargeting ROAS is inflated because it claims credit for purchases that would have
happened anyway. **Blended MER is the honest number** — Phase 6.

### Deliverables

| # | Deliverable | Owner | Due |
|---|---|---|---|
| 3.1 | Domain + Shopify Basic provisioned | Op | Sep 16 |
| 3.2 | Dawn theme customised, mobile-first | Op | Sep 23 |
| 3.3 | Product page copy from review-mining angles | AI | Sep 25 |
| 3.4 | Offer, bundle, post-purchase upsell live | Op | Sep 30 |
| 3.5 | GA4 + Meta CAPI + TikTok Events API verified | Op | Oct 2 |
| 3.6 | Test purchase end-to-end; confirm all events fire | Op | Oct 2 |
| 3.7 | Policies: shipping, returns, privacy, ToS | AI | Oct 2 |

---

# PHASE 4 — AI-Powered Creative

**W6–W7 · Sep 28 – Oct 11 · Owner: AI (volume), Op (approval), Ext (real UGC)**

## 4.1 Where AI is actually good enough — and where it isn't

Be honest about this, because the failure mode is expensive and slow to detect.

| Task | Verdict | Why |
|---|---|---|
| Ad angles, hooks, script variants at volume | ✅ **Excellent** | Genuine 100x on ideation throughput |
| Ad copy, headlines, primary text variants | ✅ **Excellent** | High volume, cheap, easy to A/B |
| Static ads, product composited into scenes | ✅ **Good** | Mature tooling; convincing output |
| Voiceover over real product b-roll | ✅ **Good** | Quality is there; no uncanny-valley risk |
| Review mining → positioning | ✅ **Excellent** | Genuinely better than a human at 200+ reviews |
| **AI avatar physically using the product** | ❌ **Not good enough** | Hand-object interaction still fails; reads fake |
| **AI-generated "real customer" testimonial** | 🚫 **Illegal** | See 4.3 — not a quality question |

**The operating split: buy real footage of hands using the product, generate everything
around it at volume.** One real creator video yields dozens of AI-assisted variants —
different hooks, captions, edits, voiceovers, and openers cut against the same demo
footage. That combines the credibility AI can't fake with the volume humans can't produce.

Also: **the QC sample from Phase 2 is the creative shoot.** Film it while inspecting it.

## 4.2 Pipeline

1. **Angles** (AI) — from review-mining, generate 10–15 distinct positioning angles.
   Angles, not hooks: "for people whose problem is X."
2. **Hooks** (AI) — 5 hooks per angle → 50–75 first-3-seconds. The hook is the highest-
   leverage element on paid social.
3. **Scripts** (AI) — 15–30s, hook → problem → demo → offer → CTA.
4. **Footage** (Ext) — 2–3 real creator videos. Market rate **$99–150/video** via Billo-type
   marketplaces, $150–300 for a beginner independent creator [UNCERTAIN — secondary].
   ⚠️ **Usage rights add 50–150% on top of base rate** and are the line item people forget
   to budget.
5. **Assembly** (AI + Op) — cut each hook against the real footage. 12+ finished variants.
6. **Statics** (AI) — 6–10 image ads for retargeting and Meta placements.

**Volume target: 12+ video variants and 6+ statics before launch.** Calibration from
[BENCHMARK — Motion Creative Benchmarks 2026, $1.29B Meta spend, 578,750 creatives]:
**only ~5% of creatives become "winners," and 55% of spend concentrates on them.**
Enterprise accounts ship **18.8 creatives/week**. At a 5% hit rate, 12 variants is roughly
*one* expected winner — which is why creative volume, not targeting, is the real lever.

**Tooling** [UNCERTAIN — verify pricing directly, vendor pages change constantly]:
Pebblely $9–39/mo or Flair.ai free–$38/mo for product imagery; Photoroom API $0.02–0.10/call
for volume background work; HeyGen $29–149/mo for voice/avatar. **Meta's native Advantage+
creative tools generate variants inside Ads Manager** and may be free — worth checking
first, as it would undercut the paid stack entirely. [NOT VERIFIED whether free]

## 4.3 ⚠️ Compliance — the real ban risk

**Read this section before writing a single script.** These are not best practices; they
are the two ways this business dies suddenly.

### Platform disclosure

- **Meta auto-labels.** [CONFIRMED —
  [about.fb.com](https://about.fb.com/news/2025/02/gen-ai-transparency-metas-ads-products/)]
  You do not self-declare for commercial ads, but Meta detects third-party AI tools via
  industry-standard provenance signals. Critically: *"When these tools result in the
  inclusion of an AI-generated photorealistic human, the label will appear next to the
  Sponsored label"* — the **most visible** position.
- **TikTok requires you to affirmatively label.** [CONFIRMED —
  [ads.tiktok.com](https://ads.tiktok.com/help/article/tiktok-ads-policy-misleading-and-false-content)]
  *"Significantly edited media and AIGC content is allowed if the following requirements
  are met: Apply the AIGC label, or by adding a clear disclaimer, caption, watermark, or
  sticker."*
- **Do not attempt metadata stripping.** TikTok applies **invisible watermarking** designed
  to survive download and re-upload, and Meta uses independent detection. [CONFIRMED]

**Design implication: assume every AI-avatar ad is visibly badged as AI on both platforms.
Make creative that still works when the audience knows.**

Also prohibited on TikTok [CONFIRMED, same source]: before/after imagery that creates "a
false or distorted impression about a product's outcome," and ads that "promise or
exaggerate results."

### FTC — the bright line

**16 CFR Part 465** (Rule on the Use of Consumer Reviews and Testimonials) took effect
**2024-10-21** and is actively enforced — the FTC sent fake-review warning letters in
**December 2025 and January 2026**. [CONFIRMED]

It prohibits fake or false reviews and testimonials **including AI-generated ones and
testimonials from people who never used the product** — plus buying reviews, undisclosed
insider reviews, and fake indicators of social influence.

> **Maximum civil penalty: $53,088 per violation.** [CONFIRMED]
> Note this is a **nonstandard year** — the October 2025 appropriations lapse prevented BLS
> from computing the required CPI-U, and OMB cancelled the 2026 adjustment
> ([FR 2026-13629](https://www.federalregister.gov/documents/2026/07/07/2026-13629/no-adjustment-to-civil-monetary-penalty-amounts)).
> The 2025 figure carries through 2026. Anyone quoting a higher 2026 number is
> extrapolating an adjustment that did not occur.

**The FTC treats each individual fake testimonial as a separate violation.** Exposure is
effectively unbounded at ad scale.

### 🚫 The rules, stated as rules

1. **An AI persona may present. An AI persona may NEVER claim to have bought or used the
   product.** That single sentence is the line between a synthetic presenter (permitted)
   and a false testimonial (illegal). Every script gets checked against it.
2. **No AI-generated reviews.** Not on the site, not in ads, not "just for launch."
3. **Every objective claim needs substantiation we actually hold** before it runs.
4. **No fake urgency, no fake scarcity, no fake compare-at pricing.**
5. **Disclose material connections** for any creator we pay.

**Note the enforcement context:** the FTC's *Operation AI Comply* (2024) and the
**Ecom Empire Builders** action (~$25M consumer harm, court order May 2025) both targeted
"AI-powered online store" businesses specifically. **This is a named FTC enforcement
priority category, not a neutral one.** We are in it by definition.

### Open question — resolve empirically

**Does AI-labeled content get suppressed?** There is **no credible evidence either way** —
every claim in circulation traces to marketing blogs, not to Meta or TikTok. One confirmed,
relevant fact: TikTok ships a user-facing **"Manage Topics" AIGC slider** letting viewers
dial AI content down in their own feed. That is not algorithmic suppression, but it is real
distribution risk we cannot measure from outside.

**Therefore: a matched A/B test of AI-avatar vs. real-creator creative at equal spend is a
Phase 5 deliverable.** It is the only way to answer this.

### Deliverables

| # | Deliverable | Owner | Due |
|---|---|---|---|
| 4.1 | 10–15 angles from review-mining | AI | Sep 29 |
| 4.2 | 50+ hooks | AI | Sep 30 |
| 4.3 | 2–3 real creator videos commissioned **with usage rights** | Op + Ext | Oct 2 |
| 4.4 | 12+ finished video variants | AI + Op | Oct 8 |
| 4.5 | 6–10 statics | AI | Oct 8 |
| 4.6 | **Compliance pass — every asset against the 5 rules** | **Op** | Oct 9 |
| 4.7 | AIGC labels applied to all AI assets | Op | Oct 9 |

### 🚪 GATE C — Fri Oct 9 (Phases 3 + 4)

- [ ] Test purchase completes; GA4, Meta CAPI, TikTok Events API all fire
- [ ] 12+ video variants and 6+ statics finished
- [ ] **Every asset passed the compliance checklist and is labeled**
- [ ] Offer, bundle, upsell live
- [ ] Fulfilment confirmed ready to ship within 48h of order

---

# PHASE 5 — Paid Acquisition

**W7–W10 · Oct 5 – Nov 1 · Owner: Op (media buying), AI (analysis)**

## 5.1 Channel order of operations

**1. TikTok first.** Not fashion — arithmetic. Median TikTok CPA is **$17.07** against
Meta's **$38.99** [BENCHMARK], and at our $45–70 price band **only TikTok's median CPA
clears our CAC ceiling**. Cheapest place to learn which creative works.

**2. Meta second**, once we have a proven hook *or* AOV above ~$58. Meta's audience network
and retargeting are stronger, but its median CPA demands a higher AOV to work.

**3. Google Shopping / PMax last**, only after creative is proven. Search captures existing
demand; for a product nobody is searching for yet, we must *create* demand first. Note
there is **no credible ecommerce Shopping/PMax benchmark** in the WordStream dataset — it
covers text Search only — so we will be flying on our own data here.

**Use Spark Ads on TikTok from day one.** [BENCHMARK — AdLiftr, 3,127 campaigns, $18.7M
spend, Feb–May 2026]: Spark Ads posted **1.62% CTR vs 0.84%** for standard in-feed, with
**28% lower CPA**. Running creative through a real creator handle roughly doubles CTR.

## 5.2 Testing framework

**Structure:** one campaign, broad targeting, creative as the variable. Modern algorithms
find the audience; our job is to feed them creative. Interest stacking is mostly obsolete.

**Budget per test:** $20–30/day per ad group, 3–5 creatives each. **$150–200/day total** at
full tilt, starting at $50–75/day.

**Creative volume:** 5+ new variants/week, sustained. At a ~5% winner rate [BENCHMARK,
Motion], this is the only reliable path to a winner. **Creative volume is the strategy.**

### Kill criteria — pre-committed, non-negotiable

| Level | Kill when | Rationale |
|---|---|---|
| **Creative** | 1,000 impressions, **link CTR <0.8%** (TikTok) / **<1.2%** (Meta) | Below benchmark floor — see note |
| **Creative** | Spend = 1× target CPA, zero add-to-carts | Not the audience; the creative |
| **Ad group** | Spend = 2× target CPA, zero purchases | |
| **Ad group** | Spend = 3× target CPA, CPA above break-even | |
| **Campaign** | $500 spend, CPA >2× break-even, no improving trend | |
| **Product** | $1,500 spend, no path to CPA <$32.71 | → Gate D |

> ⚠️ **Use *link* CTR, not all-clicks CTR.** The widely-quoted Meta CTR of 2.39% [Triple
> Whale] is almost certainly all-clicks. Gupta Media, which explicitly measures link CTR,
> reports **1.59–1.77% for Meta and 0.95–0.97% for TikTok**. **Setting kill thresholds
> against the all-clicks number would cut winning creatives.** Our floors above are set
> just below the measured link-CTR benchmarks.

### Scaling rules

- Winner = CPA below target for **3 consecutive days at meaningful volume**. One good day
  is noise.
- Scale **+20–30% every 2–3 days**. Larger jumps reset the learning phase.
- Never scale on a single day's ROAS.
- Duplicate winners into a higher-budget campaign rather than shocking the original.

## 5.3 Target metrics — derived, not invented

From [unit economics](docs/unit-economics.md#4-worked-example--base-case), base case
$49 AOV, $11.40 landed:

| Metric | Target | Derivation |
|---|---|---|
| **Break-even ROAS** | **1.50x** | 1 ÷ 66.8% contribution margin |
| **Target ROAS (20% net)** | **2.14x** | 1 ÷ (0.668 − 0.20) |
| **Max CPA (break-even)** | **$32.71** | = contribution margin |
| **Target CPA** | **$22.91** | CM − 20% of revenue |
| CPM | $4–16 (TT), ~$15 (Meta) | [BENCHMARK] — see warning |
| Link CTR | >1.0% (TT), >1.5% (Meta) | [BENCHMARK] Gupta Media |
| Site CVR | 1.0–1.5% cold paid social | [ASSUMPTION] — biggest gap |

> ⚠️ **Plan TikTok CPM at $16.20, not $4.08.** Triple Whale's $4.08 blends cheap reach
> inventory; AdLiftr's conversion-objective median is **$16.20** [BENCHMARK]. We will be
> buying conversion inventory. The optimistic number is not the one we pay.

> ⚠️ **The cold paid-social CVR assumption is the weakest input in the entire plan** and
> the one everything else depends on. No disclosed-sample benchmark exists for it. Replace
> with measured data at 100+ sessions and re-run every table in
> [unit-economics.md](docs/unit-economics.md).

## 5.4 Organic flywheel

Blended CAC beats paid CAC if organic contributes at all. Low cost, compounding:

- **Post every ad creative organically** to a branded TikTok. Free distribution of assets
  we already paid for, and it feeds Spark Ads.
- **Seed the creator relationship** — creators posting to their own audience produce
  Spark-eligible content with real social proof.
- **Email/SMS capture** on-site. Post-purchase flows and abandoned-cart are the highest-ROI
  marketing we will run, and they carry **no CAC at all**.
- Measure via **blended MER**, not channel ROAS — Phase 6.

### Deliverables

| # | Deliverable | Owner | Due |
|---|---|---|---|
| 5.1 | TikTok Ads + Meta Business accounts, pixels verified | Op | Oct 7 |
| 5.2 | TikTok campaign live, Spark Ads, 12+ creatives | Op | Oct 12 |
| 5.3 | **AI vs. real-creator A/B at matched spend** (from 4.3) | Op | Oct 19 |
| 5.4 | Weekly creative refresh, 5+ variants | AI + Op | ongoing |
| 5.5 | Meta launched with winning TikTok hooks | Op | Oct 22 |
| 5.6 | Weekly performance review vs. kill criteria | AI | Fridays |

### 🚪 GATE D — Mon Nov 2 · The big one

After **$1,500** in ad spend:

- [ ] CPA **below $32.71** (break-even) on at least one creative/audience combination
- [ ] ≥1 creative beating benchmark link CTR
- [ ] Site CVR **≥1.0%** on cold paid social
- [ ] A credible, specific path to a **$22.91** target CPA

**Meet all four → Phase 6, scale.**
**Meet 2–3 → one 2-week extension with new creative angles. Once. No second extension.**
**Meet 0–1 → kill the product. Return to the Gate A shortlist.**

---

# PHASE 6 — Operations & Finance

**Continuous from launch · Owner: Op**

## 6.1 The financial model

Full derivations in [docs/unit-economics.md](docs/unit-economics.md). Carry these:

```
Contribution margin  CM = R(1−r) − C − (pR + f) − b(R+K) − s
Break-even ROAS         = 1 / cm                    where cm = CM/R
Target ROAS (margin m)  = 1 / (cm − m)
Max CPA                 = CM
Break-even MER          = V / (V·cm − F)            V = revenue, F = fixed costs
```

**ROAS measures a campaign; MER measures the business.** Break-even MER is always worse
than break-even ROAS, and the gap narrows as revenue grows against fixed costs. **An early
store can hit profitable ROAS every single day and still lose money every month.** Report
MER monthly.

## 6.2 Cash flow — where profitable businesses die

Ad spend leads revenue. Revenue lags into a payout schedule. Goods are paid up front.

```
Day 0     Pay supplier · pay for ads
Day 0–2   Customer pays        → held by processor
Day 2–7   First payout         → longer for new accounts [ASSUMPTION]
Day 0–120 Reserve withheld     → [CONFIRMED mechanism]
```

**Peak cash need ≈ (daily ad spend + daily COGS) × days-to-payout + reserve balance.**

At $200/day spend with a 7-day payout and a 20% reserve, that is **$1,400–2,000 of
permanently deployed working capital** before any growth. Scaling ad spend scales this
linearly — **growth consumes cash even when every order is profitable.** This is the single
most common way an otherwise-working store dies.

## 6.3 Capital plan to Gate D

| Item | Amount | Note |
|---|---:|---|
| Samples (3 suppliers) | $200–400 | |
| Shopify | ~$3 | $1/mo promo ×3 [CONFIRMED] |
| Domain | $12 | |
| Apps | $0–150 | Free tiers where possible |
| AI creative tooling | $50–200 | 1–2 months |
| **Real creator videos + usage rights** | **$300–600** | Don't under-budget rights |
| **Ad test budget to Gate D** | **$2,000–3,000** | The real number |
| LLC + registered agent | $100–500 | State-dependent |
| **Total** | **$2,700–4,900** | [ASSUMPTION] |

**Plus working capital per §6.2 — do not count it as spendable.**

## 6.4 Legal & admin

| Item | When | Note |
|---|---|---|
| **LLC** | Before first sale | Liability separation. Home state unless a reason otherwise — Delaware adds cost and foreign-qualification for a single-member store |
| **EIN** | With LLC | Free, direct from IRS. Never pay a service |
| **Business bank account** | Before first sale | Commingling pierces the liability shield you formed the LLC for |
| **Sales tax nexus** | Monitor from day one | Economic nexus commonly triggers at **$100k or 200 transactions** per state [ASSUMPTION — thresholds vary and change; verify per state]. Shopify Tax can track it. Register **only** where nexus is established |
| **Customs bond** | Before bulk import | Required in ACE eBond *before* filing [CONFIRMED] |
| **Supplier agreement** | Before bulk order | Specs, defect rate, remedy, IP warranty, MOQ, lead time |
| **Business insurance** | Before scale | General liability + product liability |

**Do not skip the product liability question.** As importer of record on a bulk entry, we
are the responsible party for defects in US law — not the Chinese manufacturer.

## 6.5 Kill criteria for the whole product

Written now, while unemotional. The most expensive mistake in dropshipping is not picking
a bad product — it is **refusing to stop testing one.**

**Kill immediately if:**
- Gate D fails on 0–1 of 4 criteria
- Dispute ratio exceeds **0.6%** (internal ceiling, well below VAMP's 1.5%)
- A payment reserve is imposed and cash cannot cover 120 days
- Patent/trademark claim, or platform ban on the product category
- Supplier fails and no backup ships within 10 days
- Landed cost rises such that margin drops below **3x** (a duty change alone can do this)

**Kill after one extension if:**
- CPA stays above break-even across 3 consecutive weeks with fresh creative each week
- Site CVR stays below 1.0% after two rounds of page iteration
- 30+ creative variants tested with zero clearing benchmark CTR

**The re-test loop:** on kill, return to the Gate A shortlist and take the next-highest
scorer. **Everything in Phases 2–6 is reusable** — store, 3PL, pixels, creative pipeline,
LLC. A second product should reach Gate D in ~4 weeks instead of 10. **This is why the plan
front-loads reusable infrastructure.**

**Scale if Gate D passes:** raise budget 20–30% every 2–3 days, switch to bulk import + 3PL
(Phase 2 scale route), add SKUs, build email/SMS. Recompute unit economics at every step —
the numbers move when the route moves.

---

# Master Checklist

## Phase 1 — Product research → Gate A (Sep 4)
- [ ] 40+ raw ideas logged in intake table
- [ ] Hard-gate pass over all ideas; rejections logged with reason
- [ ] 20+ candidates fully scored on the weighted rubric
- [ ] Demand validated from ≥4 independent sources per finalist
- [ ] Meta Ad Library longevity check on top 5
- [ ] Review-mining brief (200+ reviews) for top 3
- [ ] Landed-cost worksheet, **both routes**, for top 5
- [ ] 3 ad angles drafted per finalist
- [ ] **GATE A:** ≥1 candidate ≥4.00, C1 & C2 both ≥3, all 8 hard gates passed

## Phase 2 — Fulfilment → Gate B (Sep 25)
- [ ] 3 suppliers contacted; **US warehouse stock verified per SKU**
- [ ] Samples ordered from 3 suppliers
- [ ] 10-digit HTS code determined
- [ ] Customs broker engaged; bulk-entry quote obtained
- [ ] Landed cost finalised incl. duty + brokerage, both routes
- [ ] Samples received; QC checklist scored
- [ ] Actual transit time logged vs. promise
- [ ] Product filmed & photographed during QC *(feeds Phase 4)*
- [ ] Backup supplier confirmed for same SKU
- [ ] Returns/refund policy written
- [ ] **GATE B:** QC passed, <10 day transit, ≥3x margin, backup identified

## Phase 3 — Store build → Gate C (Oct 9)
- [ ] Domain + Shopify Basic live
- [ ] Dawn theme customised, mobile-first
- [ ] Product page copy from review-mining angles
- [ ] Offer: anchor price, bundle, free-shipping threshold
- [ ] Post-purchase upsell configured
- [ ] Trust elements: real reviews, contact, policies
- [ ] GA4 enhanced ecommerce
- [ ] Meta pixel + **CAPI** server-side
- [ ] TikTok pixel + **Events API** server-side
- [ ] UTM convention documented
- [ ] **Test purchase — all events verified firing**

## Phase 4 — AI creative → Gate C (Oct 9)
- [ ] 10–15 angles from review-mining
- [ ] 50+ hooks
- [ ] 2–3 real creator videos **with usage rights secured**
- [ ] 12+ finished video variants
- [ ] 6–10 statics
- [ ] **No AI persona claims to have used the product**
- [ ] **No AI-generated reviews anywhere**
- [ ] **Every objective claim substantiated**
- [ ] **AIGC labels applied** (TikTok requires affirmative labeling)
- [ ] No fake urgency, scarcity, or compare-at pricing
- [ ] Creator material connections disclosed
- [ ] **GATE C:** tracking verified, 12+ assets, compliance signed off

## Phase 5 — Paid acquisition → Gate D (Nov 2)
- [ ] TikTok Ads + Meta Business accounts live, pixels verified
- [ ] Kill criteria written down **before** spending
- [ ] TikTok campaign live with **Spark Ads**
- [ ] **AI vs. real-creator A/B at matched spend**
- [ ] Weekly creative refresh (5+ variants/week)
- [ ] Weekly review against kill criteria
- [ ] Meta launched with proven hooks
- [ ] **GATE D:** CPA <$32.71, CTR above benchmark, CVR ≥1.0%, path to $22.91

## Phase 6 — Ops & finance (continuous)
- [ ] LLC formed
- [ ] EIN obtained (free, direct from IRS)
- [ ] Business bank account — **no commingling**
- [ ] Sales tax nexus monitoring on
- [ ] Customs bond filed (before bulk import)
- [ ] Supplier agreement executed
- [ ] Product liability insurance (before scale)
- [ ] Unit economics recomputed after first 100 orders
- [ ] **Monthly blended MER review**
- [ ] Dispute ratio monitored against **0.6% internal ceiling**

---

# Verification Queue

Items this plan depends on that are **not** fully verified. Close these before the capital
commitment they gate.

| # | Item | Blocks | Owner |
|---|---|---|---|
| V1 | Our specific 10-digit HTS code | Phase 2 landed cost (~$2/unit swing) | Op + Ext |
| V2 | Current informal-entry MPF amount | Landed cost | Ext |
| V3 | Customs broker quote for **postal** informal entry — the only route found that avoids the ~$17.50 express disbursement floor | Could reopen direct-parcel economics | Op + Ext |
| V4 | CSMS # 69183472 carve-outs during the delayed-compliance window ending **2026-10-22** | Phase 2 timing | Op |
| V5 | Meta Business Help articles 1010479435004531 and 539137881899016 (JS-rendered; read in a browser) | Phase 4 compliance | Op |
| V6 | 16 CFR Part 465 full text on eCFR | Phase 4 compliance | Op |
| V7 | TikTok Ads US account-opening status (evidence stops at Mar 2026; Jan 2026 JV restructuring) | Phase 5 launch | Op |
| V8 | Shopify Payments new-merchant first-payout timing | Cash flow model | Op |
| V9 | Whether dropshipping is named on Shopify/Stripe restricted-business lists | Existential | Op |
| V10 | Mastercard SMMP thresholds (live since 2026-07-24) | Dispute monitoring | Op |
| V11 | Cold paid-social CVR — no disclosed-sample benchmark exists | **Every number in the model** | Measure it |
| V12 | Whether Meta Advantage+ generative video is free | Phase 4 tooling budget | Op |

**V11 is the one that matters most.** It is the most load-bearing input in the plan and the
least supported. Everything downstream is provisional until we measure it ourselves.
