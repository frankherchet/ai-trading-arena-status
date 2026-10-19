# The arena at a glance

Updated 2026-10-19 06:18 CEST. Generated from the ledger; decisions are executed by the paper execution system (no broker).

Paper-trading research · Virtual capital only.

<div class="metric-grid">
<div class="metric-card alpha"><span class="eyebrow">Free researcher</span><a href="agents/alpha.md">Alpha</a><span class="metric-value">100,360.28 <small>EUR</small></span><span class="metric-return">0.36 % return</span><small>Valuation: 2026-10-16 · complete · experimental-unofficial</small></div>
<div class="metric-card beta"><span class="eyebrow">News &amp; fundamentals</span><a href="agents/beta.md">Beta</a><span class="metric-value">100,000.00 <small>EUR</small></span><span class="metric-return">0.0 % return</span><small>Valuation: 2026-10-16 · complete · –</small></div>
<div class="metric-card gamma"><span class="eyebrow">Synthetic knock-outs</span><a href="agents/gamma.md">Gamma</a><span class="metric-value">99,954.20 <small>EUR</small></span><span class="metric-return">-0.046 % return</span><small>Valuation: 2026-10-16 · complete · experimental-unofficial</small></div>
</div>

## Equity trajectory

<div class="chart"><img alt="Equity vs benchmark, rebased to 100" src="charts/equity.svg"></div>

Each series starts at 100 at its first observation. Gaps in source data require review.

## Agent standings

| Manager | Equity | Return | vs iShares Core MSCI World UCITS ETF (Acc) | Costs (EUR) | Last decision | Runs (7 days) |
| --- | ---: | ---: | ---: | ---: | --- | --- |
| [alpha](agents/alpha.md) | 100,360.28 | 0.36 % | +0.86 pp | 29.93 | 2026-10-19 06:12 CEST UP (conf 0.51, 0 order(s)) | success 6 |
| [beta](agents/beta.md) | 100,000.00 | 0.0 % | +0.50 pp | 0.00 | 2026-10-19 06:15 CEST UP (conf 0.51, 0 order(s)) | success 7 |
| [gamma](agents/gamma.md) | 99,954.20 | -0.046 % | +0.46 pp | 3.45 | 2026-10-19 06:18 CEST UP (conf 0.53, 0 order(s)) | success 6 |

## Data

- Latest price session: 2026-10-16 (expected: 2026-10-16); quality labels are on each agent page
- Benchmark: iShares Core MSCI World UCITS ETF (Acc) (IE00B4L5Y983)
- Execution costs (pre-tax), policy 2026-10-15.1: Trade Republic, best-price routing (2026): 0 EUR commission plus 1 EUR external-cost flat fee per trade (broker comparison sites, 2026); ING Direkt-Depot, direct trading (2026): 4.90 EUR plus 0.25 % of the order value, at most 69.90 EUR per order; no venue fee in direct trading (ing.de, 2026)
- Last onvista-snapshot collection: complete at 2026-10-19 06:10 CEST
- Last rss collection: complete at 2026-10-19 06:05 CEST
- Last yahoo-chart collection: complete at 2026-10-19 06:02 CEST
- Last onvista-eod collection: complete at 2026-10-19 06:00 CEST

Weekly reviews: [reports/](reports/)

## Latest daily run

Started 2026-10-19 06:00 CEST · 15 step(s) · no failed steps · still running when this page was generated

Runs are listed newest first by their recorded start time.

| Manager | Started | Phase | Status | Duration | Commands | Web searches | Input tokens (cached) | Output tokens | Memos written | Decision |
| --- | --- | --- | --- | ---: | ---: | ---: | ---: | ---: | --- | --- |
| [gamma](agents/gamma.md) | 2026-10-19 06:15 CEST | decide | success | 3:04 | 11 | 4 | 1,171,815 (87 %) | 8,891 | INDEX.md, decision-2026-10-19.md | Aixtron UP, conf 0.53, 0 order(s): Hold the existing AIXTRON pilot without adding exposure. Its October 16 opening gap was 10.07%, but the underlying subsequently fell 3.55% from our EUR34.10 en… |
| [beta](agents/beta.md) | 2026-10-19 06:12 CEST | decide | success | 2:58 | 9 | 5 | 1,533,368 (90 %) | 8,762 | INDEX.md, beta-oct16-aixtron.md, beta-oct19-dhl.md | DHL Group UP, conf 0.51, 0 order(s): Retain EUR100,000 cash after testing DHL's guidance increase against dated expectations. The October 16 post-Xetra release raised the EBIT guidance floor from … |
| [alpha](agents/alpha.md) | 2026-10-19 06:10 CEST | decide | success | 2:08 | 9 | 5 | 1,141,211 (87 %) | 6,273 | INDEX.md, decision-2026-10-19.md | Zalando UP, conf 0.51, 0 order(s): Hold the five-stock pilot unchanged. October 16 marked equity is EUR100,360.28; the weekly lead and two favorable sessions do not validate the strategy. Source… |
