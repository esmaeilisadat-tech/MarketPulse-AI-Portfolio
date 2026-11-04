# Architecture and module boundaries

This is an independently written conceptual view of a private research implementation. It contains no source-code excerpts or operational endpoints.

| Boundary | Owns | Must not imply |
| --- | --- | --- |
| Market-data services | Session selection, validation, bounded refresh and provenance | A continuously operating live feed |
| Price ML research | Quantitative features, frozen artifacts, forecast and outcome records | Proven predictive skill or news-feature integration |
| News intake | Provider adapters, normalization, deduplication, timestamps and budgets | Permission to redistribute provider content |
| Four-role graph | Coordinator decisions, role state and checkpointed orchestration | Independent tool authority or unrestricted autonomy |
| Shared executor | Approved transport, budgets, validation and evidence decisions | A parallel bypass around provider guards |
| Retrieval | Local embeddings, semantic search and citation references | Guaranteed truth or complete source coverage |
| News Impact research | Event grouping, observed reactions and eligibility diagnostics | Causal inference or authorized model training |
| Storage adapters | PostgreSQL / Supabase research persistence and SQLite checkpoints | A public database or transferable production access |
| Streamlit UI | Research inspection and presentation | Trading execution |
| Engineering configuration | Docker packaging and GitHub Actions test definitions | A verified production deployment |

## Modular Design and Clean Core

The showcase explains existing service boundaries without extracting private implementation. Orchestration reuses the shared executor. Presentation consumes research outputs. News research remains separate from frozen price models. Packaging and test orchestration sit outside the analytical core.

## Data and evidence flow

Approved observation intake precedes validation and persistence. Market features support price-model research. News normalization supports retrieval and event research. Research answers preserve evidence references and distinguish missing observations from negative findings. Stored outcomes support evaluation after maturity.

Publication time, retrieval time and feature eligibility answer different questions. A retrospective import cannot become prospective evidence. An observed market reaction is an association, not a causal effect.
