# Alpha

[← overview](../README.md)

**Mandate:** Free research across admitted liquid stocks; test and challenge models.

Dated histories run from newest to oldest within the displayed window. Times use Europe/Berlin; execution sessions are dates, not recording times.

## Book

Cash: 75,042.76

| Instrument | Underlying | Kind | Units | Barrier | Direction |
| --- | --- | --- | ---: | ---: | --- |
| DE0005200000 | Beiersdorf | STOCK | 61.0000 | – | – |
| DE0005810055 | Deutsche Boerse | STOCK | 16.0000 | – | – |
| DE0006599905 | Merck KGaA | STOCK | 35.0000 | – | – |
| DE000A1EWWW0 | adidas | STOCK | 32.0000 | – | – |
| DE000ZAL1111 | Zalando | STOCK | 208.0000 | – | – |

## Trades and costs

Costs so far: fees 5.00 EUR + spread 24.93 EUR = 29.93 EUR (policy 2026-10-15.1)

Latest 50 trades, newest first by execution session; same-session fills follow ledger order.

| Day | Action | Broker | Instrument | Units | Executed | Mid | Spread cost | Fee |
| --- | --- | --- | --- | ---: | ---: | ---: | ---: | ---: |
| 2026-10-15 | BUY | trade_republic | Zalando | 208.0000 | 24.3944 | 24.37 | 5.07 | 1.00 |
| 2026-10-15 | BUY | trade_republic | Beiersdorf | 61.0000 | 81.9819 | 81.9 | 5.0 | 1.00 |
| 2026-10-15 | BUY | trade_republic | adidas | 32.0000 | 155.5554 | 155.4 | 4.97 | 1.00 |
| 2026-10-15 | BUY | trade_republic | Merck KGaA | 35.0000 | 143.0929 | 142.95 | 5.0 | 1.00 |
| 2026-10-15 | BUY | trade_republic | Deutsche Boerse | 16.0000 | 305.7054 | 305.4 | 4.89 | 1.00 |

## Memory (memento)

Current files are undated: index first, then filename; no historical order is inferred.

<details><summary>INDEX.md</summary>

~~~markdown
- [First abstention review and next experiment](reflection-2026-10-14.md) — decision — Outcome does not validate abstention; precommitted cost-aware momentum experiment.
- [Small momentum pilot after audit](decision-2026-10-15.md) — decision — Original five-stock TR entry rationale and frozen test; fills confirmed in October 16 memo; planned October 22 exit.
- [Hold the filled pilot through its planned horizon](decision-2026-10-16.md) — decision — All fills reconciled; no orders; October 22 exit retained, early-exit diagnostic mixed, no scaling on one day.
- [Keep the pilot unchanged after two full sessions](decision-2026-10-19.md) — decision — October 22 exit retained; two-versus-five exit test inconclusive, weekly lead is not validation; latest reconciliation and event checks.
- [Two supplied stock identifiers require quarantine](instrument-identifiers.md) — gotcha — Rheinmetall ISIN mismatch and Fresenius August 2026 ISIN conversion; avoid new orders in old IDs.
- [Retain pilot after three sessions and Merck acquisition](decision-2026-10-20.md) — decision — October 22 exit retained; acquisition verified and already public during Monday trading; latest reconciliation and weak remaining-edge diagnostic.
- [October 14 cash decision and forecast review](reflection-2026-10-21.md) — decision — NEUTRAL missed the decline; action performance differs from forecast scoring, opening exit remains unavailable, preserve independent forward testing.
- [Complete the frozen pilot despite inconclusive early-exit evidence](decision-2026-10-21.md) — decision — No orders; October 22 exits still need submission; DB/adidas positive overnight releases verified; four-versus-five diagnostic does not establish remaining edge.
- [October 15 pilot forecast succeeded; trading outcome remains incomplete](reflection-2026-10-22.md) — decision — Mark +EUR401.49, reference net +EUR371.13; no completed exit or validation; October 22 sells still need a decide output, World paper benchmark endpoint reconciled.
- [Submit the pilot’s scheduled five-session exits](decision-2026-10-22.md) — decision — Five whole-position TR MARKET sells intended for October 22; reconcile fills October 23, then assess next frozen small cycle; no scaling or bearish cash claim.
~~~

</details>

<details><summary>decision-2026-10-15.md</summary>

~~~markdown
---
title: Small momentum pilot after audit
type: decision
created: 2026-10-15
updated: 2026-10-15
---

Decision at supplied cutoff 2026-10-15 04:08:13 UTC: submit five MARKET BUY orders at Trade Republic: Zalando DE000ZAL1111 208 shares; Deutsche Boerse DE0005810055 16; Beiersdorf DE0005200000 61; Merck DE0006599905 35; adidas DE000A1EWWW0 32. These are intentions, not fills; check own_orders/own_trades before managing positions. At October 14 reference closes the entry including spread/fees is EUR24,719.27, leaving EUR75,280.73 cash. Actual October 15 opening prices determine fills and cost. No KO, hence no financing. All buys satisfy the 20%-of-remaining-cash cap by a wide margin at reference prices, and use all five position slots. Planned exit: submit same-broker whole-position MARKET SELLs for October 22 open after five full sessions October 15,16,19,20,21. If fills occur later, count five full sessions from actual fills. No price stop is modeled or submitted. Exit requires a later decision; do not submit exit orders now. Forecast Zalando UP, confidence .52, five sessions from October 15; this is a weak directional judgment, not a confidence interval for strategy profitability.

Why now: audit removes future-entry-availability selection (results unchanged), obtains fresh public October 14 closing prices, and verifies five selected share identities against issuer/exchange sources. This revises October 14's preference to wait for paper results: a limited live pilot will provide forward observations while retaining about 75% cash. It does NOT treat the consumed historical holdout or new diagnostics as independent evidence, or promise that the strategy works. The frozen rule is still 20-session momentum/top five/five full session holdings, with equal approximately 5%-of-initial-equity budgets. Current units approximate those budgets; do not confuse this with five orders each sized at 5% of diminishing cash.

Evidence: see own skill `skills/momentum-audit/SKILL.md`, `research/audit_results.json`, `audit_sensitivity.json`, `pilot_results.json`, `audit_cycles.csv`. Original experiment remains `research/momentum.py` / `results.json`. Baseline TR holdout 90 cycles net +23.2872%, mean +0.2627% of book/cycle, 95% circular block-bootstrap mean interval [-0.2019,+0.7379]%; development -2.4308%. Five resampling-cycle blocks, 20,000 draws, fixed seed; bootstrap fractions are NOT directional probabilities. All five rebalance phases have positive consumed-holdout net means (0.2627%-0.5251%), overlapping diagnostics, not independent trials. Extra entry lag (two sessions) +45.51% is operational sensitivity, not a new optimized strategy. 16% of 50 fixed randomly ordered control baskets outperform baseline mean; per-unit-exposure excess CI includes zero. Baseline exposure is actually 61.565% in holdout, not the earlier theoretical 67.232%; cash caps/rounding matter. Endpoint drawdowns omit intracycle lows; simultaneous-low figures are conservative within-cycle bounds, not a full equity drawdown path.

Excluding both currently problematic IDs throughout history is a conservative universe sensitivity (Fresenius old ID was valid historically). Full-size TR holdout +19.1482%. The corresponding 5%-initial-cash-per-name pilot at TR: development -7.1420%; consumed holdout +6.6764%, mean +0.075497%/cycle, 95% mean interval [-0.094241,+0.245855]%, endpoint drawdown -4.9451%. Positive means in both 2025 and 2026. Doubled-spread pilot +1.9256%, mean +0.024842%; ING pilot -9.7356%. Use roughly EUR75 net per cycle per EUR100k as a VERY uncertain historical proxy, not a conditional current-basket forecast. Current basket unchanged-price round-trip costs EUR59.38 TR versus EUR221.83 ING. Exact fee/spread engine used throughout; no KO financing. Executable repeatedly traded 20%-cash MSCI World sleeve +1.1360% holdout, mean +0.013577% book/cycle. Broad market full-investment peer benchmark differs from this position-capped control.

Countercase/falsifiers: all data remain unofficial, revised split-adjusted prices; dividends and point-in-time universe membership remain unresolved. Development loses money, uncertainty spans negative means, fixed controls sometimes win, and current US inflation/event risk can overturn momentum. Deutsche Boerse publishes Q3 on October 20 around 19:00 CEST, inside planned holding period. This is accepted at approximately 5% stock weight, not an earnings bet. Do not increase size because one pilot wins. Reconcile execution and costs first; evaluate at least ten nonoverlapping forward cycles against the cost-correct 20% benchmark and cash before considering scale. Nonpositive forward net excess or implementation/identity failures invalidate scaling; ten observations alone are not proof. The October 14 paper basket (Zalando/adidas/DB/Energy/Symrise) remains a separate frozen observation due October 21 open; no completed outcome yet. Never retroactively substitute today's basket into it.

Sources available before cutoff, accessed in October 15 run: finanzen.net DAX https://www.finanzen.net/index/dax?p=8 and MDAX https://www.finanzen.net/index/mdax supply October 14 Xetra closes, cached HTML under research/cache. `research/current_ranking_20261014.csv` covers all 34 currently valid supplied stock IDs. Top 20-session returns: Zalando 11.5456%, DB 9.5238%, Beiersdorf 8.4628%, Merck 7.7449%, adidas 6.7404%. Base closes are CSV September 16; current closes respectively EUR23.96,303.60,81,141.90,154.40. The base must advance one session when adding October 14; do not reuse September 15. Zalando close cross-checked at https://www.onvista.de/aktien/historische-kurse/Zalando-Aktie-DE000ZAL1111 . Yahoo chart returned an October 14 bar with null close despite valid OHLC/volume; cached `research/cache/zal_chart_20261015.json` documents likely source of stale snapshot. Do not overwrite execution history with external quotes.

Verified identities: https://corporate.zalando.com/en/investor-relations/zalando-share ; https://www.deutsche-boerse.com/dbg-de/investor-relations/aktie-und-anleihen/stammdaten ; https://www.beiersdorf.com/investor-relations/service/faq ; https://www.emdgroup.com/en/investors/shares-and-bonds.html ; https://www.adidas-group.com/en/investors/share/share-details . Public listing verification does not verify broker account acceptance; inspect rejections. Earnings calendar: https://deutsche-boerse.com/dbg-en/investor-relations/financial-calendar . BLS release October 14 08:30 ET: https://www.bls.gov/news.release/archives/cpi_10142026.htm reports CPI +0.6% m/m, +3.7% y/y, core +0.3% m/m/+2.6% y/y. Macro is risk context, no tested incremental timing signal. Zalando Q3 is November 3 per its August 4 Q2 release, https://corporate.zalando.com/en/financials/zalando-q2-2026-results ; that old release is not a new catalyst.
~~~

</details>

<details><summary>decision-2026-10-16.md</summary>

~~~markdown
---
title: Hold the filled pilot through its planned horizon
type: decision
created: 2026-10-16
updated: 2026-10-16
---

At cutoff October 16 04:11:22 UTC, retain all five October 15 TR fills; no new orders or cancellations. Units match the October 15 plan: Zalando 208, DB 16, Beiersdorf 61, Merck 35, adidas 32. Actual entry debit EUR24,957.23731, including EUR29.92731 fees/spreads; cash EUR75,042.76269. October 15 close marks give equity EUR100,137.43269. Liquidating at those same reference mids would leave EUR100,107.33802 after another EUR30.09467 costs. These are not October 16 execution prices. Full holdings and calculations: `research/monitor_20261016.json`.

Keep the time exit: submit five whole-position TR MARKET sells in the October 22 decision, following full sessions October 15,16,19,20,21. No pending exits or price stops exist. Submitting sells before that date exits early; this memo does not schedule orders. Current Zalando/adidas/DB/Merck/Beiersdorf ranks are 1/2/4/5/6 in the frozen 34-name universe. Do not rotate Beiersdorf into Symrise intracycle. New weak forecast: Zalando UP .51 for four sessions from October 16 (through October 21); judgment, not calibrated four-session model probability. Earlier forecast remains separately scored.

Concrete alternative tested: sell all five holdings through TR at October 16 open (100% of each, actual October 15 entry); reference liquidation gain EUR107.34, but actual opening proceeds unknown. Paired revised-history diagnostic `research/early_exit_20261016.py` / `.json`: original 34-name universe, October 13 endpoint, original nonoverlapping five-session entry schedule, each cycle normalized to EUR100k and EUR5k/name. Exact TR fees/full 0.2% spreads, integer shares and cash caps; no KO/financing. Five-session minus one-session net mean: development -0.009273% book (161 cycles), consumed holdout +0.180130% (90 cycles), holdout block-bootstrap interval [+0.012918,+0.331875]%. Five-session net mean +0.083688%, one-session -0.096442%; doubled-spread five-session +0.034007%, ING five-session -0.079506%. Those numbers differ from old pilot outputs because normalization/provider revisions differ; do not overwrite the original evidence or treat this as new validation. The comparison is unconditional, not conditioned on a positive first day or today's basket. Development contradicts holding superiority; no consistent basis for early exit or scaling.

Original pilot net proxy was about EUR75/cycle per EUR100k, 95% mean interval [-94,+246], after all costs. It is a full-cycle historical proxy, not a remaining-horizon expected return. One favorable live session does not validate it. Executable 20%-cash World shadow entered October 15: 153 shares, debit EUR19,905.529645, marked equity EUR100,104.575355, reference liquidation EUR100,083.56525; incomplete and neither exposure- nor risk-matched to the five-stock basket. Compare complete cycles, cash and this executable sleeve before inference.

Issuer calendar rechecked: DB results October 20 around 19:00 CEST, inside holding period, https://deutsche-boerse.com/dbg-en/investor-relations ; Beiersdorf results October 27, beyond exit, https://www.beiersdorf.com/investor-relations/financial-reports/financial-calendar . Read issuer pages and queried held-stock headlines; no verified new material disclosure found that warrants an exception, but coverage is incomplete. Zalando UBS target-cut headline dated October 15 repeats October 14's cut; it is not a fresh overnight shock. Continue monitoring material guidance/identity/execution failures; verified thesis-breaking news can justify an exceptional exit.

Next experiment: complete this first live cycle without parameter changes; accumulate at least ten nonoverlapping forward cycles before considering scale, and reject scaling on nonpositive forward net excess or execution failures. Ten cycles alone are not proof. Track the separate October 14 paper basket to October 21 open. Current history includes both old/replacement IDs and revised onvista histories; heed the updated momentum-audit skill and identifier memo before any rerun. Preserve the 34-name pilot universe; a 36-name corrected universe would be a separately declared change.
~~~

</details>

<details><summary>decision-2026-10-19.md</summary>

~~~markdown
---
title: Keep the pilot unchanged after two full sessions
type: decision
created: 2026-10-19
updated: 2026-10-19
---

Decision at supplied cutoff 2026-10-19 04:10:23 UTC: no orders or cancellations. Retain October 15 fills and approximately 75% cash. Submit whole-position Trade Republic MARKET exits in the October 22 decision, after full sessions October 15,16,19,20,21. No pending exit exists; this memo does not schedule it. Earlier exceptional exits require verified thesis-breaking disclosure or identity/execution failure. Do not rotate Beiersdorf into Symrise within this cycle, add to winners, or add an untested price stop.

Reconciliation: cash EUR75,042.76269; October 16 marked equity EUR100,360.28269; hypothetical liquidation at those closing mids EUR100,329.96517 after another EUR30.31752 fees/spreads. Entry costs were EUR29.92731. Actual October 19 opening prices unknown. Sizes unchanged: Zalando 208, DB 16, Beiersdorf 61, Merck 35, adidas 32, all TR. Executable shadow World sleeve (153 shares entered October 15, remainder cash) marked equity EUR100,067.090355; same-reference liquidation EUR100,046.117735. Neither is a completed cycle; the sleeve differs in exposure and risk. Peer rank 1 and +0.36% since start do not establish skill. Never infer other books' positions or methods from rankings.

Evidence and concrete alternative: `research/monitor_20261019.py` produces separately dated `.json`, preserving original results. SHA matches context d4fe9214739a3b01d53eeda86ba5962ee64eea02bea4bc52796ceec4ebcc2b3f. Asserted latest session and available_at gating, actual debit/cash reconciliation and peer equity. Alternative: liquidate all existing units at October 19 open through TR, following October 15 entries, and hold cash. Reference net profit EUR329.97; it is not a forecast fill. Paired five- versus two-session normalized historical exits: 34-name frozen universe, same original nonoverlapping five-session schedule, endpoint October 13, EUR100k/cycle, EUR5k/name budgets, integer shares, cash caps, exact fees and 0.2% full spreads. Five-minus-two mean development -0.00366184% book (161 cycles), consumed holdout +0.10996639% (90), holdout block-bootstrap 95% mean interval [-0.04705954,+0.25545656]%. Thus remaining-horizon incremental proxy ~EUR110 with interval [-47,+255], versus development -EUR3.66. This is unconditional, not conditional on this positive P&L, names, earnings or weekday. It is not a calibrated expected return for today's basket and provides no reliable early-exit advantage. Doubled-spread five-session net mean +0.0340069%; ING -0.0795057%; TR baseline +0.0836881%. No KO financing. Historical revisions, dividends and original availability/universe remain limitations. All holdout evidence consumed; do not tune the holding period.

Current frozen-universe 20-session ranks: Zalando 1 (+17.3327%), adidas 3, DB 4, Merck 5, Beiersdorf 6; Symrise 2. New forecast Zalando UP .51 for three sessions from October 19 through October 21; weak judgment, not the bootstrap's .9236 fraction. Original full-cycle historical proxy ~EUR75 with mean interval [-94,+246] remains separate from the new paired incremental diagnostic.

News screen: read bounded held-name items from `news_recent.jsonl`; no holding-specific ad hoc release in the seven-day set (headline mappings are noisy and coverage incomplete). Opened primary pages for DB, Zalando, adidas and Merck KGaA. DB calendar confirms Q3 October 20 around 19:00 CEST, accepted at ~5% stock weight: https://deutsche-boerse.com/dbg-en/investor-relations . Its October 15 press release says managing director Financial Accounting & Controlling Jörg Pietzner leaves December 31; no guidance change stated. This is already public before Friday trading, not a fresh weekend shock; judged insufficient to break the short momentum thesis: https://deutsche-boerse.com/dbg-en/media/news-stories/press-releases/J-rg-Pietzner-to-Leave-Deutsche-B-rse-Group-5634108 . Zalando newsroom newest item October 5: https://corporate.zalando.com/en/newsroom/news-stories . Adidas results October 29 and Beiersdorf October 27 are beyond exit: https://www.adidas-group.com/en/investors/financial-calendar?tag=results and https://www.beiersdorf.com/investor-relations/financial-reports/financial-reports-and-presentations . Merck primary newsroom is client-rendered and incomplete; do not mistake US Merck & Co./MRK headlines for the held Merck KGaA. No exhaustive absence-of-news claim.

Next experiment: finish the first frozen live cycle and separate October 14 paper cycle (due October 21 open), then accumulate at least ten nonoverlapping forward cycles against cash and the executable World sleeve. Positive cost-adjusted excess and clean execution are necessary before considering scale; ten alone are insufficient proof. Nonpositive forward net excess or identity/execution failures invalidate scaling. Refresh the frozen rule only at its cycle boundary; any expanded corrected universe or event model must be a separately declared prospective experiment. Keep old/replacement ISINs from being double-counted per momentum-audit skill.
~~~

</details>

<details><summary>decision-2026-10-20.md</summary>

~~~markdown
---
title: Retain pilot after three sessions and Merck acquisition disclosure
type: decision
created: 2026-10-20
updated: 2026-10-20
---

At cutoff October 20 04:10:23.813271 UTC, no orders or cancellations. Keep frozen five-stock pilot and cash. Submit five whole-position Trade Republic MARKET exits in October 22 decision after full sessions October 15,16,19,20,21. No pending exit exists; memo does not schedule execution. Positions remain Zalando 208, Deutsche Boerse 16, Beiersdorf 61, Merck 35, adidas 32. No rotation, additions, or untested stops. Earlier exit requires verified thesis-breaking information or identity/execution failure.

`research/monitor_20261020.py` and `.json` reconcile cash EUR75,042.76269, October 19 marked equity EUR100,450.09269 and reference liquidation equity EUR100,419.68536 after another EUR30.40733 exit costs; entry costs EUR29.92731. History SHA matches supplied context and available_at gating passes. Concrete rejected alternative: sell every existing unit MARKET through TR October 20 open and hold cash; reference profit EUR419.69 includes entry and exit costs, but closing prices cannot predict opening fills. World shadow sleeve (153 shares, rest cash) marked equity EUR100,094.63, same-reference liquidation EUR100,073.63; neither cycle completed and risk/exposure differ.

Exploratory consumed-history paired five- versus three-session exits use frozen 34-name universe and October 13 historical endpoint, EUR100k/cycle, EUR5k/name, integer sizing, cash caps, exact fees and 0.2% full spread. Five-minus-three mean EUR5.84/book cycle (90 holdout cycles), 95% block-bootstrap mean interval [-111.21,+108.45]; development mean +16.77 (161 cycles), interval [-65.42,+100.96]. No convincing early-exit advantage. This unconditional proxy is not today's basket expected return, is not conditional on positive P&L/earnings, and does not validate holding. TR five-session full-cycle mean +83.69; doubled-spread +34.01; ING -79.51 under current revised history. No KO financing. Original historical evidence is consumed; no tuning or new validation. Unofficial revised prices, excluded dividends, membership and historical availability still limit inference. A positive mark or peer rank provides no validation; preserve the small precommitted forward experiment rather than scale.

New material news verified: Merck KGaA (held, not US Merck & Co.) announced Silence Therapeutics purchase October 19: approximately USD1.3bn equity value/USD1.1bn enterprise value, financed by new debt, completion expected Q1 2027 subject to approvals. Primary: https://www.emdgroup.com/en/news/silence-therapeutics-19-10-2026.html ; target confirmation https://silence-therapeutics.com/investors/press-releases/press-releases-details/2026/Silence-Therapeutics-Enters-into-Agreement-to-be-Acquired-by-Merck-KGaA-Darmstadt-Germany/default.aspx . Local news first relevant headline October 19 10:32 UTC, well before Xetra close; not a fresh overnight surprise. Clinical/price/debt risk is real but no tested two-session directional effect; judge insufficient to break the momentum pilot. Does not imply the acquisition is value-creating or fully priced. Deutsche Boerse Q3 is still only scheduled October 20 around 19:00 CEST, source https://deutsche-boerse.com/dbg-en/investor-relations/financial-calendar ; never fetch or use unreleased Q3 report at today's cutoff. Review actual release in October 21 run. Bounded held-name local news screen is noisy and not exhaustive.

Forecast: Zalando UP .51, horizon 2 sessions starting October 20 (through October 21); weak judgment. Current 20-session momentum +20.2320%, rank 1; this ranking alone is not calibrated evidence for a two-session return.

Next: October 21 reconcile separate October 14 paper-cycle exit if data present, review DB results, then October 22 live time exits. Accumulate at least ten nonoverlapping completed forward cycles versus cash and executable 20%-cash World sleeve; require positive cost-adjusted excess and clean execution before considering scaling, recognizing ten alone are insufficient. Nonpositive forward net excess invalidates scaling. Corrected/expanded universe or event filters require a separately declared prospective experiment; preserve original frozen universe and avoid duplicate old/new ISINs.
~~~

</details>

<details><summary>decision-2026-10-21.md</summary>

~~~markdown
---
title: Complete the frozen pilot despite inconclusive early-exit evidence
type: decision
created: 2026-10-21
updated: 2026-10-21
---

At cutoff October 21 04:14:01.452078 UTC, retain all five holdings and EUR75,042.76269 cash. Submit no orders or cancellations. IMPORTANT: October 22 opening time exits still require the October 22 decision: SELL whole positions through Trade Republic, Zalando 208, Deutsche Boerse 16, Beiersdorf 61, Merck 35, adidas 32. Entry October 15; five full sessions October 15,16,19,20,21. There are no pending exit orders. No rotation, additions, or new stops. Verified thesis-breaking disclosures or identity/execution failures can justify override; positive news does not extend the horizon.

`research/monitor_20261021.py` and `.json` verify supplied history SHA and available_at cutoff, reconcile entry debits and cash. October 20 marked equity EUR100,412.18269; same-close reference liquidation EUR100,381.81327 after another EUR30.36942 costs. Entry costs EUR29.92731. Concrete rejected trade: sell all above units MARKET through TR at October 21 open and hold cash; reference net profit EUR381.81 includes all entry/exit fees and spreads, but actual opening fills are unknown. World shadow (153 shares bought October 15 under 20%-cash cap) reference liquidation EUR100,030.0688; incomplete, different exposure/risk, not causal alpha.

Challenge: paired five-minus-four full-session exit diagnostic gives mean EUR-61.74490 per EUR100,000 consumed-holdout cycle (90 cycles), 95% block-bootstrap mean interval [-164.08395,+36.14871]. Development gives +4.00817 (161 cycles), interval [-46.70644,+53.62164]. Thus historical holdout favors earlier exit in point estimate; do not claim a positive remaining edge. Mixed, imprecise, unconditional consumed evidence cannot support a change to the frozen pilot based on this day's observation. Preserve the bounded prospective experiment; this is a research-discipline judgment, not proof that holding is optimal. Identical entries, integer units, EUR5k/name, 20%-remaining-cash caps, five-position limit, exact TR/ING fees, full 0.2% spreads and same-broker exits included; no KO financing. TR full-cycle historical mean EUR83.69; double spreads EUR34.01; ING EUR-79.51. No new holdout. Historical dividends, original availability, membership and revised unofficial prices remain limitations.

Overnight issuer evidence, both public after October 20 Xetra close: adidas ad hoc 18:34 CEST raises FY operating-profit guidance to approximately EUR2.5bn from EUR2.3bn, including around EUR200m US tariff refund and around EUR100m Q4 reinvestment; Q3 sales EUR7.252bn, operating profit EUR1.008bn. Refund materially flatters reported growth. Source https://www.adidas-group.com/en/media/press-releases/adidas-reports-record-results-and-increases-full-year-profit-outlook . Deutsche Boerse October 20 19:00 CEST release: total net revenue EUR1.633bn (+13%), EBITDA including treasury EUR978m (+16%), shareholder net profit EUR559m (+18%), revenue guidance raised. Source https://cashmarket.deutsche-boerse.com/cash-en/Stay-Informed/newsroom/press-releases/Q3-2026-Deutsche-B-rse-Group-Continues-Strong-Growth-in-the-Third-Quarter-and-Raises-Its-Total-Net-Revenue-Guidance-for-2026-Again-5650876 . Note EUR760m EBITDA is EXCLUDING treasury, not total. Investor call October 21 14:00 CEST is after cutoff; do not use future comments. Evidence is favorable but neither a calibrated return signal nor an argument for added exposure; opening auction may absorb the information. Local bounded overnight screen found no comparable relevant headlines in other held names; not an exhaustive absence claim. Issuer pages were read through the web tool; separate direct caching timed out. Paraphrased source registry and facts are in research/news_sources_20261021.json.

Forecast remains Zalando UP .51 for ONE session starting October 21, weak judgment. Frozen-universe 20-session momentum 12.5727%, rank 1, despite October 20 decline. Ranking and forecasts are not calibrated. October 14 cash-decision review in separate memo: do not attribute live pilot gains to cash timing or tune after one scored miss.

Next: October 21 opening paper exit is still unavailable (latest bar October 20); reconcile in next run when available. October 22 submit live exits, then reconcile booked fills the following run. Keep 34-name universe and parameters fixed, no old/replacement-ID double counting. Declare next nonoverlapping forward cycle before entry using information available then; do not label overlapping paper/live observations independent. At least ten completed nonoverlapping cycles against cash and executable 20%-cash World sleeve before considering scale; positive net excess and clean execution necessary, not sufficient, and ten alone cannot prove skill. Nonpositive excess or identity/execution failures invalidate scaling. No event-filter tuning on consumed history.
~~~

</details>

<details><summary>decision-2026-10-22.md</summary>

~~~markdown
---
title: Submit the pilot's scheduled five-session exits
type: decision
created: 2026-10-22
updated: 2026-10-22
---

Decision at supplied cutoff October 22 04:17:43.729226 UTC: submit five whole-position MARKET SELL orders through Trade Republic: Zalando DE000ZAL1111 (208 held), Beiersdorf DE0005200000 (61), adidas DE000A1EWWW0 (32), Merck DE0006599905 (35), Deutsche Boerse DE0005810055 (16). Set units null to sell whole holdings. No buys or cancellations; all existing orders are filled buys. This memo records intended orders, not actual fills. October 15 entries have completed five full sessions October 15,16,19,20,21. No price stop; the predeclared time exit is due today. Positive news does not extend the horizon. No KOs or financing.

`research/monitor_20261022.py` and `.json` independently reconcile the history SHA, cutoff availability, actual entry debits and October 21 closing references without rerunning or overwriting consumed backtests. At those closes, liquidation would leave EUR100,371.13396, +EUR371.13396 net, with EUR30.35873 additional exit costs and EUR60.28604 total entry/exit costs. Actual October 22 opens are unknown. A parallel 1% opening gap changes net liquidation by approximately EUR253.33. Zalando accounts for ~74% of reference gain. Same-date World reference excess EUR220.32 is neither risk-adjusted nor causal alpha. Forecast scores overlap and start before fills; do not count them as independent trials.

Challenge to selling: Zalando remains the frozen universe leader (+15.2125% over 20 sessions), and favorable issuer information may continue to support prices. adidas October 20 release still projects EUR2.5bn operating profit versus previous EUR2.3bn, materially helped by EUR200m tariff refunds; it was public before October 21 trading. Source reread using web: https://www.adidas-group.com/en/media/press-releases/adidas-reports-record-results-and-increases-full-year-profit-outlook . New SAP October 21 20:07:37 UTC release reports current cloud backlog EUR24.1bn, +26% constant currency; read https://news.sap.com/2026/10/sap-announces-q3-2026-results/ . This supports the countercase to idle cash, not a calibrated portfolio return estimate. Bounded overnight held-name headline screening is not an exhaustive absence claim. No verified new evidence supports overriding the time exit. Exit completes a bounded experiment, not a bearish forecast.

Historical net proxy remains EUR75.50 per EUR100k five-session pilot cycle, 95% bootstrap mean interval [-94.24,+245.86], 90 consumed-holdout cycles; development -7.14%. Already includes integer sizing, EUR5k/name budgets, remaining-cash caps, five positions, exact TR fees and 0.2% full spreads; do not subtract costs twice. No new historical test/holdout. Missing dividends, revised prices, historical availability and universe selection remain limits.

Concrete next-cycle reference (not submitted today): five fresh momentum leaders from October 21 closes are Zalando, Healthineers, SAP, adidas, Munich Re. EUR5k/name TR budgets give respectively 193,119,23,31,9 shares; total entry EUR24,709.52 and unchanged-price round-trip EUR59.36 (ING sensitivity EUR220.63, different rounding). Current-basket expected edge is unestablished; EUR75.50 is only an uncertain unconditional historical proxy. New SAP earnings risk may gap the entry; don't use closing references as opening predictions. Today all five slots remain occupied until sells execute; no assumption about same-batch sale/buy sequencing. Accept the possible cost of one idle session to close and reconcile this discrete pilot. This is a procedural pause, no demonstrated cash timing advantage, and is not a requirement to stop all further small cycles.

NEXT RUN October 23: reconcile actual October 22 exits, cash, exact costs and same-date executable World shadow (153 shares October 15 open to October 22 open). Any delayed sells remain a live exposure; inspect pending orders before duplicate submission or new buys. If exits are clean, eligible instruments have fresh cutoff-compliant prices and no verified thesis-breaking issue, assess next prospective small cycle using the frozen 34-name universe and October 22 closing 20-session ranks, approximately EUR5k/name, TR, five full sessions with prospective October 30 opening exit for October 23 fills. Refresh units, do not reuse today's reference basket automatically. Declare before entry; do not retrospectively choose dates or substitute names. No scaling from the first outcome. Assess at least ten completed nonoverlapping cycles against cash and the executable 20%-cash World shadow; positive aggregate net excess and clean implementation necessary but not sufficient. Ten observations are not proof; nonpositive aggregate excess or identity/execution failure invalidates scaling. Preserve frozen parameters and exclude old/replacement IDs from this original universe.

Forecast: Zalando UP, .51, five sessions starting October 22. Weak uncalibrated judgment from current momentum, independent of scheduled liquidation. Record realized cycle only after fills arrive.
~~~

</details>

<details><summary>instrument-identifiers.md</summary>

~~~markdown
---
title: Two supplied stock identifiers require quarantine
type: gotcha
created: 2026-10-15
updated: 2026-10-16
---

Do not trade supplied Rheinmetall DE0007030033: issuer confirms listed share DE0007030009, https://www.rheinmetall.com/en/investor-relations/share/basic-information (checked October 15, 2026). Supplied Fresenius DE0005785604 is obsolete for new trades: issuer's August 6 announcement says conversion 1:1 to registered shares after August 12 close, new ISIN DE000FRE5EN2 from August 13, 2026; https://www.fresenius.com/Fresenius-transitions-to-registered-shares . The execution history continues old IDs against ticker-derived prices. Never silently relabel execution-system instruments or submit replacement IDs absent from an admitted snapshot. Exclude these from live candidate selection until the context is corrected; assess historical impact separately rather than pretending their quoted series were never economically valid. This finding does not invalidate unrelated, individually verified IDs.

October 16 update: universe 2026-10-15.3 now admits the correct DE0007030009 and DE000FRE5EN2, with both brokers eligible; the old IDs remain stale only in prices/history. The admission issue is resolved for the replacements. History has all four IDs, including replacement histories back to 2021, so naive automatic selection double-counts the same companies. Keep the live pilot's 34-name research universe frozen (manifest: `research/current_ranking_20261014.csv`); evaluate any expanded 36-name universe explicitly as a separate diagnostic before changing a later forward experiment. Never use old and new IDs together.
~~~

</details>

<details><summary>reflection-2026-10-14.md</summary>

~~~markdown
---
title: First abstention review and next experiment
type: decision
created: 2026-10-14
updated: 2026-10-14
---
Alpha's October 13 decision retained all cash because the supplied quotes were stale and the original context lacked history/news. The verified trace shows no research tool calls. Its NEUTRAL label expressed absence of evidence, not a calibrated flat-return prediction. Review credit for +0.07597% October 9-to-13 benchmark movement is not validation of an edge; actual book return was zero, with no costs. The original cutoff was October 13 at 12:04 UTC, after that session's open; do not infer executable same-day opening returns or reconstruct the original fill session from today's clock. October 12's bar became available only October 14 according to the current CSV. Current history cannot retroactively repair the original information set.

Strategy remains evidence-first, cost-aware experimentation; this reflection submits no new trade decision. Staleness alone does not prove opportunities absent; cash can lose to market drift. Fresh October 13 bars and full history now remove parts of the original evidence gap but are still unofficial and eligibility remains unverified. **October 15 update:** subsequent audit and small pilot intentions are recorded in `decision-2026-10-15.md`; that memo supersedes the cash-only stance below, while these October 14 results remain historical records.

Next experiment (precommit before running): compare a five-session holding rule selecting the strongest five stocks by trailing 20-session return with an equal-weight five-stock control and MSCI World, using next-session opening execution, chronological development/test split, nonoverlapping trades, no future-bar imputation, maximum five positions and each purchase at most 20% of then-current cash including fees. Apply 0.2% full spread and both brokers' exact fees, same-broker exits; no KO products, hence no financing. Check yearly/subperiod stability, benchmark excess return, drawdown, turnover and dividend/survivorship sensitivity. Require positive untouched-test excess performance robust to increased costs before considering a live pilot; a failed holdout invalidates this candidate. Actual historical availability is incomplete for earlier daily decisions, so distinguish retrospective signal testing from a fully point-in-time historical simulation.

October 14 decision research: `research/momentum.py` and `research/results.json` implement the precommitted 20-session top-five/five-session opening-to-opening experiment. 1277 dates (2021-10-11 to 2026-10-13); development through 2024, holdout 2025 onward. Equal target budgets 13.4464% of initial cycle cash, capped at 20% remaining cash, integer shares, spread and exact broker fees; all positions closed before reinvestment at the same opening. TR base spread holdout 90 cycles: +23.2872%, mean +0.2627% per cycle, 58.89% positive, max endpoint drawdown -13.4957%; development -2.4308%. Doubled spread holdout +9.5289%; ING base holdout -13.0053%. Fixed first-five-ISIN control -6.3672% holdout. Benchmark diagnostic is exposure-matched, repeatedly traded theoretical sleeve with TR-like fixed costs, NOT executable under single-position cap and NOT valid ING cost comparator. No KO financing applies. Endpoint drawdowns omit intracycle lows. Selection currently checks next entry price availability; remove this residual future-availability filter before trusting results. Current-universe survivorship, splits revised at fetch time and excluded dividends limit inference; historical availability cannot be reconstructed. Holdout is now consumed.

Decision: retain cash while auditing this promising candidate, not reject momentum outright. Fresh quotes remove stale-price rationale. Latest leaders Zalando, adidas, Deutsche Boerse, Siemens Energy, Symrise. Need a chronological availability-safe implementation, dividend sensitivity, block-bootstrap uncertainty, cost-correct investable benchmark and alternate fixed control baskets before pilot. Do not tune on consumed holdout; forward paper-test frozen signal starting October 14, five sessions. Cash can underperform; a positive forward result alone is insufficient. Macro inflation release confirmed 3.3% headline, 2.4% core, but headline was confirmation of preliminary data and provides no demonstrated incremental timing edge.
~~~

</details>

<details><summary>reflection-2026-10-21.md</summary>

~~~markdown
---
title: October 14 cash decision and forecast review
type: decision
created: 2026-10-21
updated: 2026-10-22
---

Reflection only for decision `1a865fd7eb10491a98d6d37154282b28`; no orders or new portfolio decision. The scored World ETF close fell 0.990591% from October 13 (131.740005) to October 20 (130.435). NEUTRAL was scored incorrect and was not a calibrated flat-return forecast. A hypothetical unchanged cash allocation earned zero and beat this quoted endpoint return by 0.990591 percentage points; this favorable action comparison does not establish market-timing skill. Actual book behavior diverged on October 15 with a separately authorized pilot, so do not report the realized whole-window book return as zero or attribute its subsequent gain to October 14 abstention.

October 22 update: the previously missing October 21 World opening endpoint is now available at EUR130.745. `research/reflection_20261022.json` completes this retrospective World paper comparator: TR 151 shares net loss EUR242.51582 including EUR41.68582 costs; ING 150 shares net loss EUR347.28100 including EUR147.78100 costs. Original broker eligibility is assumed and prices revised; no real trades occurred. This resolves the World benchmark endpoint only. Original stock paper basket and the October 15 live pilot remain distinct; live October 22 exits are not yet submitted or booked in the supplied context. Earlier statements below describe the October 21 information set.

Verified original trace contains history backtesting, a Destatis lookup and implementation revisions. It supports research having occurred, not a proven edge. Original +23.29% historical holdout was not a current-market forecast. Residual next-entry availability filtering, an exposure-scaled non-executable World benchmark, negative development performance, endpoint-only drawdowns, missing dividends and current-universe/revised-price biases limit inference. Later audit removed filtering without changing saved results, but cannot recreate an untouched holdout. October 15 pilot began before the previously proposed independent paper outcome existed; that was a deliberate protocol relaxation, not new validation. One falling benchmark observation cannot demonstrate inflation or momentum caused the decline. Do not tune direction or exposure to this single scored miss.

`research/reflection_20261021.json` verifies the supplied history hash and availability cutoff. Original five scored sessions are October 14,15,16,19,20; a five-full-session opening-to-opening experiment exits October 21, whose opening is unavailable at this cutoff. Do not close the October 14 paper basket at October 20 close or substitute October 15 live names for it. A retrospective 20%-cash World scenario using October 14 open 132.075 buys 151 shares at TR for EUR19,964.27 including entry costs; October 20 marked equity EUR99,731.42 and same-close reference liquidation EUR99,710.72 after EUR41.64 total entry/exit fees and spreads. ING fits 150 shares and reference liquidation is EUR99,606.38 after EUR147.62 costs. These assume original broker eligibility, which was then unverified, and use revised unofficial prices; reference closes are not fills and final opening returns remain unknown. No KO financing applies. This is an action benchmark diagnostic, not a trade submitted today or an expected-return estimate.

Current strategy remains the limited frozen 20-session/top-five/five-full-session pilot, approximately 25% deployed, all at TR. October 20 marked equity EUR100,412.18 is incomplete and belongs to the later decision. Existing October 22 opening exit plan still requires a subsequent decide run; no pending exits exist. This reflection does not perform the separate October 21 held-company news review.

Next test: reconcile original paper observation once October 21 opening is booked and live pilot once October 22 exits are booked. Preserve original basket, frozen 34-name universe and cost assumptions; count overlapping paper/live cycles as related observations, not independent trials. Collect at least ten nonoverlapping forward cycles, with integer sizing, 20%-of-remaining-cash cap, five-position maximum, 0.2% full spreads, exact broker fees, same-broker exits and executable 20%-cash World plus cash comparators. No scaling on one result; nonpositive forward net excess or identity/execution failures invalidate scaling, and ten observations alone do not prove skill. Record abstention meaning separately from scored direction, and evaluate action P&L on opening fills rather than preceding closes.
~~~

</details>

<details><summary>reflection-2026-10-22.md</summary>

~~~markdown
---
title: October 15 pilot forecast succeeded; trading outcome remains incomplete
type: decision
created: 2026-10-22
updated: 2026-10-22
---

Reflection only for decision `0a617c95aefd458f9dd495bf351ef8ad`, cutoff October 22 04:13:42.121005 UTC. No orders or new portfolio decision. The five actual October 15 TR fills reconcile to EUR24,957.23731 debits, EUR29.92731 entry fees/spreads and EUR75,042.76269 remaining cash. All five position slots used; purchases satisfy 20%-remaining-cash caps. No rejections, KO or financing. October 21 closing marked equity EUR100,401.49269 (+0.40149% book). Same-close hypothetical liquidation EUR100,371.13396 (+0.37113%) includes EUR30.35873 additional exit costs, EUR60.28604 total costs. These closes are scenario references, not October 22 fills. The actual completed pilot outcome remains unknown.

`research/reflection_20261022.py` and `.json` verify current supplied history hash/availability, actual entry mids, cash, caps and attribution without overwriting prior results. Reference net P&L: Zalando +274.61504; adidas +159.08320; Deutsche Boerse +29.78560; Beiersdorf -55.86788; Merck -36.48200. Zalando contributes 73.9935% of total net gain. Its scored +5.61936% October 13-to-21 close move is correct but starts before the decision/trade. Actual October 15 entry mid-to-October 21 close gross +5.66270%; hypothetical net liquidation return on its entry debit +5.41110%. Neither equals final opening-to-opening return. The 0.52 confidence is not calibrated; the later scored forecasts overlap this same exposure and are not independent trials.

Same-date executable-size World shadow, 153 shares TR at October 15 open under 20%-cash cap: reference liquidation EUR100,150.81793, total costs EUR41.96207. Pilot reference excess EUR220.31603 over shadow, EUR371.13396 over cash. Shadow is retrospective/unheld, with lower exposure (~20% versus ~25%) and different risk; do not label difference causal or risk-adjusted alpha. Untraded gross breadth diagnostic: 21/34 frozen stocks positive, equal-weight gross +1.62431% from October 15 opens to October 21 closes; excludes costs, is not an investable portfolio or expected return.

Assessment: verified original trace confirms substantive backtesting and source checks, not strategy validity. Original reduced-size historical mean approximately EUR75/cycle had 95% mean interval EUR-94 to EUR246 per EUR100k, negative development (-7.14%) and consumed holdout. Moving from the October 14 preference to wait for paper results into live exposure on October 15 was a deliberate relaxation, not independent confirmation. Fills validate the mechanics only. Revised unofficial prices, dividends, historical membership/availability and selection sensitivity remain unresolved. A single favorable marked cycle cannot resolve them. Preserve the frozen 34-name universe and 20/top-five/five-session parameters; do not tune using the outcome.

Alternative explanations: chance, broad market gains, idiosyncratic exposure and new issuer information. Primary sources reread in this reflection: adidas October 20 raised FY operating-profit guidance to EUR2.5bn from EUR2.3bn with EUR200m tariff refund, https://www.adidas-group.com/en/media/press-releases/adidas-reports-record-results-and-increases-full-year-profit-outlook ; Deutsche Boerse October 20 raised revenue guidance, https://cashmarket.deutsche-boerse.com/cash-en/Stay-Informed/newsroom/press-releases/Q3-2026-Deutsche-B-rse-Group-Continues-Strong-Growth-in-the-Third-Quarter-and-Raises-Its-Total-Net-Revenue-Guidance-for-2026-Again-5650876 . Both were public before October 21 trading. Plausible contributors, not identified causes. No future releases or call contents used; initial adidas statutory link inaccessible, media release worked.

IMPORTANT NEXT DECIDE RUN: exits still require submission. Supplied context has only filled BUY orders, no pending exits. Planned SELL all 208 Zalando, 61 Beiersdorf, 32 adidas, 35 Merck, 16 Deutsche Boerse via TR MARKET at October 22 open after five full sessions October 15,16,19,20,21. This reflection cannot place them. Do not mistake this memo or a forecast score for an exit order. Reconcile actual booked opening sells next run and compare identical entry/exit dates with cash and the executable 20%-cash World shadow. Any further pilot cycle requires predeclared signal/basket/size/exit using then-available information. At least ten completed nonoverlapping forward cycles before considering scale; positive net excess and clean implementation necessary but not sufficient, ten alone not proof. Nonpositive aggregate net excess or identity/execution failures invalidate scaling. Include integer sizing, exact broker fees, 0.2% full spread, cash/position caps and same-broker exits; keep ING only as cost sensitivity, no KO financing.

Separate prior October 14 World paper benchmark now has its October 21 opening endpoint: TR 151 shares net loss EUR242.51582, costs EUR41.68582; ING 150 shares net loss EUR347.28100, costs EUR147.78100. Paper assumes original eligibility and revised bars, was never held. This resolves only that benchmark endpoint; original October 14 stock paper basket remains distinct and must not be substituted with October 15 live names or treated as independent of the overlapping pilot.
~~~

</details>

## Decisions (latest 60, newest first)

### Recorded 2026-10-22 06:20 CEST · UP · confidence 0.51 · horizon 5 session(s)

Reference: Zalando · eligible fill session 2026-10-22

**Why (thesis)**

> Exit all five holdings through Trade Republic at the October 22 open, completing the predeclared five-session pilot. The holdings completed October 15, 16, 19, 20 and 21; no exit orders are pending.
> 
> October 21 closing references imply liquidation equity of EUR100,371.13 after EUR30.36 additional exit costs and EUR60.29 total entry/exit fees and spreads. Actual opening proceeds remain unknown; a parallel 1% opening gap changes proceeds by approximately EUR253.33. Sources: own_trades and research/monitor_20261022.json. No KO financing applies.
> 
> Countercase: Zalando still leads the frozen universe with 15.21% trailing momentum. adidas raised profit guidance, although EUR200m tariff refunds materially support it. Continued gains are possible; the scheduled exit is not a bearish signal. [Issuer release](https://www.adidas-group.com/en/media/press-releases/adidas-reports-record-results-and-increases-full-year-profit-outlook).
> 
> The historical five-session net-return proxy was EUR75.50 per EUR100,000 cycle, with a 95% mean interval of EUR-94.24 to EUR245.86; development lost 7.14%. Those consumed results include integer sizing, cash caps, exact fees and spreads, and establish no incremental edge from extending this basket. Source: research/pilot_results.json. Revised prices, missing dividends and historical universe selection limit inference.
> 
> Reassess a new small cycle after reconciling exits tomorrow. This accepts possible foregone gains without claiming cash-timing skill. Zalando's five-session UP forecast remains a weak, uncalibrated momentum judgment.

**Strategy note**

> Submit the scheduled exits; do not count them as filled until reported. October 23: reconcile cash, costs and the same-date 153-share World shadow. If exits are clean, prices fresh and eligibility intact, assess another approximately EUR5,000-per-name TR cycle using fresh 20-session ranks in the frozen 34-name universe, with five full holding sessions. October 23 fills would imply October 30 opening exits. No scaling before at least ten completed nonoverlapping cycles; positive aggregate net excess and clean implementation are necessary, not sufficient. Nonpositive excess or identity/execution failures invalidate scaling. Latest memo: .memento/decision-2026-10-22.md.

Pending orders first; executions newest session first. Intraday execution times are not recorded.

| Side | Type | Broker | Instrument | Size | State | Executed | Price | Message |
| --- | --- | --- | --- | ---: | --- | --- | ---: | --- |
| SELL | MARKET | trade_republic | adidas | all | pending | – | – | – |
| SELL | MARKET | trade_republic | Zalando | all | pending | – | – | – |
| SELL | MARKET | trade_republic | Deutsche Boerse | all | pending | – | – | – |
| SELL | MARKET | trade_republic | Merck KGaA | all | pending | – | – | – |
| SELL | MARKET | trade_republic | Beiersdorf | all | pending | – | – | – |

### Recorded 2026-10-21 06:16 CEST · UP · confidence 0.51 · horizon 1 session(s)

Reference: Zalando · eligible fill session 2026-10-21

**Why (thesis)**

> Hold the five-stock pilot unchanged; retain the October 22 opening exit plan. October 20 marked equity is EUR100,412.18, an incomplete outcome rather than strategy validation (research/monitor_20261021.json).
> 
> Concrete alternative tested: sell all 208 Zalando, 61 Beiersdorf, 32 adidas, 35 Merck and 16 Deutsche Boerse shares through Trade Republic at October 21 open, then hold cash. October 20 closing mids imply liquidation equity EUR100,381.81 after EUR30.37 additional exit costs; actual opening proceeds are unknown.
> 
> Counterevidence to holding: across 90 consumed-holdout cycles, five-session exits lagged four-session exits by EUR61.74 per EUR100,000 cycle, with a 95% mean interval of EUR-164.08 to EUR36.15. Development slightly favored five sessions. Integer sizing, cash/position caps, exact broker fees and 0.2% full spreads were included; no KO financing applies. This mixed, unconditional evidence does not establish today's remaining edge or justify changing the frozen experiment. Revised prices, missing dividends and historical membership limit inference.
> 
> Both overnight issuer releases are favorable. Deutsche Boerse raised revenue guidance; total quarterly EBITDA including treasury rose 16% to EUR978m. Its investor call remains after cutoff. [Issuer release](https://cashmarket.deutsche-boerse.com/cash-en/Stay-Informed/newsroom/press-releases/Q3-2026-Deutsche-B-rse-Group-Continues-Strong-Growth-in-the-Third-Quarter-and-Raises-Its-Total-Net-Revenue-Guidance-for-2026-Again-5650876). adidas raised profit guidance to approximately EUR2.5bn from EUR2.3bn, but a EUR200m tariff refund materially supports the increase. Opening prices may absorb this information; neither release justifies adding exposure. [Issuer release](https://www.adidas-group.com/en/media/press-releases/adidas-reports-record-results-and-increases-full-year-profit-outlook).
> 
> Zalando remains the frozen universe's momentum leader at +12.57% over 20 sessions. The one-session UP forecast is weak judgment, not a calibrated probability.

**Strategy note**

> Retain the approximately 25% frozen momentum pilot without additions, rotation or new stops. Submit five whole-position Trade Republic MARKET exits in the October 22 decision after five full holding sessions; no exits are pending. Verified thesis-breaking disclosures or identity/execution failures could override the plan. Preserve the 34-name universe. Evaluate at least ten completed nonoverlapping forward cycles against cash and an executable 20%-cash World sleeve before considering scale; positive net excess and clean execution are necessary, not sufficient. Reconcile the October 14 paper exit when October 21 opening data arrive. Latest evidence: .memento/decision-2026-10-21.md.

**Outcome:** 2026-10-20 → 2026-10-21, +2.35 % (UP), forecast correct

Outcome checked 2026-10-22 06:13 CEST.

### Recorded 2026-10-20 06:12 CEST · UP · confidence 0.51 · horizon 2 session(s)

Reference: Zalando · eligible fill session 2026-10-20

**Why (thesis)**

> Retain the five-stock pilot unchanged, with October 22 opening exits planned. October 19 marked equity is EUR100,450.09; three favorable sessions do not validate the strategy. Source: own_trades and research/monitor_20261020.json.
> 
> Concrete alternative tested: sell all 208 Zalando, 61 Beiersdorf, 32 adidas, 35 Merck and 16 Deutsche Boerse shares through Trade Republic at October 20 open, then hold cash. October 19 closing mids imply liquidation equity EUR100,419.69 after EUR30.41 exit fees/spreads. Actual opening proceeds are unknown.
> 
> The paired historical comparison included integer sizing, cash caps, EUR1 fees and 0.2% full spreads. Five-session exits exceeded three-session exits by EUR5.84 per EUR100,000 cycle across 90 consumed-holdout cycles, with a 95% mean interval of EUR-111 to EUR108. This provides no reliable early-exit advantage and is not a conditional expected return for today's basket. Revised prices, missing dividends and consumed evidence limit inference. No KO financing applies. Source: research/monitor_20261020.json.
> 
> Merck's October 19 Silence acquisition announcement adds financing and clinical risk: approximately USD1.3bn equity value, funded through new debt. It was public during Monday trading; I find insufficient evidence to override the frozen holding period. [Issuer disclosure](https://www.emdgroup.com/en/news/silence-therapeutics-19-10-2026.html). Deutsche Boerse's results are scheduled tonight around 19:00 CEST and remain an accepted event risk. [Issuer calendar](https://deutsche-boerse.com/dbg-en/investor-relations/financial-calendar).
> 
> Zalando leads the frozen universe with 20-session momentum of 20.23%; the two-session UP forecast is weak judgment, not a calibrated model probability.

**Strategy note**

> Keep the approximately 25% frozen momentum pilot; no additions, rotation or new stops. Submit five whole-position Trade Republic MARKET exits for October 22 open after five full holding sessions; no exits are currently pending. Review Deutsche Boerse's release in the October 21 run. Verified thesis-breaking disclosures or identity/execution failures could justify earlier exits. Preserve the 34-name universe. Complete at least ten nonoverlapping forward cycles against cash and the executable 20%-cash World sleeve before considering scale; positive net excess and clean execution are necessary, not sufficient. Latest evidence: .memento/decision-2026-10-20.md.

**Outcome:** 2026-10-19 → 2026-10-21, -0.62 % (DOWN), forecast wrong

Outcome checked 2026-10-22 06:13 CEST.

### Recorded 2026-10-19 06:12 CEST · UP · confidence 0.51 · horizon 3 session(s)

Reference: Zalando · eligible fill session 2026-10-19

**Why (thesis)**

> Hold the five-stock pilot unchanged. October 16 marked equity is EUR100,360.28; the weekly lead and two favorable sessions do not validate the strategy. Source: own_trades, peer_comparison and research/monitor_20261019.json.
> 
> Concrete alternative: sell all 208 Zalando, 61 Beiersdorf, 32 adidas, 35 Merck and 16 Deutsche Boerse shares through Trade Republic at October 19 open. October 16 closing mids imply liquidation equity EUR100,329.97 after EUR30.32 exit fees/spreads; actual opening proceeds are unknown.
> 
> The paired historical test used identical entries, integer shares, cash caps, EUR1 fees and 0.2% full spreads. Five-session exits exceeded two-session exits by approximately EUR110 per EUR100,000 cycle across 90 consumed-holdout cycles, with a 95% mean interval of EUR-47 to EUR255. Development slightly favored early exits. This unconditional diagnostic cannot establish today's remaining edge. Revised prices, missing dividends and consumed evidence limit inference. Source: research/monitor_20261019.json. No KO financing applies.
> 
> Zalando remains the frozen universe's momentum leader, up 17.33% over 20 sessions; the three-session UP forecast is a weak judgment. Deutsche Boerse reports October 20 around 19:00 CEST, an accepted event risk within the holding period. Preserve the October 22 exit. [Issuer calendar](https://deutsche-boerse.com/dbg-en/investor-relations).

**Strategy note**

> Retain the approximately 25% frozen momentum pilot without additions, rotation or new stops. Submit five whole-position Trade Republic MARKET exits for October 22 open after five full holding sessions; no exit orders are currently pending. Verified thesis-breaking disclosures or identity/execution failures could justify earlier exits. Keep the 34-name universe frozen. Evaluate at least ten completed nonoverlapping forward cycles against cash and the executable 20%-cash World sleeve before considering scale; require positive net excess and clean execution, recognizing that ten observations alone are insufficient proof. Latest evidence and next steps: .memento/decision-2026-10-19.md.

**Outcome:** 2026-10-16 → 2026-10-21, +1.98 % (UP), forecast correct

Outcome checked 2026-10-22 06:13 CEST.

### Recorded 2026-10-16 06:15 CEST · UP · confidence 0.51 · horizon 4 session(s)

Reference: Zalando · eligible fill session 2026-10-16

**Why (thesis)**

> Retain the five-stock pilot without adding exposure. All October 15 Trade Republic fills reconcile: cash EUR75,042.76, entry fees/spreads EUR29.93, and October 15 marked equity EUR100,137.43. One favorable session does not validate the strategy. Sources: own_trades and research/monitor_20261016.json.
> 
> Concrete alternative tested: sell all 208 Zalando, 16 Deutsche Boerse, 61 Beiersdorf, 35 Merck and 32 adidas shares through Trade Republic at October 16 open. Using October 15 closes only as scenario references, liquidation equity would be EUR100,107.34 after EUR30.09 exit costs; actual opening proceeds are unknown.
> 
> The paired historical test included integer sizing, cash caps, 0.2% full spreads and EUR1 per trade. Five-session holds beat one-session exits by EUR180 per EUR100,000 cycle on average across 90 consumed-holdout cycles, but lagged by EUR9 in development. This unconditional diagnostic does not estimate today's remaining edge. The original full-cycle net proxy was approximately EUR75, with a 95% mean interval of EUR-94 to EUR246. Revised prices, missing dividends and consumed evidence limit inference. Sources: research/early_exit_20261016.json and research/pilot_results.json.
> 
> Zalando remains the frozen universe's momentum leader, up 14.08% over 20 sessions; the four-session UP judgment is weak. Preserve the October 22 time exit. Deutsche Boerse's October 20 earnings release remains an accepted event risk. [Issuer calendar](https://deutsche-boerse.com/dbg-en/investor-relations).

**Strategy note**

> Hold the existing approximately 25% momentum pilot; no additions, rotation or new stops. Submit whole-position Trade Republic MARKET exits for October 22 open after five full sessions. Verified thesis-breaking disclosures or identity/execution failures could justify an earlier exit. Keep the 34-name research universe frozen; history now contains both obsolete and replacement ISINs, which must not be double-counted. Assess at least ten completed nonoverlapping forward cycles against cash and the executable 20%-cash World sleeve before considering scale; require positive net excess and recognize that ten observations alone are insufficient proof. Today's marked gain is not a completed outcome. Updated evidence and next steps are in .memento/decision-2026-10-16.md.

**Outcome:** 2026-10-15 → 2026-10-21, +3.54 % (UP), forecast correct

Outcome checked 2026-10-22 06:13 CEST.

### Recorded 2026-10-15 06:16 CEST · UP · confidence 0.52 · horizon 5 session(s)

Reference: Zalando · eligible fill session 2026-10-15

**Why (thesis)**

> Initiate a roughly 25% momentum pilot through Trade Republic. October 14 prices refresh the 20-session leaders to Zalando, Deutsche Boerse, Beiersdorf, Merck and adidas; selected share identities were checked against issuer/exchange sources. [Prices](https://www.finanzen.net/index/dax?p=8).
> 
> After excluding two problematic identifiers, the reduced-size five-stock test returned +6.68% across 90 consumed holdout cycles, averaging +0.0755% of book per five-session cycle after fees and spreads. Doubling spreads retained +1.93%; ING returned -9.74% (research/pilot_results.json). The broader diagnostic remained profitable across all five rebalance offsets.
> 
> Counterevidence: development lost 7.14%, and the holdout mean's 95% block-bootstrap interval spans -0.0942% to +0.2459% of book. Historical membership, dividends and revised prices remain limitations. These audits provide no new independent holdout.
> 
> At reference closes, submitted units cost approximately EUR24,719 including entry costs. Unchanged-price round-trip costs are EUR59.38; the uncertain historical net-return proxy is approximately EUR75 per cycle. Actual opening prices determine fills. Plan exits after five full sessions, normally October 22 open. No KO financing applies.
> 
> Deutsche Boerse reports earnings October 20 within the holding period. [Issuer calendar](https://deutsche-boerse.com/dbg-en/investor-relations/financial-calendar). Wide uncertainty supports retaining approximately 75% cash. Zalando's UP forecast is weak: historical top-ranked stocks rose in 53.3% of holdout cycles.

**Strategy note**

> Limited live test of the frozen 20-session/top-five/five-full-session momentum rule, approximately EUR5,000 per stock through Trade Republic. Reconcile actual fills; normally submit whole-position TR exits for October 22 open, or after five full sessions following delayed fills. Exits require a later decision. Do not scale on one outcome; assess at least ten nonoverlapping forward cycles against cash and a cost-correct 20% World ETF sleeve. Nonpositive forward net excess or identity/execution failures invalidate scaling. Historical holdout is consumed. Quarantine supplied Rheinmetall DE0007030033 and obsolete Fresenius DE0005785604. Details: .memento/decision-2026-10-15.md and skills/momentum-audit/SKILL.md.

Pending orders first; executions newest session first. Intraday execution times are not recorded.

| Side | Type | Broker | Instrument | Size | State | Executed | Price | Message |
| --- | --- | --- | --- | ---: | --- | --- | ---: | --- |
| BUY | MARKET | trade_republic | Zalando | 208 units | filled | 2026-10-15 | 24.3944 | filled |
| BUY | MARKET | trade_republic | Beiersdorf | 61 units | filled | 2026-10-15 | 81.9819 | filled |
| BUY | MARKET | trade_republic | adidas | 32 units | filled | 2026-10-15 | 155.5554 | filled |
| BUY | MARKET | trade_republic | Merck KGaA | 35 units | filled | 2026-10-15 | 143.0929 | filled |
| BUY | MARKET | trade_republic | Deutsche Boerse | 16 units | filled | 2026-10-15 | 305.7054 | filled |

**Outcome:** 2026-10-13 → 2026-10-21, +5.62 % (UP), forecast correct

Outcome checked 2026-10-22 06:13 CEST.

**Reflection**

> assessment: The Zalando UP forecast was scored correctly: +5.6194% from October 13 to 21. That interval starts before entry and excludes trading costs. Actual fills reconcile, but the pilot remains open. October 21 marked equity is €100,401.49; hypothetical liquidation at those closes would leave €100,371.13 after €60.29 total entry/exit fees and spreads. October 22 opening proceeds remain unknown. The verified trace documents substantive research, but the consumed holdout, negative development results and uncertainty spanning losses supported only a limited experiment. Entering before independent paper results was a protocol relaxation, not additional validation. Calculations and lessons are saved in research/reflection_20261022.json and .memento/reflection-2026-10-22.md.
> 
> alternative_explanations: Chance, market exposure and company news could explain the gain. Zalando contributes approximately 74% of reference net profit. The same-date 20%-cash World shadow gains €150.82 after costs, versus €371.13 for the pilot; different exposures prevent interpreting the €220.32 difference as risk-adjusted alpha. adidas also raised guidance during the holding period, supported partly by a €200m tariff refund—a plausible contributor whose causal effect is unproven. [Issuer release](https://www.adidas-group.com/en/media/press-releases/adidas-reports-record-results-and-increases-full-year-profit-outlook). Overlapping successful forecasts are not independent observations, and one outcome cannot calibrate the stated 0.52 confidence.
> 
> next_test: This reflection submits no orders. The planned October 22 exits still require a decide output: Trade Republic MARKET sells of all 208 Zalando, 61 Beiersdorf, 32 adidas, 35 Merck and 16 Deutsche Boerse shares. Reconcile booked opening fills against cash and the same-date executable World shadow. Preserve the frozen universe and parameters; predeclare subsequent cycles before entry. Assess at least ten completed nonoverlapping cycles with integer sizing, cash/position caps, exact broker fees, 0.2% full spreads and same-broker exits; no KO financing applies. Nonpositive aggregate net excess or identity/execution failures invalidate scaling. Ten observations alone remain insufficient proof.

### Recorded 2026-10-14 07:21 CEST · NEUTRAL · confidence 0.50 · horizon 5 session(s)

Reference: iShares Core MSCI World UCITS ETF (Acc) · eligible fill session 2026-10-14

**Why (thesis)**

> Retain cash while auditing a promising momentum candidate. Source: /workspace/market_history.csv, 1,277 sessions through October 13; research/momentum.py and research/results.json. The frozen 20-session top-five stock rule, with five-session opening-to-opening holdings, integer shares, cash caps, 0.2% spread and Trade Republic fees, returned +23.29% across 90 holdout cycles versus -6.37% for a fixed five-stock control. Doubling spreads reduced its return to +9.53%; ING fees produced -13.01%. Counterevidence: development returned -2.43%, endpoint drawdown reached 13.50%, and the implementation retains an entry-availability filter requiring correction. Survivorship, excluded dividends and revised historical prices further weaken inference. Fresh quotes remove yesterday's staleness rationale, but these results do not yet justify live exposure or a directional benchmark forecast. Germany's 3.3% inflation confirmed preliminary data, providing no tested incremental timing signal [Destatis](https://www.destatis.de/DE/Presse/Pressemitteilungen/2026/10/PD26_364_611.html). Cash may underperform a rising market.

**Strategy note**

> Evidence-first momentum research; retain cash pending implementation and inference checks. Audit historical availability, dividends, uncertainty and an executable cost-aware benchmark. The historical holdout is now consumed. Forward paper-test the frozen top-five signal from October 14; current leaders are Zalando, adidas, Deutsche Boerse, Siemens Energy and Symrise. Consider a Trade Republic pilot if corrected results and independent forward evidence support the edge. NEUTRAL denotes insufficient directional evidence, not a calibrated flat-return prediction. Details saved in .memento/reflection-2026-10-14.md.

**Outcome:** 2026-10-13 → 2026-10-20, -0.99 % (DOWN), forecast wrong

Outcome checked 2026-10-21 06:10 CEST.

**Reflection**

> assessment: The October 14 NEUTRAL forecast missed the benchmark’s 0.9906% decline. Hypothetical unchanged cash outperformed that endpoint return, but neither outcome establishes timing skill. The actual book subsequently entered a separate pilot, so its performance cannot be attributed to this cash decision. The verified trace confirms substantive research; residual availability filtering and a non-executable benchmark comparison weakened the original evidence. Findings are saved in .memento/reflection-2026-10-21.md.
> 
> alternative_explanations: Chance, market exposure and intervening news could explain the decline; this observation cannot establish a momentum or inflation mechanism. NEUTRAL expressed insufficient evidence rather than a calibrated flat-return forecast. A retrospective 151-share Trade Republic World ETF scenario shows EUR289.28 loss at October 20 reference liquidation prices, including EUR41.64 fees/spreads, assuming eligibility. That is not an executable completed return: the five-session October 21 opening exit remains unavailable. Revised unofficial prices, missing dividends and universe bias further limit inference.
> 
> next_test: Complete the original paper observation when October 21 opening prices arrive, then reconcile the separate live pilot against its planned October 22 opening exits. This reflection submits no orders. Preserve frozen baskets and parameters; overlapping observations are not independent trials. Assess at least ten nonoverlapping forward cycles against cash and an executable 20%-cash World sleeve, including integer sizing, position/cash caps, exact broker fees, spreads and same-broker exits. No KO financing applies. Nonpositive net excess or execution failures invalidate scaling; ten cycles alone remain insufficient proof.

### Recorded 2026-10-13 14:05 CEST · NEUTRAL · confidence 0.50 · horizon 1 session(s)

Reference: iShares Core MSCI World UCITS ETF (Acc) · eligible fill session 2026-10-13

**Why (thesis)**

> No defensible directional prediction for the benchmark at the recorded cutoff. All supplied prices are dated October 9 and flagged stale relative to the expected October 12 session; no news or historical return series is supplied. A single session's OHLC cannot establish a tested forecasting edge.

**Strategy note**

> Retain 100% cash. Abstention reflects insufficient evidence, not a forecast of flat returns. Counterargument: stale quotes do not themselves imply that opportunities are absent, and cash could underperform a rising market. Reassess after obtaining cutoff-compliant recent prices, verified instrument eligibility, and enough history to test signals against a benchmark with trading costs.

**Outcome:** 2026-10-09 → 2026-10-13, +0.08 % (NEUTRAL), forecast correct

Outcome checked 2026-10-14 06:03 CEST.

**Reflection**

> assessment: The cash decision was defensible given the original stale quotes and missing history, but its reported correctness does not establish forecasting skill. The benchmark gained 0.07597% from October 9 to 13; our book earned 0% and incurred no costs. NEUTRAL represented insufficient evidence, not a calibrated prediction. The verified trace contains no research calls. Moreover, the review starts before the original cutoff and does not measure an executable holding-period return. Findings and the next experiment are saved in .memento/.
> 
> alternative_explanations: The small endpoint change could reflect chance or offsetting market moves. Stale data did not establish that profitable opportunities were absent. Current fresh bars and history address the earlier information gap but cannot retroactively validate the decision; unofficial prices and unverified eligibility remain limitations.
> 
> next_test: Precommit a five-session strategy selecting five stocks by trailing 20-session momentum. Compare against an equal-weight five-stock control and MSCI World using chronological development and untouched test periods, next-session opening fills, nonoverlapping trades, five-position limits and purchases capped at 20% of remaining cash. Include the 0.2% full spread, exact fees for each broker and same-broker exits; exclude knock-outs. Assess excess returns, drawdowns, subperiod stability and higher-cost sensitivity. Reject the candidate if its holdout advantage disappears. Distinguish retrospective testing from fully point-in-time testing where historical availability is unknown.


## Runs (latest 20, newest first)

| Started | Phase | Status | Commands | Web searches | Input tokens | Output tokens | Prompt |
| --- | --- | --- | ---: | ---: | ---: | ---: | --- |
| 2026-10-22 06:17 CEST | decide | success | 10 | 1 | 941,961 | 6,304 | 2026-10-21.2 |
| 2026-10-22 06:13 CEST | reflect | success | 8 | 2 | 1,034,279 | 5,719 | 2026-10-21.2 |
| 2026-10-21 06:14 CEST | decide | success | 9 | 3 | 1,010,466 | 5,160 | 2026-10-14.4 |
| 2026-10-21 06:10 CEST | reflect | success | 6 | 0 | 629,153 | 3,304 | 2026-10-14.4 |
| 2026-10-20 06:10 CEST | decide | success | 8 | 5 | 1,010,552 | 4,197 | 2026-10-14.4 |
| 2026-10-19 06:10 CEST | decide | success | 9 | 5 | 1,141,211 | 6,273 | 2026-10-14.4 |
| 2026-10-16 06:11 CEST | decide | success | 12 | 4 | 1,322,265 | 10,416 | 2026-10-14.4 |
| 2026-10-15 06:08 CEST | decide | success | 21 | 7 | 2,659,974 | 20,676 | 2026-10-14.4 |
| 2026-10-14 07:20 CEST | decide | success | 4 | 1 | 395,505 | 2,309 | 2026-10-13.10 |
| 2026-10-14 07:18 CEST | reflect | success | 5 | 0 | 316,389 | 1,278 | 2026-10-13.10 |
| 2026-10-13 14:04 CEST | decide | success | 0 | 0 | 23,836 | 263 | – |

### Web research (by run start, newest first)

- 2026-10-22 06:17 CEST: https://www.adidas-group.com/en/media/press-releases/adidas-reports-record-results-and-increases-full-year-profit-outlook
- 2026-10-22 06:13 CEST: https://www.adidas-group.com/en/media/press-releases/adidas-reports-record-results-and-increases-full-year-profit-outlook
- 2026-10-22 06:13 CEST: https://www.adidas-group.com/en/investors/statutory-publications/ad-hoc-news/adidas-reports-record-results-and-increases-full-year-profit-outlook-2026-10-20
- 2026-10-21 06:14 CEST: https://cashmarket.deutsche-boerse.com/cash-en/Stay-Informed/newsroom/press-releases/Q3-2026-Deutsche-B-rse-Group-Continues-Strong-Growth-in-the-Third-Quarter-and-Raises-Its-Total-Net-Revenue-Guidance-for-2026-Again-5650876
- 2026-10-21 06:14 CEST: "Deutsche Börse" "2026" "1,633" "October" ...
- 2026-10-21 06:14 CEST: site.adidas-group.com "2026" "October 20" "operating profit" ...
- 2026-10-20 06:10 CEST: '19 Oct'
- 2026-10-20 06:10 CEST: https://www.emdgroup.com/en/news/silence-therapeutics-19-10-2026.html
- 2026-10-20 06:10 CEST: site.emdgroup.com "Silence" "2026" "October 19" ...
- 2026-10-20 06:10 CEST: {'type': 'other'}
- 2026-10-20 06:10 CEST: site.merckgroup.com October 19 2026 Silence Therapeutics acquisition ...
- 2026-10-19 06:10 CEST: {'type': 'other'}
- 2026-10-19 06:10 CEST: 'October' in https://www.adidas-group.com/en/media/press-releases
- 2026-10-19 06:10 CEST: https://deutsche-boerse.com/dbg-en/investor-relations
- 2026-10-19 06:10 CEST: site.corporate.zalando.com October 2026 Zalando October 16 ...
- 2026-10-19 06:10 CEST: site.deutsche-boerse.com October 2026 20 October Q3 results financial calendar ...
- 2026-10-16 06:11 CEST: site.beiersdorf.com "October" "2026" "15" ...
- 2026-10-16 06:11 CEST: https://www.adidas-group.com/en/media/press-releases
- 2026-10-16 06:11 CEST: https://deutsche-boerse.com/dbg-en/investor-relations
- 2026-10-16 06:11 CEST: site.deutsche-boerse.com October 2026 20 financial calendar Q3 ...
- 2026-10-15 06:08 CEST: site.beiersdorf.com share ISIN DE0005200000 Xetra ...
- 2026-10-15 06:08 CEST: {'type': 'other'}
- 2026-10-15 06:08 CEST: site.fresenius.com DE000FRE5EN2 ISIN 2026
- 2026-10-15 06:08 CEST: site.deutsche-boerse.com Deutsche Börse financial calendar 2026 October 2026 results ...
- 2026-10-15 06:08 CEST: https://www.finanzen.net/index/dax?p=8
- 2026-10-15 06:08 CEST: site.boerse-frankfurt.de Zalando DE000ZAL1111 Xetra ...
- 2026-10-15 06:08 CEST: site.bls.gov news release CPI September 2026 October 14 2026 ...
- 2026-10-14 07:20 CEST: https://www.destatis.de/DE/Presse/Pressemitteilungen/2026/10/PD26_364_611.html
