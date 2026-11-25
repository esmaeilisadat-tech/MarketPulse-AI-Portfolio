# MarketPulse AI — Interview presentation notes

## English — 3–5 minutes

**Problem.** Financial forecasting demos can overstate performance, ignore simple baselines, and accidentally use information that was not available at the prediction time.

**What I engineered.** MarketPulse AI is a private Python/PostgreSQL research system covering time-aware data lineage, market-quality checks, chronological ML evaluation, stored forecasts, a four-role LangGraph research workflow, Chroma retrieval and Streamlit research views. The separate bounded FastAPI demonstration uses fixed synthetic examples rather than a live financial feed.

**How I approached reliability.** I separated publication, acquisition, ingestion, NLP completion and association timestamps; wrote negative tests for point-in-time leakage; placed limits on network-response bytes before JSON parsing; protected credentials and constrained model/tool calls. I kept production and test database privileges separate.

**What testing proved.** The private 25 November report records 1,358 passing local software tests and one skipped real-model-evidence test. Browser and disposable PostgreSQL checks were also reported locally. These are not public CI passes and do not certify production security.

**What did not work.** The 29-outcome experimental directional sample showed 31.0% model accuracy versus 65.5% for Always-UP, with 28/29 sharing the same anchor date. Synthetic retrieval hit@3 was 20/23, but the attempted local Llama answerable questions produced 0/20 valid answers. I kept these failures in the result.

**Conclusion.** My strongest result is an auditable AI/ML engineering workflow, not a claim of profitable forecasts. Next steps would be independent prospective evaluation, better model-quality measurements and approved data freshness checks before considering production.

## Deutsch — 3–5 Minuten

**Ausgangsproblem.** Finanzprognose-Demos können Erfolgsquoten überbewerten, einfache Baselines ignorieren und versehentlich Informationen aus der Zukunft verwenden.

**Meine Umsetzung.** MarketPulse AI ist eine private Forschungsplattform mit Python und PostgreSQL: Datenherkunft, zeitbewusste Merkmale, chronologische ML-Evaluation, gespeicherte Prognosen, ein Vier-Rollen-Workflow mit LangGraph, Chroma-Retrieval und eine Streamlit-Oberfläche. Eine getrennte FastAPI-Demo nutzt ausschließlich synthetische Beispiele.

**Qualität und Sicherheit.** Ich habe Veröffentlichungs-, Verfügbarkeits-, Import-, NLP- und Zuordnungszeitpunkte getrennt behandelt, negative Leakage-Tests ergänzt, HTTP-Antwortgrößen vor dem JSON-Parsing begrenzt sowie Zugangsdaten und Modellaufrufe geschützt. Lokale Tests wurden von Produktionszugriffen getrennt.

**Nachweise.** Der private Prüfbericht vom 25. November nennt 1.358 bestandene lokale Softwaretests und einen übersprungenen Modellnachweistest. Das ist kein GitHub-CI-Nachweis und keine Produktionsfreigabe.

**Negative Ergebnisse.** Das kleine Prognoseexperiment erreichte 31,0 % gegenüber 65,5 % einer Always-UP-Baseline. Beim synthetischen Retrieval lag Chroma bei 20/23 hit@3, die lokalen Llama-Antworten erfüllten jedoch bei 0/20 bearbeiteten beantwortbaren Aufgaben die Gültigkeitskriterien.

**Fazit.** Das Projekt zeigt reproduzierbares Data Engineering, ML-Evaluation, AI Engineering und eine transparente Fehleranalyse. Es ist keine freigegebene Finanzprognose oder Handelssoftware.
