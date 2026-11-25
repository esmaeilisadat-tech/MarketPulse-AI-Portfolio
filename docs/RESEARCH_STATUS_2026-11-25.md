# MarketPulse AI — Public research and engineering update

**Engineering review date:** 25 November 2026  
**Financial-metric evidence cutoff:** 17 November 2026  
**Evidence scope:** previously published dated research results and reported local engineering verification from the private implementation. No private source code, logs, or provider payloads are redistributed here.

## Implemented research and engineering components

The private MarketPulse AI project includes Python/PostgreSQL market-data validation, point-in-time features, stored forecast evaluation, a four-role LangGraph financial-news research workflow, Chroma-based retrieval, Streamlit research views and a separate bounded FastAPI research demonstration. The public site is an **independently authored, static portfolio**; it does not operate those components or access live data.

Recent private development work investigated news timestamp leakage, restricted database reads, bounded HTTP streaming (1,000,000 bytes before JSON parsing), credential echo protection and literal text rendering of untrusted headlines. Tests were performed locally, not as public GitHub CI.

## Dated measured evidence

| Research question | Observed result | Caution |
| --- | --- | --- |
| Direction of 29 stored experimental forecast outcomes | Model **31.0%** vs Always-UP **65.5%** | **28/29** share one anchor date; not independent forward evidence |
| RGLD price-only historical walk-forward | Logistic regression **36.4%** vs training-majority **41.7%** | Not a test of the frozen macroeconomic model |
| AEM price-only historical walk-forward | Logistic regression **38.7%** vs training-majority **42.8%** | No demonstrated directional edge |
| Chroma hit@3 on owner-authored synthetic corpus | **20/23**, lexical baseline **19/23** | Retrieval success does not establish answer quality |
| Attempted answerable local Llama questions | **0/20 valid generated answers** | The measured experiment FAILED/PARTIAL; remaining tasks were not all run |
| Reported private local software regression, 25 Nov 2026 | **1,358 passed / 0 failed / 1 skipped**, with 13 additional subtests | Disposable PostgreSQL 18 and offline fixtures; not GitHub CI or Production acceptance |

The skipped test requires missing retained real-model M4 evidence. No new model inference was performed to conceal the unresolved result. A passing synthetic demo and software unit tests do not imply successful predictive modeling or reliable autonomous agents.

## What visitors can inspect

- The public, high-level [architecture](ARCHITECTURE.md) and explicit trust boundaries
- This dated research and engineering summary, including negative evidence
- [English and German presentation notes](../presentation/PRESENTATION.md)
- [English and German CV/LinkedIn descriptions](../career/PROJECT_DESCRIPTIONS_EN_DE.md)
- The static [bilingual HTML portfolio](../index.html), using only local CSS and JavaScript

The static display contains no financial-data feed, model runtime, analytics SDK, remote images or third-party API calls. It does not demonstrate a real price/news refresh; synthetic before/after examples from private tests are illustrative only.

## Boundaries and remaining work

- **Official forecast: `NOT_READY`**. Stale/uncertified inputs and insufficient evidence prevent formal forecast readiness.
- **Production: `NO-GO`**. No authorization to deploy, trade, change production database privileges or run acquisition jobs.
- Real provider access, entitlements, licensing, quota and live data freshness: **NOT VERIFIED**.
- Independent integration review of private development PRs and actual model-quality improvements are separate future tasks.
- Historical NLP completion flags cannot reconstruct every past pending-news state.
- Public source-code release, screenshots containing real data and live services are **not** included in this portfolio.

**Portfolio purpose:** evidence-led AI/ML engineering case study, not financial advice or proof of a profitable strategy.
