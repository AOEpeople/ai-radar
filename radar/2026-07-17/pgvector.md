---
title: "pgvector"
ring: trial
segment: data-features
tags: [vector-db, retrieval]
---

[pgvector](https://github.com/pgvector/pgvector) is the de-facto standard extension for vector similarity search in PostgreSQL. Its strongest argument is operational: if you already run Postgres, vector search is one `CREATE EXTENSION` away - no additional database to deploy and operate.

Hybrid search works with plain SQL: combine vector similarity with Postgres full-text search and ordinary joins/metadata filters in one query (see [Smart Vector Database Usage](/data-features/smart_vector_db_usage/)).

For larger scale there are drop-in performance extensions (**pgvectorscale**, **VectorChord**) with faster index builds and better throughput at high recall - benchmarks in 2026 show Postgres-based setups competitive with dedicated vector databases well into the tens of millions of vectors.

## Team Insights

We run pgvector in production in customer projects. The operational simplicity is the deciding factor: Postgres is already operated and understood, so pgvector adds RAG-scale vector search without a new infrastructure component.

## Recommendation

If Postgres is already part of your stack, evaluate pgvector before introducing a dedicated vector database - for typical RAG workloads it is usually sufficient and cheaper to operate. Revisit dedicated options when scale or feature requirements demand it.
