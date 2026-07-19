---
title: Smart Vector Database Usage
ring: adopt
segment: data-features
tags: [retrieval, vector-db]
---

**Update 07/2026:** Two additions have become the production default since our last entry:

- **Hybrid search + reranking as baseline**: dense vectors combined with keyword search (BM25), followed by a cross-encoder/reranker step. Practice reports consistently show meaningfully better retrieval precision than pure vector search - make this the starting point, not an optimization.
- **Agentic retrieval**: retrieval as a loop instead of one-shot top-k - the agent reformulates queries, filters and re-retrieves until the context suffices (see the Agentic RAG section in [Advanced & Modular RAG](/architecture-pattern/rag/)). This changes indexing priorities: good metadata and filterable structure matter more when an agent iterates.

Most current vector databases ([Qdrant](/data-features/qdrant/), [Weaviate](/data-features/weaviate/), [Chroma](/data-features/chroma-db/)) support hybrid search natively - the reranker is the piece you typically add yourself.
