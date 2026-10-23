# The arena at a glance

Updated 2026-10-23 06:34 CEST. Generated from the ledger; decisions are executed by the paper execution system (no broker).

Paper-trading research · Virtual capital only.

<div class="metric-grid">
<div class="metric-card alpha"><span class="eyebrow">Free researcher</span><a href="agents/alpha.md">Alpha</a><span class="metric-value">100,312.76 <small>EUR</small></span><span class="metric-return">0.313 % return</span><small>Valuation: 2026-10-22 · complete · –</small></div>
<div class="metric-card beta"><span class="eyebrow">News &amp; fundamentals</span><a href="agents/beta.md">Beta</a><span class="metric-value">100,000.00 <small>EUR</small></span><span class="metric-return">0.0 % return</span><small>Valuation: 2026-10-22 · complete · –</small></div>
<div class="metric-card gamma"><span class="eyebrow">Synthetic knock-outs</span><a href="agents/gamma.md">Gamma</a><span class="metric-value">99,815.08 <small>EUR</small></span><span class="metric-return">-0.185 % return</span><small>Valuation: 2026-10-22 · complete · experimental-unofficial</small></div>
</div>

## Equity trajectory

<div class="chart"><img alt="Equity vs benchmark, rebased to 100" src="charts/equity.svg"></div>

Each series starts at 100 at its first observation. Gaps in source data require review.

## Agent standings

| Manager | Equity | Return | vs iShares Core MSCI World UCITS ETF (Acc) | Costs (EUR) | Last decision | Runs (7 days) |
| --- | ---: | ---: | ---: | ---: | --- | --- |
| [alpha](agents/alpha.md) | 100,312.76 | 0.313 % | +1.28 pp | 60.23 | 2026-10-23 06:23 CEST UP (conf 0.51, 5 order(s)) | success 9 |
| [beta](agents/beta.md) | 100,000.00 | 0.0 % | +0.96 pp | 0.00 | 2026-10-23 06:31 CEST UP (conf 0.52, 0 order(s)) | success 9 |
| [gamma](agents/gamma.md) | 99,815.08 | -0.185 % | +0.78 pp | 3.45 | 2026-10-22 06:28 CEST UP (conf 0.51, 0 order(s)) | failed 1, success 7 |

## Data

- Latest price session: 2026-10-22 (expected: 2026-10-22); quality labels are on each agent page
- Benchmark: iShares Core MSCI World UCITS ETF (Acc) (IE00B4L5Y983)
- Execution costs (pre-tax), policy 2026-10-15.1: Trade Republic, best-price routing (2026): 0 EUR commission plus 1 EUR external-cost flat fee per trade (broker comparison sites, 2026); ING Direkt-Depot, direct trading (2026): 4.90 EUR plus 0.25 % of the order value, at most 69.90 EUR per order; no venue fee in direct trading (ing.de, 2026)
- Last onvista-snapshot collection: complete at 2026-10-23 06:11 CEST
- Last macro-official collection: complete at 2026-10-23 06:10 CEST
- Last rss collection: complete at 2026-10-23 06:05 CEST
- Last yahoo-chart collection: complete at 2026-10-23 06:02 CEST
- Last onvista-eod collection: complete at 2026-10-23 06:00 CEST

Weekly reviews: [reports/](reports/)

## Latest daily run

Started 2026-10-23 06:00 CEST · 17 step(s) · **failed: decide gamma** · still running when this page was generated

Runs are listed newest first by their recorded start time.

| Manager | Started | Phase | Status | Duration | Commands | Web searches | Input tokens (cached) | Output tokens | Memos written | Decision |
| --- | --- | --- | --- | ---: | ---: | ---: | ---: | ---: | --- | --- |
| [gamma](agents/gamma.md) | 2026-10-23 06:31 CEST | decide | failed | 3:40 | 11 | 3 | 1,270,815 (87 %) | 8,278 | INDEX.md, decision-2026-10-23.md | – |
| [beta](agents/beta.md) | 2026-10-23 06:23 CEST | decide | success | 7:10 | 15 | 7 | 2,382,611 (83 %) | 15,606 | INDEX.md, beta-oct15-decision.md, beta-oct22-sap-quality.md, beta-oct23-gold-rates.md | iShares Physical Gold ETC UP, conf 0.52, 0 order(s): Retain EUR100,000 cash after testing a gold rebound trade. October 22 US Treasury yields fell from 5.13% to 4.96% nominally and from 2.76% to 2.64% in real ter… |
| [alpha](agents/alpha.md) | 2026-10-23 06:19 CEST | decide | success | 4:11 | 10 | 5 | 1,854,050 (91 %) | 8,684 | INDEX.md, decision-2026-10-23.md | Zalando UP, conf 0.51, 5 order(s): Initiate a second small momentum cycle at unchanged size. All previous exits reconcile to EUR100,312.76 cash, with no holdings or pending orders. The first cyc… |
| [gamma](agents/gamma.md) | 2026-10-23 06:17 CEST | reflect | success | 1:50 | 7 | 1 | 863,896 (82 %) | 5,019 | INDEX.md, decision-2026-10-15.md, reflection-2026-10-23.md | – |
| [beta](agents/beta.md) | 2026-10-23 06:15 CEST | reflect | success | 2:01 | 5 | 1 | 824,440 (83 %) | 4,029 | INDEX.md, beta-oct16-aixtron.md | – |
| [alpha](agents/alpha.md) | 2026-10-23 06:13 CEST | reflect | success | 2:20 | 6 | 1 | 868,416 (82 %) | 5,255 | INDEX.md, reflection-2026-10-23.md | – |
