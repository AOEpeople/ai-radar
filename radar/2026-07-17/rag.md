---
title: "Advanced & Modular RAG"
ring: adopt
segment: architecture-pattern
tags: [retrieval]
---

**Update 07/2026:** The 2026 consensus in one sentence: naive RAG is dead, retrieval is not. Two things changed since our last entry:

- **Long-context hybrid architectures are standard**: with context windows in the million-token range, small corpora can skip retrieval entirely - but for large or dynamic knowledge bases, retrieval remains essential for cost, latency and grounding. Production systems combine both: retrieval narrows down, long context carries more of it.
- **Agentic RAG is increasingly used in production and works well**: embedded in agent loops, the retrieve → rethink → retrieve cycle fits naturally - the agent reformulates queries, evaluates results and retrieves again until the context suffices. RAG evolves from a fixed pipeline into a "context engine" that agents query iteratively. See also [Context Engineering](/architecture-pattern/context-engineering/) and [Smart Vector Database Usage](/data-features/smart_vector_db_usage/) for the retrieval-side defaults (hybrid search + reranking).

The RAG-paradigm framing of our previous entry (Gao et al., 2023) is still useful vocabulary, but read it as history of the field rather than current architecture guidance.
