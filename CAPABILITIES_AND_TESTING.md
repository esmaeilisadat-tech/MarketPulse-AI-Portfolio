# Capability and evidence boundaries

Evidence review date: 4 November 2026. This summary is documentation for a private prototype, not independent certification.

| Capability | Evidence available | Public claim boundary |
| --- | --- | --- |
| Four-role LangGraph routing | Selected offline graph tests passed | Bounded workflow implementation, not general autonomous reliability |
| Price refresh safeguards | Selected mock-provider safety tests passed | Budget and validation logic, not current provider service availability |
| News-dataset contracts | Selected offline tests passed | Evidence classification and separation checks, not modeling readiness |
| Streamlit dashboard | Implementation and historical AppTest reports inspected | Existing research UI, no new browser validation or publishable screenshot |
| RAG / Chroma | Implementation and configuration inspected | Retrieval integration, no fresh grounding benchmark |
| Directional ML evaluation | Private implementation and historical reports inspected | Experimental evaluation, no proven predictive advantage |
| Local-model / Giskard evaluation | Historical reports include quality failures and an incorrectly accepted negative control | Experimental evaluation tooling, not a reliable safety gate |
| PostgreSQL / Supabase | Adapters, schema and tests inspected | SQL research persistence, no production connection during this task |
| Docker | Build configuration inspected | Container packaging preparation, not a tested deployment |
| GitHub Actions | Test workflow inspected locally | CI configuration, no verified recent remote result |

## Fresh selected tests

66 passed, 2 skipped, 0 failed on 4 November 2026 in 7.19 seconds. Two plugin assertion-rewrite warnings occurred. Three test files covered graph contracts, price-refresh safety and news-dataset behavior. Python socket connections were blocked. Local environment-file loading was disabled for these tests. The graph entry point redirected its default checkpoint location into a temporary directory. No model inference or provider requests were performed. PostgreSQL tests skipped because no isolated test database was configured.

This is a selected local run against the available working tree. It is not a claim about the complete test suite, PR checks, production integrity or live service performance. Private detailed receipts remain outside this showcase.

## Deliberately excluded performance claims

Historical forecast outcomes do not establish statistically independent predictive skill. Small correlated cohorts, baseline underperformance in earlier reports and limited forward evidence prevent a strong performance claim. No accuracy headline, simulated trading return or agent-success percentage is presented here.
