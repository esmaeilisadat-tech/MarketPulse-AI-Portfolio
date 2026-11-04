# MarketPulse AI
### An AI/ML research platform for traceable financial analysis

MarketPulse AI explores how modular Python services, machine learning and evidence-based language-model workflows can support financial research. It combines market-data quality controls, directional-model evaluation, a bounded four-role research graph and a Streamlit inspection interface.

The engineering focus is reproducibility: preserve the evidence available at a cutoff, separate observations from interpretations and evaluate recorded forecasts against realized outcomes and simple baselines.

**Portfolio showcase only.** This repository contains independently written project documentation and presentation material. The implementation remains private. This is a research prototype, not financial advice or a trading service. No proven predictive advantage, general agent reliability or currently operating live news service is claimed.

## Architecture

```mermaid
flowchart TB
  subgraph PRICE[Price research boundary]
    A[Approved market observations] --> B[Validation and quantitative features]
    B --> C[Frozen directional-model artifacts]
    C --> D[Forecast records and outcome evaluation]
  end
  subgraph NEWS[News research boundary]
    E[Bounded provider adapters] --> F[Normalize, deduplicate and track provenance]
    F --> G[Local semantic retrieval]
    G --> H[Four-role research graph]
    F --> I[Event and reaction research]
    H --> J[Evidence-linked research result]
  end
  D --> K[Streamlit research views]
  I --> K
  J --> K
  L[(PostgreSQL / Supabase)] --- B
  L --- F
```

News Impact research and price forecasting remain separate. The diagram does not imply that news-derived features feed frozen price models. The graph orchestrates the existing executor. Provider calls, source validation and request budgets belong to that executor. See [module boundaries](docs/ARCHITECTURE.md).

## Technology stack

| Area | Technologies and role |
| --- | --- |
| Language and contracts | Python, Pydantic, typed research contracts |
| ML research | pandas, NumPy, scikit-learn, XGBoost, Transformers tooling |
| Agent orchestration | LangGraph, LangChain, local-model integration |
| Retrieval | Chroma, sentence embeddings and citation-oriented RAG |
| Persistence | PostgreSQL through Supabase, SQLAlchemy, local SQLite checkpoints |
| Interface | Streamlit, Plotly |
| Packaging | Docker build configuration with a non-root runtime user |
| Quality | pytest, GitHub Actions test workflow, Giskard evaluation experiments |

Tool presence does not establish deployment, live availability or model quality. Docker configuration was inspected, not built for this showcase. Remote CI execution could not be verified in this preparation session.

## Four-role research architecture

1. **Research Coordinator** chooses bounded actions based on available tools and evidence.
2. **API News Collector** uses the approved provider route within its request budget.
3. **Web Discovery and Extraction** addresses permitted evidence gaps when enabled.
4. **Evidence Reviewer** checks evidence decisions and citation references before delivery.

These are runtime responsibilities within a shared graph and executor, not four independently validated autonomous systems. Selected graph tests use injected model/tool responses. Historical local-model evaluations retained quality failures and a negative-control misclassification.

## Existing workflows

- Market observations pass session-date, corporate-action and provider-budget checks before authorized ingestion.
- Price research records forecasts separately from realized outcomes and compares directional results with simple baselines.
- News processing tracks normalization, deduplication, source provenance and availability separately from publication time.
- Retrieval and research views expose evidence-linked results and missing-evidence states.
- News Impact experiments distinguish retrospective evidence from prospective acquisition. Temporal association does not establish causation.

## Testing and CI evidence

**Local verification on 4 November 2026: 66 passed, 2 skipped, 0 failed** across three selected test files. The scope covered graph routing and repeat-execution boundaries, price-refresh safety and news-dataset contracts. Real network access was blocked, graph checkpoints used a disposable directory and production connections were unavailable. The two PostgreSQL-dependent tests were skipped. Two pytest plugin rewrite warnings occurred. This was not a full-suite run or live-provider validation.

The private project contains a GitHub Actions workflow that declares unit and PostgreSQL integration tests for pushes and pull requests. No green CI badge or recent remote success is asserted. See [evidence and limits](docs/CAPABILITIES_AND_TESTING.md).

## Dashboard screenshots

The private Streamlit dashboard provides research and evaluation views. **No approved public dashboard screenshot is included.** Existing screens may contain licensed news or operational data. A future screenshot requires an owner-approved synthetic-only session, visible demo labeling and a separate image audit. The architecture and presentation can be used without screenshots.

## Skills demonstrated

- Modular Python service design with clear orchestration and transport ownership.
- ML evaluation discipline, baseline comparisons and honest uncertainty reporting.
- Stateful LangGraph orchestration, RAG integration and evidence provenance.
- SQL persistence, additive schema evolution and isolated test design.
- Streamlit research interfaces and Docker / GitHub Actions configuration.
- Security-aware separation of private implementation from public documentation.

## Limitations and roadmap

Predictive skill remains unproven. Agent quality and evaluator reliability need further work. Live provider operation depends on fresh authorization, account rights and quota evidence. News Impact modeling readiness does not authorize training.

Future work includes more independent forward observations, stronger evaluator negative controls, stricter feature-availability audits, reproducible deployment checks and an approved synthetic dashboard demonstration. These research items do not prevent presenting the existing engineering work in job applications.

## Portfolio material

- [English presentation](presentation/MarketPulse_AI_Portfolio.pptx)
- [Readable presentation narrative](presentation/PRESENTATION.md)
- [English and German application descriptions](career/PROJECT_DESCRIPTIONS_EN_DE.md)
- [Public-content and rights statement](PUBLIC_CONTENT_NOTICE.md)

This showcase provides no installation path to the private system and distributes no implementation source, production datasets, model binaries, credentials or third-party news content.
