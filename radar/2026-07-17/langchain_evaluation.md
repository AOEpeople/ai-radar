---
title: "LangChain Evaluation"
ring: hold
segment: evaluation
tags: [evaluation]
featured: false
---

**Update 07/2026 (trial → hold):** The classic `langchain.evaluation` module is legacy since LangChain 1.0 (October 2025), and the documentation linked in our previous entry no longer exists.

Evaluation in the LangChain ecosystem now happens via **LangSmith** (commercial platform) and the open-source packages [openevals](https://github.com/langchain-ai/openevals) and [agentevals](https://github.com/langchain-ai/agentevals) (prebuilt evaluators for LLM outputs and agent trajectories, Python and TypeScript).

Do not build new evaluation setups on the legacy module. For a framework-independent alternative see [Deepeval](/evaluation/deepeval/).
