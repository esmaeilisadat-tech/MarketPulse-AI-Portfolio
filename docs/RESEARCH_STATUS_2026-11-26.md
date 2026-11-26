# Research evidence — 26 November 2026

This public update summarizes owner-supplied offline experiment outputs and reported local execution logs. It is not a source-code release or independent prospective validation.

## Experiment scope

- 14 assets; five trading-session horizons; seven monitored economic series.
- 16,501 price rows in the input snapshot; seven invalid platinum-series rows rejected. Only 31 next-open eligible feature observations were reported under the strict historical availability check.
- Five executed ML families: Logistic Regression, Random Forest, Gradient Boosting, XGBoost and LightGBM (4.6.0).
- 574,092 out-of-training-sample prediction records; 3,290 model-report rows, of which 2,520 are exploratory evaluated rows and 770 are NOT_READY rows.
- 590 strategy-report rows, including 576 exploratory and 14 NOT_READY rows.
- Price-only and technical-feature tracks evaluated; macro, news and existing frozen-model tracks not ready.
- Expanding chronological folds, exact-session target purging, one-row embargo; paired circular block bootstrap (length 20, 999 repetitions, seed 42); BH and BY multiple-testing diagnostics.
- Long/cash accounting with next-open execution assumptions, 252-session annualization and transaction-cost sensitivity.

## Findings and limitations

The lowest reported BH-adjusted q-value was 1.00 for model comparisons and 0.48 for strategy comparisons. No comparison reached the 5% threshold. These are exploratory statistical diagnostics, not evidence of validated strategy superiority.

Input prices ended between 20 October and 16 November 2026 depending on asset; all seven indicator series ended 13 October. A separate isolated staging pilot reported recovery through 25 November, but this was not the input snapshot used for the comparison and is not a production refresh.

Historical data was reconstructed from current snapshots, not archived historical vintages. The holdout had been previously inspected. Prospective validation and production readiness were explicitly false in the run receipt.

Limited real-web agent pilots and local retained-record research are distinct. Complete live four-role execution for the full universe is not independently verified.

## Software evidence

Latest supplied local regression log: 1,515 passed, one skipped, 111 warnings, 13 subtests passed. The skip requires retained real-model M4 evidence. Later edits have not been independently regression-tested. GitHub CI is not claimed.

## Source boundary

Aggregate figures derived from the supplied offline run manifest and model/strategy comparison CSVs; raw files, private implementation, licensed content and credentials are deliberately excluded. Earlier dated reports remain historical records.

Forecast: NOT_READY. Production: NO-GO. No investment recommendation.
