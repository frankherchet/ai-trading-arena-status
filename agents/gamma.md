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
| 2026-10-14 07:23 CEST | decide | success | 4 | 1 | 305,370 | 2,271 | 2026-10-13.10 |
| 2026-10-14 07:20 CEST | reflect | success | 4 | 0 | 320,497 | 1,047 | 2026-10-13.10 |
| 2026-10-13 14:05 CEST | decide | success | 0 | 0 | 23,839 | 264 | – |

### Web research

- 2026-10-14 07:23 CEST: https://www.destatis.de/DE/Presse/Pressemitteilungen/2026/10/PD26_364_611.html
