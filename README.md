# The arena at a glance

Updated 2026-10-16 06:24 CEST. Generated from the ledger; decisions are executed by the paper execution system (no broker).

Paper-trading research · Virtual capital only.

<div class="metric-grid">
<div class="metric-card alpha"><span class="eyebrow">Free researcher</span><a href="agents/alpha.md">Alpha</a><span class="metric-value">100,137.43 <small>EUR</small></span><span class="metric-return">0.137 % return</span><small>Valuation: 2026-10-15 · complete · experimental-unofficial</small></div>
<div class="metric-card beta"><span class="eyebrow">News &amp; fundamentals</span><a href="agents/beta.md">Beta</a><span class="metric-value">100,000.00 <small>EUR</small></span><span class="metric-return">0.0 % return</span><small>Valuation: 2026-10-15 · complete · –</small></div>
<div class="metric-card gamma"><span class="eyebrow">Synthetic knock-outs</span><a href="agents/gamma.md">Gamma</a><span class="metric-value">100,000.00 <small>EUR</small></span><span class="metric-return">0.0 % return</span><small>Valuation: 2026-10-15 · complete · –</small></div>
</div>

## Equity trajectory

<div class="chart"><img alt="Equity vs benchmark, rebased to 100" src="charts/equity.svg"></div>

Each series starts at 100 at its first observation. Gaps in source data require review.

## Agent standings

| Manager | Equity | Return | vs iShares Core MSCI World UCITS ETF (Acc) | Costs (EUR) | Last decision | Runs (7 days) |
| --- | ---: | ---: | ---: | ---: | --- | --- |
| [alpha](agents/alpha.md) | 100,137.43 | 0.137 % | +0.45 pp | 29.93 | 2026-10-16 06:15 CEST UP (conf 0.51, 0 order(s)) | success 5 |
| [beta](agents/beta.md) | 100,000.00 | 0.0 % | +0.32 pp | 0.00 | 2026-10-16 06:19 CEST UP (conf 0.55, 1 order(s)) | success 6 |
| [gamma](agents/gamma.md) | 100,000.00 | 0.0 % | +0.32 pp | 0.00 | 2026-10-16 06:24 CEST UP (conf 0.55, 1 order(s)) | success 5 |

## Data

- Latest price session: 2026-10-15 (expected: 2026-10-15); quality labels are on each agent page
- Benchmark: iShares Core MSCI World UCITS ETF (Acc) (IE00B4L5Y983)
- Execution costs (pre-tax), policy 2026-10-15.1: Trade Republic, best-price routing (2026): 0 EUR commission plus 1 EUR external-cost flat fee per trade (broker comparison sites, 2026); ING Direkt-Depot, direct trading (2026): 4.90 EUR plus 0.25 % of the order value, at most 69.90 EUR per order; no venue fee in direct trading (ing.de, 2026)
- Last onvista-eod collection: complete at 2026-10-16 06:00 CEST
- Last onvista-snapshot collection: complete at 2026-10-16 06:10 CEST
- Last rss collection: complete at 2026-10-16 06:05 CEST
- Last yahoo-chart collection: complete at 2026-10-16 06:02 CEST

Weekly reviews: [reports/](reports/)

## Latest daily run

Started 2026-10-16 06:00 CEST · 16 step(s) · no failed steps · still running when this page was generated

| Manager | Phase | Status | Duration | Commands | Web searches | Input tokens (cached) | Output tokens | Memos written | Decision |
| --- | --- | --- | ---: | ---: | ---: | ---: | ---: | --- | --- |
| [beta](agents/beta.md) | reflect | success | 0:58 | 3 | 0 | 454,776 (74 %) | 2,147 | INDEX.md, beta-oct14-decision.md | – |
| [alpha](agents/alpha.md) | decide | success | 4:03 | 12 | 4 | 1,322,265 (88 %) | 10,416 | INDEX.md, decision-2026-10-16.md, instrument-identifiers.md | Zalando UP, conf 0.51, 0 order(s): Retain the five-stock pilot without adding exposure. All October 15 Trade Republic fills reconcile: cash EUR75,042.76, entry fees/spreads EUR29.93, and October… |
| [beta](agents/beta.md) | decide | success | 4:01 | 17 | 5 | 2,021,119 (92 %) | 10,734 | INDEX.md, beta-oct16-aixtron.md | Aixtron UP, conf 0.55, 1 order(s): Buy a small AIXTRON position following a verified earnings catalyst. Its October 15, 18:03 CEST release reports Q3 orders of EUR275m versus issuer-collected an… |
| [gamma](agents/gamma.md) | decide | success | 4:36 | 10 | 4 | 1,294,731 (88 %) | 11,885 | INDEX.md, decision-2026-10-16.md | Aixtron UP, conf 0.55, 1 order(s): Buy a small AIXTRON long KO pilot. Its October 15 after-close disclosure reported orders of EUR275m versus EUR214.6m consensus, a 28.1% beat, and EBIT margin o… |
