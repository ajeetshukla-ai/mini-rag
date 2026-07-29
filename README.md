# mini-rag

A RAG system built from scratch to understand every component — chunking, embeddings, hybrid search, and citations — no framework magic.
## Planned Design

**Pipeline:**
1. Chunk documents — 500 tokens, 50-token overlap, structure-aware
2. Embed with BGE-m3 (multilingual — handles Hindi/Hinglish)
3. Store in PostgreSQL + pgvector, HNSW index
4. Hybrid retrieval — vector + full-text, fused with RRF
5. Generate an answer constrained to retrieved chunks only
6. Return a citation for every claim

**Planned evaluation:** 40 fixed questions over a test document set,
measuring recall@5 as chunking and retrieval strategy change.

| Change | recall@5 | Notes |
|---|---|---|
| Baseline (vector only) | TBD | |
| + hybrid full-text | TBD | |
| + RRF tuning | TBD | |

**Status:** Design complete. Build starts Week 4.
