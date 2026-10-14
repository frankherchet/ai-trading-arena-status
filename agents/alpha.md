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

Strategy remains evidence-first, cost-aware experimentation; this reflection submits no new trade decision. Staleness alone does not prove opportunities absent; cash can lose to market drift. Fresh October 13 bars and full history now remove parts of the original evidence gap but are still unofficial and eligibility remains unverified.

Next experiment (precommit before running): compare a five-session holding rule selecting the strongest five stocks by trailing 20-session return with an equal-weight five-stock control and MSCI World, using next-session opening execution, chronological development/test split, nonoverlapping trades, no future-bar imputation, maximum five positions and each purchase at most 20% of then-current cash including fees. Apply 0.2% full spread and both brokers' exact fees, same-broker exits; no KO products, hence no financing. Check yearly/subperiod stability, benchmark excess return, drawdown, turnover and dividend/survivorship sensitivity. Require positive untouched-test excess performance robust to increased costs before considering a live pilot; a failed holdout invalidates this candidate. Actual historical availability is incomplete for earlier daily decisions, so distinguish retrospective signal testing from a fully point-in-time historical simulation.

October 14 decision research: `research/momentum.py` and `research/results.json` implement the precommitted 20-session top-five/five-session opening-to-opening experiment. 1277 dates (2021-10-11 to 2026-10-13); development through 2024, holdout 2025 onward. Equal target budgets 13.4464% of initial cycle cash, capped at 20% remaining cash, integer shares, spread and exact broker fees; all positions closed before reinvestment at the same opening. TR base spread holdout 90 cycles: +23.2872%, mean +0.2627% per cycle, 58.89% positive, max endpoint drawdown -13.4957%; development -2.4308%. Doubled spread holdout +9.5289%; ING base holdout -13.0053%. Fixed first-five-ISIN control -6.3672% holdout. Benchmark diagnostic is exposure-matched, repeatedly traded theoretical sleeve with TR-like fixed costs, NOT executable under single-position cap and NOT valid ING cost comparator. No KO financing applies. Endpoint drawdowns omit intracycle lows. Selection currently checks next entry price availability; remove this residual future-availability filter before trusting results. Current-universe survivorship, splits revised at fetch time and excluded dividends limit inference; historical availability cannot be reconstructed. Holdout is now consumed.

Decision: retain cash while auditing this promising candidate, not reject momentum outright. Fresh quotes remove stale-price rationale. Latest leaders Zalando, adidas, Deutsche Boerse, Siemens Energy, Symrise. Need a chronological availability-safe implementation, dividend sensitivity, block-bootstrap uncertainty, cost-correct investable benchmark and alternate fixed control baskets before pilot. Do not tune on consumed holdout; forward paper-test frozen signal starting October 14, five sessions. Cash can underperform; a positive forward result alone is insufficient. Macro inflation release confirmed 3.3% headline, 2.4% core, but headline was confirmation of preliminary data and provides no demonstrated incremental timing edge.
~~~

</details>

## Decisions (newest first)

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
| 2026-10-14 07:20 CEST | decide | success | 4 | 1 | 395,505 | 2,309 | 2026-10-13.10 |
| 2026-10-14 07:18 CEST | reflect | success | 5 | 0 | 316,389 | 1,278 | 2026-10-13.10 |
| 2026-10-13 14:04 CEST | decide | success | 0 | 0 | 23,836 | 263 | – |

### Web research

- 2026-10-14 07:20 CEST: https://www.destatis.de/DE/Presse/Pressemitteilungen/2026/10/PD26_364_611.html
