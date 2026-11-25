# MarketPulse AI — Evidence-first AI/ML engineering portfolio

**Public research case study · Python, PostgreSQL, scikit-learn, LangGraph, Chroma, Streamlit and FastAPI**

[View the bilingual static portfolio](index.html) · [Architecture](docs/ARCHITECTURE.md) · [Dated evidence](docs/RESEARCH_STATUS_2026-11-25.md) · [Presentation notes](presentation/PRESENTATION.md) · [English/German CV descriptions](career/PROJECT_DESCRIPTIONS_EN_DE.md)

MarketPulse AI is a privately implemented financial-data research platform. This **public repository is a separate, selectively authored presentation of engineering work**, not a source mirror and not a runnable live financial service. It explains data lineage, time-aware validation, model comparisons, evidence-grounded retrieval, bounded local agents and reproducible offline testing.

## Engineering contributions

| Component | Engineering focus | Verified boundary |
|---|---|---|
| Market data & features | PostgreSQL, data quality, availability timestamps and chronological evaluation | No claim of continuously fresh/live data |
| Forecast evaluation | Baseline comparisons, immutable outcome records, leakage-conscious research | No demonstrated predictive edge; Forecast `NOT_READY` |
| Four-role research graph | Coordinator, bounded news collection, evidence discovery and review | Offline tests are not evidence of reliable live autonomy |
| Chroma / local Llama RAG | Retrieval, citations, guarded source handling and budgeted local inference | Measured LLM answer quality failed; no hidden successful rerun |
| Streamlit / FastAPI | Historical research UI and a separate synthetic-only demonstration | Not a production API or trading interface |
| Testing & security | pytest, disposable PostgreSQL 18, bounded HTTP streaming and safe headline rendering | Local receipts; not a substitute for CI, penetration tests or Production approval |

## Measured results — including failures

- **Stored experimental forecast record (17 Nov 2026):** 29 outcomes, **31.0%** directional accuracy versus **65.5%** Always-UP on the same outcomes. **28/29** share an anchor date. No reliable predictive advantage can be inferred.
- **Price-only walk-forward (17 Nov 2026):** RGLD logistic regression **36.4%** vs training-majority **41.7%**; AEM logistic regression **38.7%** vs training-majority **42.8%**. These are **not** results for the frozen macroeconomic model.
- **Local synthetic retrieval:** Chroma hit@3 **20/23**, lexical baseline **19/23**; retrieval success is distinct from generated-answer quality.
- **Attempted answerable local LLM tasks:** **0/20** valid answers in the recorded experiment; the experiment stopped after its timeout, with other tasks unexecuted. This is a failure, not a model-quality acceptance.
- **Latest reported local full regression (25 Nov 2026):** **1,358 passed, 0 failed, 1 skipped**, with 13 separately reported subtests. This is **local execution evidence, not GitHub CI**. The skip concerns missing real-model M4 evidence; no model inference was run to fill it.

**Current boundaries:** Forecast `NOT_READY` · Production `NO-GO` · Live provider entitlements and data freshness **not verified** · No trading or investment recommendations.

## Explore

- [Dated evidence and test scope](docs/RESEARCH_STATUS_2026-11-25.md)
- [Architecture and boundaries](docs/ARCHITECTURE.md)
- [Presentation narrative for interviews](presentation/PRESENTATION.md)
- [English/German portfolio wording](career/PROJECT_DESCRIPTIONS_EN_DE.md)
- [Existing historical status, dated 17 Nov 2026](docs/RESEARCH_STATUS_2026-11-17.md)

**What is intentionally not published:** the private implementation, account/configuration secrets, database URLs or contents, retained licensed news, paid provider payloads, internal logs, original LLM traces, model binaries, private Git commit history and screenshots of real account data. All synthetic visual examples must remain explicitly labeled.

*Portfolio research only. Not financial advice, a trading system, or a production-ready forecasting service.*