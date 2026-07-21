---
title: "Text-to-SQL"
ring: trial
segment: architecture-pattern
tags: [patterns]
---

Text-to-SQL lets users query structured data in natural language - the LLM generates SQL against a database schema. The technique is production-ready for internal analytics on well-curated domains, but its success depends almost entirely on context engineering, not on the model: on clean benchmarks the problem looks nearly solved (~82% on BIRD), while raw enterprise schemas without prepared context yield reported success rates of 10-30%.

## What works in 2026

- **Agentic loops instead of one-shot translation**: schema exploration, query execution against the live database and self-correction from execution feedback. The first correction pass brings the largest gain.
- **Semantic layer / curated views instead of raw schema** - the single most impactful practice. Metrics, dimensions and join paths are encoded explicitly; schema linking becomes a lookup instead of guessing.
- **Rich schema context**: column descriptions, sample values for categorical columns, known data pitfalls; for large schemas, retrieval over schema descriptions ("minimal viable schema" in context).
- **Curated few-shot examples**: verified question-SQL pairs retrieved per query; confirmed queries feed back into the example pool.
- **Validation before and after execution**: EXPLAIN/dry-run, row limits and timeouts before; plausibility checks and showing the generated SQL with an explanation after. Ask back on ambiguous questions instead of guessing.

## Security

- **Read-only enforced at the database level** via a dedicated role with SELECT on curated views. Never rely on prompt-level read-only checks only - they have been bypassed in practice (e.g. in a popular Postgres MCP server).
- Row-level security in the database, with the user identity passed through - not requested from the LLM via WHERE clauses.
- Treat database content and schema comments as untrusted input: [prompt injection](/architecture-pattern/prompt_injection_awareness/) can arrive through retrieved rows.

## Failure modes

The most dangerous one: **plausibly wrong numbers** - the query runs without error, the result looks right, but a wrong join path or missing filter silently distorts it. Ambiguous metrics ("revenue", "active customer") without a semantic layer, schema hallucination on large schemas and complex multi-table joins remain the weak points. Evaluate with your own question set (see [Evaluation Driven AI Development](/evaluation/evaluation_driven_development/)); public benchmarks are BIRD and Spider 2.0.

## Tools

Text-to-SQL pattern can be applied to custom agents, however there are already specialized tools that could be considered for certain use cases also. 

Established options are for example: Vanna (MIT, RAG over question-SQL pairs, since 2.0 agent-based with user identity/audit), Wren AI (open-source GenBI with its own semantic layer), MCP servers for direct agent-database access (e.g. Google MCP Toolbox for Databases)
