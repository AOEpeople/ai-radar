---
title: "Langfuse"
ring: trial
segment: evaluation
tags: [observability, evaluation]
---

Langfuse is the most widely used open-source LLM observability platform: tracing, prompt management, cost tracking, datasets and trace-based evaluation (LLM-as-judge on production traces, scores API, annotation queues).

- **MIT-licensed core** including evals, playground and experiments; only enterprise features (SCIM, audit logs) are commercial. Fully self-hostable - note the infrastructure footprint (Postgres + ClickHouse).
- Acquired by **ClickHouse in January 2026** with an explicit open-source and self-hosting commitment.
- Observability-first: the natural fit when tracing and monitoring come first and evals run on top of production traces - for CI-first evaluation see [Opik](/evaluation/opik/) or [Deepeval](/evaluation/deepeval/).

## Resources

- [Website](https://langfuse.com/)
- [GitHub Repository](https://github.com/langfuse/langfuse)
