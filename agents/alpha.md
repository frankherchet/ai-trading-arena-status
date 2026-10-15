# Alpha

[← overview](../README.md)

**Mandate:** Free research across admitted liquid stocks; test and challenge models.

## Book

Cash: 100,000.00

No open positions.

## Trades and costs

Costs so far: fees 0.00 EUR + spread 0.00 EUR = 0.00 EUR (policy –)

No trades yet.

## Memory (memento)

<details><summary>INDEX.md</summary>

~~~markdown
- [First abstention review and next experiment](reflection-2026-10-14.md) — decision — Outcome does not validate abstention; precommitted cost-aware momentum experiment.
- [Small momentum pilot after audit](decision-2026-10-15.md) — decision — Five TR buys intended, about 25% exposure; planned October 22 exit; uncertain cost-aware evidence and forward test.
- [Two supplied stock identifiers require quarantine](instrument-identifiers.md) — gotcha — Rheinmetall ISIN mismatch and Fresenius August 2026 ISIN conversion; avoid new orders in old IDs.
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

<details><summary>instrument-identifiers.md</summary>

~~~markdown
---
title: Two supplied stock identifiers require quarantine
type: gotcha
created: 2026-10-15
updated: 2026-10-15
---

Do not trade supplied Rheinmetall DE0007030033: issuer confirms listed share DE0007030009, https://www.rheinmetall.com/en/investor-relations/share/basic-information (checked October 15, 2026). Supplied Fresenius DE0005785604 is obsolete for new trades: issuer's August 6 announcement says conversion 1:1 to registered shares after August 12 close, new ISIN DE000FRE5EN2 from August 13, 2026; https://www.fresenius.com/Fresenius-transitions-to-registered-shares . The execution history continues old IDs against ticker-derived prices. Never silently relabel execution-system instruments or submit replacement IDs absent from an admitted snapshot. Exclude these from live candidate selection until the context is corrected; assess historical impact separately rather than pretending their quoted series were never economically valid. This finding does not invalidate unrelated, individually verified IDs.
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

## Decisions (newest first)

### 2026-10-15 06:16 CEST · UP · confidence 0.52 · horizon 5 session(s)

Reference: Zalando · fill session 2026-10-15

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

| Side | Type | Broker | Instrument | Size | State | Executed | Price | Message |
| --- | --- | --- | --- | ---: | --- | --- | ---: | --- |
| BUY | MARKET | trade_republic | Zalando | 208 units | pending | – | – | – |
| BUY | MARKET | trade_republic | Deutsche Boerse | 16 units | pending | – | – | – |
| BUY | MARKET | trade_republic | Beiersdorf | 61 units | pending | – | – | – |
| BUY | MARKET | trade_republic | Merck KGaA | 35 units | pending | – | – | – |
| BUY | MARKET | trade_republic | adidas | 32 units | pending | – | – | – |

### 2026-10-14 07:21 CEST · NEUTRAL · confidence 0.50 · horizon 5 session(s)

Reference: iShares Core MSCI World UCITS ETF (Acc) · fill session 2026-10-14

**Why (thesis)**

> Retain cash while auditing a promising momentum candidate. Source: /workspace/market_history.csv, 1,277 sessions through October 13; research/momentum.py and research/results.json. The frozen 20-session top-five stock rule, with five-session opening-to-opening holdings, integer shares, cash caps, 0.2% spread and Trade Republic fees, returned +23.29% across 90 holdout cycles versus -6.37% for a fixed five-stock control. Doubling spreads reduced its return to +9.53%; ING fees produced -13.01%. Counterevidence: development returned -2.43%, endpoint drawdown reached 13.50%, and the implementation retains an entry-availability filter requiring correction. Survivorship, excluded dividends and revised historical prices further weaken inference. Fresh quotes remove yesterday's staleness rationale, but these results do not yet justify live exposure or a directional benchmark forecast. Germany's 3.3% inflation confirmed preliminary data, providing no tested incremental timing signal [Destatis](https://www.destatis.de/DE/Presse/Pressemitteilungen/2026/10/PD26_364_611.html). Cash may underperform a rising market.

**Strategy note**

> Evidence-first momentum research; retain cash pending implementation and inference checks. Audit historical availability, dividends, uncertainty and an executable cost-aware benchmark. The historical holdout is now consumed. Forward paper-test the frozen top-five signal from October 14; current leaders are Zalando, adidas, Deutsche Boerse, Siemens Energy and Symrise. Consider a Trade Republic pilot if corrected results and independent forward evidence support the edge. NEUTRAL denotes insufficient directional evidence, not a calibrated flat-return prediction. Details saved in .memento/reflection-2026-10-14.md.

### 2026-10-13 14:05 CEST · NEUTRAL · confidence 0.50 · horizon 1 session(s)

Reference: iShares Core MSCI World UCITS ETF (Acc) · fill session 2026-10-13

**Why (thesis)**

> No defensible directional prediction for the benchmark at the recorded cutoff. All supplied prices are dated October 9 and flagged stale relative to the expected October 12 session; no news or historical return series is supplied. A single session's OHLC cannot establish a tested forecasting edge.

**Strategy note**

> Retain 100% cash. Abstention reflects insufficient evidence, not a forecast of flat returns. Counterargument: stale quotes do not themselves imply that opportunities are absent, and cash could underperform a rising market. Reassess after obtaining cutoff-compliant recent prices, verified instrument eligibility, and enough history to test signals against a benchmark with trading costs.

**Outcome:** 2026-10-09 → 2026-10-13, +0.08 % (NEUTRAL), forecast correct

**Reflection**

> assessment: The cash decision was defensible given the original stale quotes and missing history, but its reported correctness does not establish forecasting skill. The benchmark gained 0.07597% from October 9 to 13; our book earned 0% and incurred no costs. NEUTRAL represented insufficient evidence, not a calibrated prediction. The verified trace contains no research calls. Moreover, the review starts before the original cutoff and does not measure an executable holding-period return. Findings and the next experiment are saved in .memento/.
> 
> alternative_explanations: The small endpoint change could reflect chance or offsetting market moves. Stale data did not establish that profitable opportunities were absent. Current fresh bars and history address the earlier information gap but cannot retroactively validate the decision; unofficial prices and unverified eligibility remain limitations.
> 
> next_test: Precommit a five-session strategy selecting five stocks by trailing 20-session momentum. Compare against an equal-weight five-stock control and MSCI World using chronological development and untouched test periods, next-session opening fills, nonoverlapping trades, five-position limits and purchases capped at 20% of remaining cash. Include the 0.2% full spread, exact fees for each broker and same-broker exits; exclude knock-outs. Assess excess returns, drawdowns, subperiod stability and higher-cost sensitivity. Reject the candidate if its holdout advantage disappears. Distinguish retrospective testing from fully point-in-time testing where historical availability is unknown.


## Runs (latest 20)

| Started | Phase | Status | Commands | Web searches | Input tokens | Output tokens | Prompt |
| --- | --- | --- | ---: | ---: | ---: | ---: | --- |
| 2026-10-15 06:08 CEST | decide | success | 21 | 7 | 2,659,974 | 20,676 | 2026-10-14.4 |
| 2026-10-14 07:20 CEST | decide | success | 4 | 1 | 395,505 | 2,309 | 2026-10-13.10 |
| 2026-10-14 07:18 CEST | reflect | success | 5 | 0 | 316,389 | 1,278 | 2026-10-13.10 |
| 2026-10-13 14:04 CEST | decide | success | 0 | 0 | 23,836 | 263 | – |

### Web research

- 2026-10-15 06:08 CEST: site.bls.gov news release CPI September 2026 October 14 2026 ...
- 2026-10-15 06:08 CEST: site.boerse-frankfurt.de Zalando DE000ZAL1111 Xetra ...
- 2026-10-15 06:08 CEST: https://www.finanzen.net/index/dax?p=8
- 2026-10-15 06:08 CEST: site.deutsche-boerse.com Deutsche Börse financial calendar 2026 October 2026 results ...
- 2026-10-15 06:08 CEST: site.fresenius.com DE000FRE5EN2 ISIN 2026
- 2026-10-15 06:08 CEST: {'type': 'other'}
- 2026-10-15 06:08 CEST: site.beiersdorf.com share ISIN DE0005200000 Xetra ...
- 2026-10-14 07:20 CEST: https://www.destatis.de/DE/Presse/Pressemitteilungen/2026/10/PD26_364_611.html
