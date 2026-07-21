---
title: "Graphiti"
ring: assess
segment: data-features
tags: [knowledge, retrieval]
---

Graphiti (Zep, open source) builds real-time, incrementally updated **temporal knowledge graphs** for agents: facts carry validity intervals (bi-temporal), so the graph tracks how knowledge changes over time instead of overwriting it. Positioned primarily as a long-term memory layer for agents, and as a foundation for temporal GraphRAG.

- Distinct from generic graph DBs (Neo4j, which it can use as backend) and from LLM-extracted entity graphs (LightRAG/GraphRAG): the differentiator is the temporal model with point-in-time queries.
- Overlaps with [mem0](/frameworks/mem0/) on the agent-memory use case, but with an explicit graph and time dimension - evaluate which fits your recall and auditing needs.
- Assess: relevant when agents need durable, evolving memory or time-aware retrieval; graph modeling adds operational complexity over plain vector memory.

## Resources

- [GitHub Repository](https://github.com/getzep/graphiti)
