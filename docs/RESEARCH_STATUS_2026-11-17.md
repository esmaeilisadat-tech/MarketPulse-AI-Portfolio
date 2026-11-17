# Research and delivery status — 17 November 2026

> Portfolio-safe summary of the private project’s retained engineering and evaluation evidence. It does **not** grant access to the private code, datasets, credentials, operational SQL, or paid/licensed content.

## What changed since the previous portfolio snapshot

- **Consolidated dashboard:** The root Streamlit application on port 8502 incorporates a price-only **Research Sandbox** alongside market overview, asset analysis, forecasts, news intelligence, research and status views. An older port-8503 interface is retained until owner verification; do not describe it as retired.
- **Access boundaries:** An owner-run test confirmed a dedicated PostgreSQL reader could retrieve real stored market data without superuser/BYPASSRLS privileges. At the audit date its SELECT grants covered **7 tables**; other sections can show access-limited notices. A proposed expansion to 14 readable tables was tested on disposable PostgreSQL but **not applied to production**.
- **Four-role research graph:** Coordinator, API news collection, web evidence discovery/extraction and evidence review are covered by offline fixture tests. The live research feature remains disabled, with zero request budgets; this is **not** a demonstration of generally reliable autonomous agents.
- **Research workflow and data-quality documentation:** The project now records freshness gaps and safe, bounded *plans* for price/indicator refresh and pending news NLP analysis. These plans are not evidence that the corresponding production jobs were executed.
- **Security proposals:** Additional API-role privilege hardening and rollback procedures have been tested locally but await separate owner approval and production application.

## Reproducible evaluation: negative findings matter

The private evaluation report dated **17 November 2026** explicitly concluded **NO DEMONSTRATED EDGE**. The results below are from the private, retained evaluation record; the public portfolio does not redistribute the underlying stored data or code.

| Evaluation | Research model | Simple baseline | Interpretation |
| --- | ---: | ---: | --- |
| 29 preregistered experimental forecasts, 2–3 session horizon | **31.0%** directional accuracy | **65.5%** always UP | No demonstrated advantage; 28 of 29 forecasts share an anchor date |
| RGLD, price-only historical walk-forward, logistic regression | **36.4%** accuracy | **41.7%** training-window majority; **43.9%** always UP | Below both reference accuracy baselines |
| AEM, price-only historical walk-forward, logistic regression | **38.7%** accuracy | **42.8%** training-window majority; **45.1%** always UP | Below both reference accuracy baselines |

The historical experiment included expanding-window retraining, a three-session purge at the split, and checks with non-overlapping test observations. The stored ledger's near-single-date concentration means its forecasts are not 29 independent market episodes. These experiments should not be interpreted as proof of predictive performance, a profitable strategy, or causal news impact.

The canonical model is **NOT_READY**, pending an authorized refresh and verification of seven stale macroeconomic indicator series. Nothing was promoted or retrained as part of this status report.

## Dataset and operations snapshot

The private read-only audit recorded on 17 November:
- Selected assets RGLD and AEM had their latest stored price session on **2 November 2026**; several others stopped on **20–21 October**.
- Seven indicator series stopped on **13 October 2026**.
- The news table contained **171 articles**, with **131** yet to receive NLP processing.
- The production price workflow was approval-gated and scheduled runs were skipped; diagnosis of staleness does not imply a provider failure.
- A single forward prediction and its evaluation were present; this is far too little to infer model skill.

These figures are dated historical observations, **not** currently live counts.

## Testing and readiness evidence

| Scope | Recorded status |
| --- | --- |
| PR #40 / #41 remote checks | 9/9 checks passed on each PR according to the private release record |
| Latest local integrated suite after PR #42 | **1,140 passed, 0 failed, 1 skipped** on Python 3.12 with disposable PostgreSQL |
| PR #42 remote CI | Pushed commits skipped CI; no fresh green run is claimed |
| Offline research/agent fixture tests | Passed selected paths; not a live-provider reliability test |
| Production SQL hardening and extended SELECT grants | Prepared and locally tested; **not applied** |
| Live research, paid providers, automated price refresh, NLP backlog | Approval-gated or disabled |
| Public dashboard deployment | Not provided by this portfolio |

## Ownership, scope and publication safeguards

This repository is an independently authored skills showcase, not a code mirror. It intentionally excludes production data and database connection strings, `.env` values, API tokens, internal operational reports, privilege-altering SQL scripts, pretrained model binaries, third-party licensed article text, personal holdings and private screenshots.

The engineering result worth presenting is a research platform with explicit evidence and safety boundaries. The negative model results and incomplete operational readiness are reported rather than concealed. This is **not financial advice** and not an automated trading service.
