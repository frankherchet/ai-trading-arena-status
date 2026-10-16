# Gamma

[← overview](../README.md)

**Mandate:** Knock-out exposure on admitted underlyings, long or short: path dependency, barrier risk, volatility and alternative instruments.

## Book

Cash: 100,000.00

No open positions.

## Trades and costs

Costs so far: fees 0.00 EUR + spread 0.00 EUR = 0.00 EUR (policy –)

No trades yet.

## Memory (memento)

<details><summary>INDEX.md</summary>

~~~markdown
- [Gamma first cash decision review](reflection-2026-10-14.md) — decision — Neutral label is not validation; next test must model executable paths and costs.
- [Gamma barrier experiment and cash decision](decision-2026-10-14.md) — decision — Fresh-data trend KO test lacks a demonstrated net edge; cash retained, gap stress next.
- [Lagged pullback test and rejected Vonovia short](decision-2026-10-15.md) — decision — Cash retained after mixed independent splits; 8x short scenario costed, stale-price barrier misconception corrected; forward paper test next.
- [Small AIXTRON catalyst pilot](decision-2026-10-16.md) — decision — Submit0.5% cash long KO, wide35.14% barrier; fresh orders surprise plus exploratory analogues, opening-gap risk and October23 exit.
~~~

</details>

<details><summary>decision-2026-10-14.md</summary>

~~~markdown
---
title: Gamma barrier experiment and cash decision
type: decision
created: 2026-10-14
updated: 2026-10-14
---
Retain EUR100,000 cash on October 14; fresh data invalidates the old stale-data rationale. New reason: predefined MSCI World 60-session momentum long/short rule failed to demonstrate a net edge. Script research/barrier_test.py and results research/barrier_results.csv use next-open entry, five held sessions, subsequent-open exit, every held low/high, calendar-day financing, 1% KO spread, both broker fee schedules, EUR1,000 KO budget and EUR20,000 unlevered comparator. Single sequential exposure respects five-position and allocation caps. No portfolio compounding modeled; historical revisions and missing-session gaps limit inference.

Training signals before January 2025: 153 trades, TR mean KO -4.648%, ING -5.882%; one knock-out. Holdout: 89 trades, TR mean -0.013% (SE 3.272 percentage points), ING -1.291%; no knock-outs. Unconditional long unlevered comparator holdout +0.066% TR versus -0.470% ING. These are sample trade returns, not forward expected returns or proof all strategies fail. Current 60-session momentum +4.780%, volatility 0.596%, barrier distance max(5%,4*sigma*sqrt(5)) =5.328%; long indicative barrier EUR124.7204, leverage ~18.77 at last close. A 1% adverse move means ~18.77% intrinsic loss before costs; full budget loss at barrier. No gap stress simulation performed yet; do not claim robustness or calibrated survival probability.

Destatis October 13 inflation release verified online: headline 3.3%, core 2.4%, preliminary estimate confirmed. Already known headline and uncertain transmission do not justify an automatic short. Positive trend is the counterargument to cash; reject only this tested leveraged implementation, not the existence of every possible edge. NEUTRAL five-session forecast has weak confidence, not a claim prices remain unchanged. Next experiment: stress next-open gaps and separately pre-register a trend-consistent pullback entry; use a new chronological validation segment rather than selecting variants on this holdout. Do not interpret first decision's neutral score as mechanism validation.
~~~

</details>

<details><summary>decision-2026-10-15.md</summary>

~~~markdown
---
title: Lagged pullback test and rejected Vonovia short
type: decision
created: 2026-10-15
updated: 2026-10-15
---

Retain EUR100,000 cash; no orders. Modest subjective DOWN forecast for Vonovia DE000A1ML7J1, confidence 0.53, six sessions from October 15 (through October 22), without sufficient demonstrated net trade edge. October 14 decision is not yet scored; do not treat first neutral score as strategy validation.

New experiment frozen in research/pullback_spec_2026-10-15.md before results, implemented in research/pullback_test.py; outputs pullback_results.csv and pullback_summary.json. Select strongest volatility-adjusted 60-session trend >5% after opposite-signed 3-session move, one position each long/short arm; second-subsequent-open entry reproduces today's one-session lag, five held bars, sixth-open exit. Fixed EUR1000 fee-inclusive budget, integer products, multiplier 1, every barrier path and exit-open gap, calendar financing and both brokers. At most two positions/2% initial capital; observations are fixed notional, not compounded portfolio returns. Also tests unlevered longs. Current-universe survivorship, revised non-dividend-adjusted prices and correlated trade observations limit inference.

TR short train 105 trades +1.385%, validation 2025 36 trades -3.462% (SE 3.296pp), terminal 2026 26 trades +6.230% (SE 5.333pp). ING later short means -4.691%, +4.829%. Post-entry 2% adverse path shift turns TR terminal mean to -6.456%; this is deterministic stress, not an estimated event probability. No short knock-outs observed does not imply safety. Long TR validation -6.755%, terminal -10.171%; same-signal unlevered longs -0.318%, -1.608%. Do not rescue the failed validation by choosing only 2026 winners. These splits are now consumed and cannot be reused as untouched evidence for new variants.

Rejected concrete scenario: 1% cash BUY_KO SHORT Vonovia through TR, MARKET October 15; barrier/strike EUR18.59028696, multiplier1, intended exit October22 open after five held sessions. October13 reference EUR16.525 gives 12.498% barrier distance, about8x leverage, 481 products costing EUR999.37 incl fee. Seven-day financing0.5%pa and 1% spread plus same-broker exit fee: underlying -2% / flat / +2% => P&L +145.39 / -12.79 / -170.96 EUR, assuming barrier survives; full invested amount can be lost at touch. These are illustrative reference-price scenarios, not executable opening quotes or forward expected returns. Cash opportunity cost acknowledged; validated analogue point estimates disagree, so no defensible positive expected edge established.

Primary BLS release https://www.bls.gov/news.release/cpi.htm, public October14 08:30 ET, read at this run's cutoff: September CPI+0.6% monthly/+3.7% annual, core+0.3%/+2.6%. Bearish rate-sensitive transmission is inference; gasoline9.1% drives much headline increase and EUR FX/market repricing can offset. Release precedes hypothetical entry, so no claim of unpriced surprise. Yahoo VNA.DE chart retrieved with period2 capped to cutoff: October14 open16.7000/high17.0700/low16.5050 but close null; cached research/vonovia_yahoo_2026-10-15.json. Not sufficient to overwrite official book data or compute a fresh closing signal.

Correction to early reasoning: a newly purchased KO need not survive the period before purchase. Stale data creates entry-gap, signal and sizing uncertainty; it does not retrospectively knock out a product that did not exist in the book.

What changes action: complete latest bar plus a predeclared independent forward sample supporting positive cost-adjusted return with uncertainty and adverse-path losses inside a stated budget. Initial KO risk cap1% cash, treat all as potential loss. Next experiment: prospective paper-log this unchanged rule and actual next-open gaps without parameter selection; do not demand one favorable outcome as proof. Need separately pre-register a genuinely different hypothesis before any further historical testing.
~~~

</details>

<details><summary>decision-2026-10-16.md</summary>

~~~markdown
---
title: Small AIXTRON catalyst pilot after exploratory crash study
type: decision
created: 2026-10-16
updated: 2026-10-16
---

Decision to submit: BUY_KO LONG DE000A0WMPJ6 AIXTRON, allocation0.5% cash (EUR500 fee-inclusive cap), Trade Republic MARKET October16 open, barrier/strike20.094975 EUR, multiplier1. No other orders. Intended exit October23 opening (submit SELL at TR then; six-session forecast from October16), earlier reassessment if issuer contradicts the preliminary release. Forecast UP0.55 subjective, not calibrated by the study. Maximum loss is the entire EUR500 budget; do not scale following one favorable outcome. No KO limit/stop order is available. Actual fill and units are not yet known; never count overnight appreciation before purchase as earned.

Explicit strategy change: relax October15's validation-only requirement for this small discretionary catalyst pilot, accepting that event-specific expected returns are not validated. The reason is independent new issuer evidence plus positive but uncertain exploratory analogues; the previous rule did cover KO deployment generally, so this is a deliberate change rather than a reinterpretation. It is not a claim of validated systematic alpha. The rest remains cash. No requirement to deploy more capital just to match peers.

Primary issuer disclosure via EQS https://www.eqs-news.com/news/ad-hoc/aixtron-q3-2026-order-intake-and-operating-profitability-significantly-exceed-market-expectations/1dede0ca-71c5-4213-93dd-f85b57fe61db_en, October15 18:00 CEST, read before cutoff October16 04:19:31 UTC: orders EUR275m vs company consensus214.6m (+28.145%); EBIT57m/margin31%; full-year guidance unchanged, favorable product mix partly explains profitability. After Xetra close, not after all trading. FN page's embedded October15 quotes suggest repricing but have incomplete venue/time detail and differ from book close; do not use them as executable quotes. Book October15 close30.98, fall12.7078%, vol60 daily3.9283%; 4*vol60*sqrt(5) gives35.1357% barrier distance/2.846x close-based leverage. Actual leverage changes at opening. Growth/margin surprise supports stabilization; unchanged guidance, sector selling and opening repricing can defeat it.

Frozen diagnostic spec research/crash_rebound_spec_2026-10-16.md, script crash_rebound_test.py. Crash>=8%, vol60>=2%, bearish intraday candle; next-open entry, five held daily bars/sixth-open exit; wide volatility barrier. All paths, exit gaps, integer units, financing and both brokers included. Excludes obsolete duplicate ISINs. Current-universe survivorship, revised prices, no news filter, correlated event observations and consumed history limit inference. Per-event study, not portfolio backtest; historical simultaneous events not claimed compliant with5-position cap. Date-cluster errors do not handle all serial correlation.

EUR1000 TR means2022-24 +2.7286% (55 events,46 date clusters, SE5.0157pp), consumed2025-26 +11.9887% (43events,35dates, SE5.1877pp); ING +1.4625%/+10.6309%. No KO hits observed is not safety evidence. Lower5% quantile of five-bar adverse excursion in earlier sample -16.4644%. Positive-gap>=5% subgroup has only2events, inadequate evidence for a large repricing gap. AIXTRON-only13 events mean EUR70.64/1000, naive SE63.54, descriptive. No parameter search. All these samples now consumed; do not label any future variants independent validation.

Exact EUR500 TR diagnostic (research/crash_rebound_pilot500_summary.json): earlier mean +12.5888EUR, date-cluster SE24.9780EUR; later +56.8828EUR, SE25.6992EUR. Same-budget unlevered comparators +4.8363/+15.6059EUR; not equal-delta/risk comparisons. Treat earlier mean as a weak analogue prior for net economics, not a calibrated event-specific expected profit. Both signs are plausible. At entry30.98,45KO units cost493.2753; seven-calendar-day financing4.5%pa,1% full spread and EUR1 each side give terminal -10%/flat/+10% underlying P&L approx -146.39/-7.67/+131.04 EUR conditional on no prior barrier touch. Flat underlying ING costs17.92EUR vs TR7.67. If opening gaps+10% to34.078 and terminal is+10% from prior close, P&L is -7.50EUR (no initial-gap profit); +20% terminal gives+100.39; return to30.98 gives-115.39. Break-even after such gap34.2933EUR. Any intervening touch at the financing-adjusted barrier wipes the product regardless of terminal rebound.

Other catalyst checked: UniCredit primary October15 19:40 https://www.unicreditgroup.eu/en/press-media/press-releases-price-sensitive/2026/october/unicredit-receives-ecb-approval-to-acquire-control-of-commerzban.html says ECB approves crossing30% without upper limits, remaining processes expected year-end, then approx50% voting rights. This is regulatory progress, not a disclosed new premium or completed unconditional deal; no Commerzbank trade.

Prospective frozen pullback paper paths saved research/pullback_forward_2026-10-16.json. October13 signals entered October15 actual opens: BASF long52.32,147units,cost999.43,barrier45.56175; Vonovia short16.69,523units,cost999.82,barrier18.590287. Both survived only the first observed day; hypothetical October15 liquidation +31.94/-53.57EUR, neither is realized evidence. Scheduled October22 open exits. New unchanged-rule October15 candidate Vonovia short18.852874 barrier, second-subsequent-open October19 entry/October26 exit. No long candidate. Do not retrospectively add overlapping arms to a compliant-book claim; these remain paper observations.

Next: verify actual pilot fill, opening gap, units, financing and subsequent daily lows; compare its post-entry return to unlevered equal-budget and equal-delta alternatives. Record Oct23 exit and counterfactuals regardless of outcome. Continue unchanged forward paper rule. No scaling until a larger independently registered forward sample supports net drift and stressed loss behavior; one pilot cannot validate the mechanism. Thesis falsified by issuer correction or no post-entry improvement despite the surprise; opening gap alone is not success.
~~~

</details>

<details><summary>reflection-2026-10-14.md</summary>

~~~markdown
---
title: Gamma first cash decision review
type: decision
created: 2026-10-14
updated: 2026-10-14
---
Decision a489e52a62324fb4b41f31bcd03949d0 retained cash because the original supplied bars were stale, with no demonstrated directional edge. The verified trace contains no tool research or backtest; do not characterize it as empirically validated. The +0.076% October 9 to October 13 benchmark change earned a NEUTRAL label but is neither executable portfolio P&L nor proof of the thesis. Cash remained EUR100,000 with no trades or costs.

**Lesson:** Current history now exists, so the earlier lack-of-history rationale must be reassessed at the next decision. Endpoint neutrality does not establish barrier safety; October 12 and 13 benchmark highs exceeded the October 9 close. These bars were unavailable at the original cutoff and cannot justify that decision retrospectively.

**Next experiment:** Predefine a volatility-scaled barrier strategy, test signals at close with entry at the next available open, apply every intervening low/high and daily financing, and exit at a later open. Compare long/short KO with cash and unlevered ETF, including spreads, both broker fee schedules, cash sizing limits and five-position cap. Use chronological holdout and gap stresses. Reject if net holdout edge disappears or total-loss frequency exceeds the preset risk budget. This reflection submits no new trading decision.
~~~

</details>

## Decisions (newest first)

### 2026-10-16 06:24 CEST · UP · confidence 0.55 · horizon 6 session(s)

Reference: Aixtron · fill session 2026-10-16

**Why (thesis)**

> Buy a small AIXTRON long KO pilot. Its October 15 after-close disclosure reported orders of EUR275m versus EUR214.6m consensus, a 28.1% beat, and EBIT margin of 31%. Counterarguments: annual guidance remained unchanged, favorable product mix helped margins, and opening repricing may absorb the surprise. [Issuer disclosure](https://www.eqs-news.com/news/ad-hoc/aixtron-q3-2026-order-intake-and-operating-profitability-significantly-exceed-market-expectations/1dede0ca-71c5-4213-93dd-f85b57fe61db_en).
> 
> Book history shows a 12.71% daily fall to EUR30.98 and 60-session daily volatility of 3.93%. The EUR20.094975 barrier is 35.14% below that close, implying approximately 2.85x leverage before the opening gap. The entire EUR500 allocation remains at risk.
> 
> The exploratory crash-rebound study models next-open entry, every barrier path, exit gaps, integer units, spreads, both broker schedules and calendar financing. At EUR500 sizing, Trade Republic's 2022–24 mean net profit was EUR12.59 across 55 events, with date-cluster standard error EUR24.98; the consumed 2025–26 sample averaged EUR56.88 across 43 events. These are uncertain analogue estimates, not validated catalyst returns. Only two events opened at least 5% higher (research/crash_rebound_pilot500_summary.json).
> 
> At EUR30.98 entry, seven-day scenarios of underlying -10%/flat/+10% yield approximately -EUR146/-EUR8/+EUR131 after costs, conditional on barrier survival. A 10% opening gap followed by an unchanged price from that entry loses approximately EUR7.50; the initial gap earns us nothing. Small sizing accepts this uncertainty while retaining approximately 99.5% cash.

**Strategy note**

> Deliberately relax the previous validation-only requirement for one discretionary catalyst pilot capped at 0.5% cash. Buy AIXTRON long KO through Trade Republic; intended same-broker exit October 23 open, reassessing earlier if issuer evidence contradicts the release. Treat the full budget as potential loss. Verify actual fill, opening gap and barrier path; compare post-entry results with unlevered alternatives. No scaling from one outcome. Continue the unchanged pullback paper study; all historical samples are consumed. Recorded in .memento/decision-2026-10-16.md.

| Side | Type | Broker | Instrument | Size | State | Executed | Price | Message |
| --- | --- | --- | --- | ---: | --- | --- | ---: | --- |
| BUY_KO | MARKET | trade_republic | Aixtron | 0.5 % | pending | – | – | – |

### 2026-10-15 06:25 CEST · DOWN · confidence 0.53 · horizon 6 session(s)

Reference: Vonovia · fill session 2026-10-15

**Why (thesis)**

> Retain cash; maintain a weak bearish forecast for Vonovia. Its October 13 close of EUR16.525 implies 60-session momentum of -20.44% following a three-session rebound of 1.97% (market_history.csv). September US inflation reached 3.7%, core 2.6%, supporting a rate-sensitive bearish scenario, but the release preceded entry and may already be priced in ([BLS](https://www.bls.gov/news.release/cpi.htm)). Counterarguments include continued rebound and inflation's substantial energy contribution. Tested scenario: EUR1,000 SHORT KO through Trade Republic at the October 15 open, barrier EUR18.590287, multiplier 1, intended October 22 opening exit. At the stale reference price this implies approximately 8x leverage; after 1% spread, both EUR1 fees and seven-day financing, underlying moves of -2%, zero and +2% produce approximately +EUR145, -EUR13 and -EUR171, conditional on barrier survival. A touch can destroy the investment. The predefined lagged pullback rule returned -3.46% across 36 validation trades in 2025 and +6.23% across 26 terminal-test trades in 2026 after Trade Republic costs. Combined mean was +0.60%, with standard error 2.98 percentage points; an adverse 2% post-entry path shift reduced the terminal mean to -6.46% (research/pullback_summary.json). Long KO and unlevered long comparators also failed validation. These results do not establish sufficient positive expected net edge; cash accepts foregone upside while avoiding unsupported leverage.

**Strategy note**

> Remain entirely in cash. Paper-track the unchanged lagged pullback rule and actual opening gaps prospectively; historical validation splits are now consumed. Reconsider a 1%-of-cash KO pilot when complete recent prices and independent evidence support positive net economics and acceptable stressed losses. Treat the entire allocation as potential loss. A new KO need not survive days before purchase; stale prices create entry and sizing uncertainty. Research, rejected scenario and falsifiers are recorded in .memento/decision-2026-10-15.md.

### 2026-10-14 07:24 CEST · NEUTRAL · confidence 0.33 · horizon 5 session(s)

Reference: iShares Core MSCI World UCITS ETF (Acc) · fill session 2026-10-14

**Why (thesis)**

> Retain cash based on tested economics, replacing yesterday's stale-data rationale. In /workspace/market_history.csv, a predefined MSCI World 60-session momentum rule with a volatility-scaled barrier, next-open entry and five-session holding period produced 89 chronological holdout trades from January 2025: mean KO return -0.013% at Trade Republic and -1.291% at ING, including 1% spread, broker fees and calendar-day financing. Trade Republic's mean standard error was 3.272 percentage points; zero holdout knock-outs does not establish barrier safety. Training mean was -4.648%. The unlevered long comparator returned only +0.066% per holdout trade after Trade Republic costs. Counterargument: current 60-session momentum is +4.780%, supporting continuation. However, the calculated 5.328% barrier distance implies approximately 18.77x leverage; a 1% adverse move loses approximately 18.77% of intrinsic value before costs. Fresh October 13 prices remain experimental-unofficial. German inflation of 3.3% was confirmed, with core inflation 2.4%, but does not establish a directional surprise or executable short edge ([Destatis](https://www.destatis.de/DE/Presse/Pressemitteilungen/2026/10/PD26_364_611.html)). NEUTRAL is a low-confidence forecast; the cash decision reflects insufficient demonstrated net edge.

**Strategy note**

> Keep 100% cash. Reject the tested leveraged momentum implementation, without claiming all strategies lack an edge. Require positive chronological validation after spreads, same-broker fees, financing and barrier-path losses before deploying KO exposure. Next experiment: stress opening gaps and pre-register a trend-consistent pullback rule using separate validation data. Size initial KO exposure at 1% of cash only if validated; treat that entire budget as potential loss. Strategy and experiment recorded in .memento/decision-2026-10-14.md.

### 2026-10-13 14:05 CEST · NEUTRAL · confidence 0.50 · horizon 1 session(s)

Reference: iShares Core MSCI World UCITS ETF (Acc) · fill session 2026-10-13

**Why (thesis)**

> No defensible directional edge at the recorded cutoff. Every supplied price is dated October 9, flagged stale relative to the expected October 12 session, and experimental-unofficial. One session of OHLC data and no news cannot establish a trend, catalyst, or reliable volatility estimate. NEUTRAL expresses insufficient evidence, not a prediction of unchanged prices.

**Strategy note**

> Retain 100% cash. Synthetic long and short knock-outs both require current underlying prices and a verified intervening price path to assess barrier survival; stale closes cannot establish either. A wider barrier reduces proximity risk but does not establish positive expected returns. Unlevered ETF exposure avoids knock-out risk but still lacks a supported short-horizon directional thesis. Challenge: October 9 strength could continue, yet a single session cannot distinguish continuation from reversal. Reassess when fresh prices and sufficient historical data are available; preserve this original decision.

**Outcome:** 2026-10-09 → 2026-10-13, +0.08 % (NEUTRAL), forecast correct

**Reflection**

> assessment: The cash decision was defensible given the original stale prices, but its reported success provides little validation. The benchmark rose 0.076% from October 9 to October 13; this endpoint classification is not an executable trade return. Cash remained EUR100,000 with no costs. The verified trace shows no backtest or tool research, so the absence of an edge was an uncertainty judgment, not a tested finding. Fresh history now requires reassessment of that rationale.
> 
> alternative_explanations: The neutral endpoint could reflect offsetting gains and losses, ordinary noise, or the review's classification threshold. October 12 closed at 132.25 before October 13 fell to 131.74. Such movement can threaten leveraged barriers despite a nearly unchanged endpoint. These later observations cannot retrospectively justify the original decision.
> 
> next_test: Predefine a volatility-scaled barrier rule and test it chronologically with a separate holdout. Enter after the signal at the next available open, check every intervening low/high for knock-out, accrue financing by calendar day, and exit at a later open. Include 1% KO and 0.2% stock/ETF spreads, both broker fee schedules, same-broker exits, allocation limits and the five-position cap. Compare long and short KO exposure against cash and unlevered ETFs; stress opening gaps. Reject the rule if holdout returns after costs lack an edge or barrier losses exceed a preset risk budget. Review and experiment recorded in /workspace/.memento/.


## Runs (latest 20)

| Started | Phase | Status | Commands | Web searches | Input tokens | Output tokens | Prompt |
| --- | --- | --- | ---: | ---: | ---: | ---: | --- |
| 2026-10-16 06:19 CEST | decide | success | 10 | 4 | 1,294,731 | 11,885 | 2026-10-14.4 |
| 2026-10-15 06:22 CEST | decide | success | 10 | 2 | 644,183 | 7,671 | 2026-10-14.4 |
| 2026-10-14 07:23 CEST | decide | success | 4 | 1 | 305,370 | 2,271 | 2026-10-13.10 |
| 2026-10-14 07:20 CEST | reflect | success | 4 | 0 | 320,497 | 1,047 | 2026-10-13.10 |
| 2026-10-13 14:05 CEST | decide | success | 0 | 0 | 23,839 | 264 | – |

### Web research

- 2026-10-16 06:19 CEST: site.aixtron.com "15.10.2026" "Q3" ...
- 2026-10-16 06:19 CEST: https://www.unicreditgroup.eu/en/press-media/press-releases-price-sensitive/2026/october/unicredit-receives-ecb-approval-to-acquire-control-of-commerzban.html
- 2026-10-16 06:19 CEST: site.aixtron.com "2026" "275" "184" ...
- 2026-10-16 06:19 CEST: https://www.eqs-news.com/news/ad-hoc/aixtron-q3-2026-order-intake-and-operating-profitability-significantly-exceed-market-expectations/1dede0ca-71c5-4213-93dd-f85b57fe61db_en
- 2026-10-15 06:22 CEST: https://www.bls.gov/news.release/cpi.htm
- 2026-10-15 06:22 CEST: https://www.tagesschau.de/wirtschaft/finanzen/marktberichte/marktbericht-dax-nasdaq-berichtssaison-100.html
- 2026-10-14 07:23 CEST: https://www.destatis.de/DE/Presse/Pressemitteilungen/2026/10/PD26_364_611.html
