# MarketPulse AI | Applied AI & ML Engineering

**Multi-agent financial research · Machine learning · Data engineering · RAG · Quantitative evaluation**

[Explore the bilingual portfolio](index.html) · [Architecture](docs/ARCHITECTURE.md) · [Latest research evidence](docs/RESEARCH_STATUS_2026-11-26.md) · [Presentation](presentation/PRESENTATION.md) · [English/German career profile](career/PROJECT_DESCRIPTIONS_EN_DE.md)

MarketPulse AI is an end-to-end AI/ML research project exploring how market data, economic indicators and financial news can support evidence-based analysis. Its focus is reproducible engineering, rigorous model evaluation and responsible AI—not trading signals or investment recommendations.

This public repository is a curated portfolio case study of a separate private implementation. It contains no private source mirror, credentials, licensed news payloads or raw research datasets.

## Research at a glance — 26 November 2026

| Scope | Latest reported offline experiment |
|---|---:|
| Assets across Germany, US-listed markets and London | 14 |
| Forecast horizons (trading sessions) | 1–5 |
| Economic indicators monitored | 7 |
| ML model families evaluated | 5 |
| Out-of-training-sample prediction records | 574,092 |
| Model comparison rows | 3,290 |
| Strategy evaluation rows | 590 |
| Latest reported local regression tests | 1,515 passed / 1 skipped |

Prediction records reuse observations across models and horizons; they are not independent events. The experiment used reconstructed historical snapshots and a previously inspected holdout. Results are exploratory, not prospective validation. The local test count predates subsequent unfinished edits and is not a GitHub CI result.

## Engineering contributions

| Area | Implementation and research |
|---|---|
| Data engineering | OHLCV ingestion, PostgreSQL/Supabase, source timestamps, corporate-action checks, normalization and data-quality diagnostics |
| Machine learning | Logistic Regression, Random Forest, Gradient Boosting, XGBoost and LightGBM; price-only and technical-feature experiments |
| Quantitative research | Expanding chronological folds, target purging, embargo, paired block bootstrap, multiple-testing diagnostics and benchmark comparisons |
| Strategy evaluation | Long/cash portfolio accounting, buy-and-hold and cash benchmarks, momentum, mean reversion, model-based rules, transaction-cost sensitivity and drawdown |
| Agentic AI | Four-role LangGraph research workflow: coordination, API collection, web discovery and evidence review |
| NLP & RAG | Financial sentiment, topic classification, local Llama inference, Chroma retrieval and evidence attribution |
| Application engineering | Streamlit research dashboard, FastAPI demonstration, offline result visualization and reproducible local test workflows |
| Responsible AI | Explicit insufficient-evidence states, bounded provider requests, least-privilege design and no unsupported production claims |

## Architecture

```mermaid
flowchart TD
    A[Market and macro data] --> C[Validation and timestamp checks]
    B[Financial news] --> D[Four-role research graph]
    D --> E[NLP and evidence-grounded retrieval]
    C --> F[Feature engineering]
    E -. gated news features .-> F
    F --> G[ML models and baselines]
    G --> H[Walk-forward and strategy evaluation]
    H --> I[Research dashboard]
    E --> I
```

## What the experiments actually demonstrate

The latest offline comparison evaluated price-only and technical-feature tracks across all 14 assets and five horizons. Five ML families were run alongside deterministic baselines. Economic evaluation included transaction-cost assumptions of 0, 10, 20 and 50 basis points per round trip.

**No statistically demonstrated predictive advantage:** no model comparison or strategy comparison passed the reported multiple-testing significance threshold of 5%. Positive historical results are exploratory candidates, not proof of future profitability.

Macro-enhanced and news-enhanced model tracks remain NOT_READY because historical availability and provenance are insufficient. Limited live agent pilots and retained-evidence executions do not establish reliable end-to-end live autonomy.

For methodology, measured limitations and evidence status, see [the dated research update](docs/RESEARCH_STATUS_2026-11-26.md). Earlier findings remain available in the [25 November report](docs/RESEARCH_STATUS_2026-11-25.md) and [17 November report](docs/RESEARCH_STATUS_2026-11-17.md).

## Technology stack

Python · pandas · NumPy · scikit-learn · XGBoost · LightGBM · PostgreSQL · SQLAlchemy · LangGraph · ChromaDB · Ollama/Llama · NLP · Streamlit · FastAPI · pytest · Docker

## Current status

Research prototype | Forecast NOT_READY | Production NO-GO

Next research priorities: prospective point-in-time data collection, validated news/macro features, independent holdout evaluation and guarded operational scheduling.

## Kurzprofil (Deutsch)

MarketPulse AI ist ein KI- und ML-Forschungsprojekt zur Analyse von Finanzmarktdaten, Wirtschaftsindikatoren und Nachrichten. Der Schwerpunkt liegt auf Datenpipelines, agentenbasierter Recherche, RAG, nachvollziehbarer Modellvalidierung und risikobewussten Backtests. Fünf ML-Modellfamilien wurden für 14 Assets und fünf Prognosehorizonte untersucht. Ein statistisch belastbarer Prognosevorteil wurde bislang nicht nachgewiesen.

## Privacy and responsible publication

Only sanitized aggregate research findings and separately authored portfolio materials are published. No account credentials, private implementation, database contents, licensed news, raw prediction files, model binaries or private execution traces are included. Synthetic examples remain explicitly labeled.

*Research and engineering portfolio only. Not financial advice or an automated trading service.*
