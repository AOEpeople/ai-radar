---
title: "Evaluation Driven AI Development"
ring: adopt
segment: architecture-pattern
tags: [evaluation]
---

**Update 07/2026:** The methodology stands unchanged and has become standard practice. Two updates:

- **Agent evaluation** extends the practice beyond output quality: trajectory evals (did the agent take a sensible path?), tool-call correctness and task completion over multi-step runs. Trace-based evaluation (production traces become eval cases) closes the loop between monitoring and offline evals.
- **Tool landscape shifted**: the "LangChain Evaluation" module referenced in our previous entry is legacy (moved to hold) - in the LangChain ecosystem its successors are LangSmith with openevals/agentevals. Our primary recommendation remains [Deepeval](/evaluation/deepeval/); 
