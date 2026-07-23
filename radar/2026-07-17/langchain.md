---
title: "LangChain"
ring: adopt
segment: frameworks
tags: []
---

**Update 07/2026:** With **LangChain 1.0** (GA October 2025) the framework was consolidated around agents ([announcement](https://www.langchain.com/blog/langchain-langgraph-1dot0)):

- `create_agent` is the new standard abstraction, running on the [LangGraph](/frameworks/langgraph/) runtime.
- A **middleware system** covers cross-cutting concerns like human-in-the-loop, summarization and PII redaction.
- Standardized content blocks across model providers; legacy chains moved to `langchain-classic`.
- Stability commitment: no breaking changes until 2.0.

Documentation moved to [docs.langchain.com](https://docs.langchain.com/) - the python.langchain.com links in our previous entry are partially dead.
