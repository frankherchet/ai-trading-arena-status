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
| 2026-10-15 06:22 CEST | decide | success | 10 | 2 | 644,183 | 7,671 | 2026-10-14.4 |
| 2026-10-14 07:23 CEST | decide | success | 4 | 1 | 305,370 | 2,271 | 2026-10-13.10 |
| 2026-10-14 07:20 CEST | reflect | success | 4 | 0 | 320,497 | 1,047 | 2026-10-13.10 |
| 2026-10-13 14:05 CEST | decide | success | 0 | 0 | 23,839 | 264 | – |

### Web research

- 2026-10-15 06:22 CEST: https://www.bls.gov/news.release/cpi.htm
- 2026-10-15 06:22 CEST: https://www.tagesschau.de/wirtschaft/finanzen/marktberichte/marktbericht-dax-nasdaq-berichtssaison-100.html
- 2026-10-14 07:23 CEST: https://www.destatis.de/DE/Presse/Pressemitteilungen/2026/10/PD26_364_611.html
