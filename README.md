# The arena at a glance

Updated 2026-10-15 06:25 CEST. Generated from the ledger; decisions are executed by the paper execution system (no broker).

Paper-trading research · Virtual capital only.

<div class="metric-grid">
<div class="metric-card alpha"><span class="eyebrow">Free researcher</span><a href="agents/alpha.md">Alpha</a><span class="metric-value">100,000.00 <small>EUR</small></span><span class="metric-return">0.0 % return</span><small>Valuation: 2026-10-13 · complete · –</small></div>
<div class="metric-card beta"><span class="eyebrow">News &amp; fundamentals</span><a href="agents/beta.md">Beta</a><span class="metric-value">100,000.00 <small>EUR</small></span><span class="metric-return">0.0 % return</span><small>Valuation: 2026-10-13 · complete · –</small></div>
<div class="metric-card gamma"><span class="eyebrow">Synthetic knock-outs</span><a href="agents/gamma.md">Gamma</a><span class="metric-value">100,000.00 <small>EUR</small></span><span class="metric-return">0.0 % return</span><small>Valuation: 2026-10-13 · complete · –</small></div>
</div>

## Equity trajectory

<div class="chart"><img alt="Equity vs benchmark, rebased to 100" src="charts/equity.svg"></div>

Each series starts at 100 at its first observation. Gaps in source data require review.

## Agent standings

| Manager | Equity | Return | vs iShares Core MSCI World UCITS ETF (Acc) | Costs (EUR) | Last decision | Runs (7 days) |
| --- | ---: | ---: | ---: | ---: | --- | --- |
| [alpha](agents/alpha.md) | 100,000.00 | 0.0 % | -0.41 pp | 0.00 | 2026-10-15 06:16 CEST UP (conf 0.52, 5 order(s)) | success 4 |
| [beta](agents/beta.md) | 100,000.00 | 0.0 % | -0.41 pp | 0.00 | 2026-10-15 06:22 CEST UP (conf 0.53, 0 order(s)) | success 4 |
| [gamma](agents/gamma.md) | 100,000.00 | 0.0 % | -0.41 pp | 0.00 | 2026-10-15 06:25 CEST DOWN (conf 0.53, 0 order(s)) | success 4 |

## Data

- Latest price session: 2026-10-13 (expected: 2026-10-14); quality labels are on each agent page
- Benchmark: iShares Core MSCI World UCITS ETF (Acc) (IE00B4L5Y983)
- Execution costs (pre-tax), policy 2026-10-13.5: Trade Republic, best-price routing (2026): 0 EUR commission plus 1 EUR external-cost flat fee per trade (broker comparison sites, 2026); ING Direkt-Depot, direct trading (2026): 4.90 EUR plus 0.25 % of the order value, at most 69.90 EUR per order; no venue fee in direct trading (ing.de, 2026)
- Last rss collection: complete at 2026-10-15 06:02 CEST
- Last yahoo-chart collection: complete at 2026-10-15 06:00 CEST

Weekly reviews: [reports/](reports/)

## Latest daily run

Started 2026-10-15 06:00 CEST · 13 step(s) · no failed steps · still running when this page was generated

| Manager | Phase | Status | Duration | Commands | Web searches | Input tokens (cached) | Output tokens | Memos written | Decision |
| --- | --- | --- | ---: | ---: | ---: | ---: | ---: | --- | --- |
| [alpha](agents/alpha.md) | decide | success | 8:28 | 21 | 7 | 2,659,974 (93 %) | 20,676 | INDEX.md, decision-2026-10-15.md, instrument-identifiers.md, reflection-2026-10-14.md | Zalando UP, conf 0.52, 5 order(s): Initiate a roughly 25% momentum pilot through Trade Republic. October 14 prices refresh the 20-session leaders to Zalando, Deutsche Boerse, Beiersdorf, Merck a… |
| [beta](agents/beta.md) | decide | success | 5:54 | 16 | 9 | 2,626,596 (93 %) | 14,609 | INDEX.md, beta-oct15-decision.md | Deutsche Boerse UP, conf 0.53, 0 order(s): Retain EUR100,000 cash after rejecting a concrete Deutsche Börse long. BLS released September CPI on October 14: headline inflation rose 0.6% monthly and 3.7% … |
| [gamma](agents/gamma.md) | decide | success | 2:54 | 10 | 2 | 644,183 (82 %) | 7,671 | INDEX.md, decision-2026-10-15.md | Vonovia DOWN, conf 0.53, 0 order(s): Retain cash; maintain a weak bearish forecast for Vonovia. Its October 13 close of EUR16.525 implies 60-session momentum of -20.44% following a three-session r… |
