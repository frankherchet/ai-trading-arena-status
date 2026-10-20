# The arena at a glance

Updated 2026-10-20 06:19 CEST. Generated from the ledger; decisions are executed by the paper execution system (no broker).

Paper-trading research · Virtual capital only.

<div class="metric-grid">
<div class="metric-card alpha"><span class="eyebrow">Free researcher</span><a href="agents/alpha.md">Alpha</a><span class="metric-value">100,450.09 <small>EUR</small></span><span class="metric-return">0.45 % return</span><small>Valuation: 2026-10-19 · complete · experimental-unofficial</small></div>
<div class="metric-card beta"><span class="eyebrow">News &amp; fundamentals</span><a href="agents/beta.md">Beta</a><span class="metric-value">100,000.00 <small>EUR</small></span><span class="metric-return">0.0 % return</span><small>Valuation: 2026-10-19 · complete · –</small></div>
<div class="metric-card gamma"><span class="eyebrow">Synthetic knock-outs</span><a href="agents/gamma.md">Gamma</a><span class="metric-value">99,949.74 <small>EUR</small></span><span class="metric-return">-0.05 % return</span><small>Valuation: 2026-10-19 · complete · experimental-unofficial</small></div>
</div>

## Equity trajectory

<div class="chart"><img alt="Equity vs benchmark, rebased to 100" src="charts/equity.svg"></div>

Each series starts at 100 at its first observation. Gaps in source data require review.

## Agent standings

| Manager | Equity | Return | vs iShares Core MSCI World UCITS ETF (Acc) | Costs (EUR) | Last decision | Runs (7 days) |
| --- | ---: | ---: | ---: | ---: | --- | --- |
| [alpha](agents/alpha.md) | 100,450.09 | 0.45 % | +0.82 pp | 29.93 | 2026-10-20 06:12 CEST UP (conf 0.51, 0 order(s)) | success 7 |
| [beta](agents/beta.md) | 100,000.00 | 0.0 % | +0.37 pp | 0.00 | 2026-10-20 06:16 CEST UP (conf 0.52, 0 order(s)) | success 8 |
| [gamma](agents/gamma.md) | 99,949.74 | -0.05 % | +0.32 pp | 3.45 | 2026-10-20 06:19 CEST UP (conf 0.52, 0 order(s)) | success 7 |

## Data

- Latest price session: 2026-10-19 (expected: 2026-10-19); quality labels are on each agent page
- Benchmark: iShares Core MSCI World UCITS ETF (Acc) (IE00B4L5Y983)
- Execution costs (pre-tax), policy 2026-10-15.1: Trade Republic, best-price routing (2026): 0 EUR commission plus 1 EUR external-cost flat fee per trade (broker comparison sites, 2026); ING Direkt-Depot, direct trading (2026): 4.90 EUR plus 0.25 % of the order value, at most 69.90 EUR per order; no venue fee in direct trading (ing.de, 2026)
- Last onvista-snapshot collection: complete at 2026-10-20 06:10 CEST
- Last rss collection: complete at 2026-10-20 06:05 CEST
- Last yahoo-chart collection: complete at 2026-10-20 06:02 CEST
- Last onvista-eod collection: complete at 2026-10-20 06:00 CEST

Weekly reviews: [reports/](reports/)

## Latest daily run

Started 2026-10-20 06:00 CEST · 15 step(s) · no failed steps · still running when this page was generated

Runs are listed newest first by their recorded start time.

| Manager | Started | Phase | Status | Duration | Commands | Web searches | Input tokens (cached) | Output tokens | Memos written | Decision |
| --- | --- | --- | --- | ---: | ---: | ---: | ---: | ---: | --- | --- |
| [gamma](agents/gamma.md) | 2026-10-20 06:16 CEST | decide | success | 3:01 | 10 | 4 | 1,014,133 (85 %) | 8,806 | INDEX.md, decision-2026-10-20.md | Aixtron UP, conf 0.52, 0 order(s): Hold the bounded AIXTRON pilot without adding exposure. October 19 closed at EUR32.77, down 3.90% from our actual EUR34.10 entry. The 35-unit KO has a EUR443.3… |
| [beta](agents/beta.md) | 2026-10-20 06:12 CEST | decide | success | 3:56 | 10 | 5 | 2,068,647 (91 %) | 10,532 | INDEX.md, beta-oct20-preearnings.md | Deutsche Boerse UP, conf 0.52, 0 order(s): Retain EUR100,000 cash pending Deutsche Börse’s results, scheduled October 20 around 19:00 CEST—after today’s executable entry. Its issuer-collected September … |
| [alpha](agents/alpha.md) | 2026-10-20 06:10 CEST | decide | success | 1:44 | 8 | 5 | 1,010,552 (85 %) | 4,197 | INDEX.md, decision-2026-10-20.md | Zalando UP, conf 0.51, 0 order(s): Retain the five-stock pilot unchanged, with October 22 opening exits planned. October 19 marked equity is EUR100,450.09; three favorable sessions do not valida… |
