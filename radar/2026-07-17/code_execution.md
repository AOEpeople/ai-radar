---
title: "Code Execution / Code Mode"
ring: trial
segment: architecture-pattern
tags: [patterns]
---

Code Execution ("Code Mode") is the pattern of letting an agent **write and run code** as its primary way of working, instead of emitting many individual tool calls or trying to solve a task in prose. Two overlapping uses:

- **Code as the way to use tools**: instead of one model round per tool call - each intermediate result flowing back through the context - the agent writes code that orchestrates the tools (loops, filtering, parallel calls) and only the final result returns to the model. Anthropic reported large token savings from this; Cloudflare productized it as "Code Mode", Pydantic AI ships it as CodeMode.
- **Code as the way to do the work**: for data transformation, calculation, file and document processing the agent writes a script rather than reasoning token by token - more reliable and verifiable, and the natural mechanism behind [skills](/tools/claude_code/) that bundle reusable procedures.

## Considerations

- **Requires a sandbox**: generated code must run isolated (see the isolation discussion in [Harness Engineering](/architecture-pattern/harness_engineering/)) - untrusted code plus data access is a [prompt injection](/architecture-pattern/prompt_injection_awareness/) surface.
- Best fit for tasks with many steps, structured data or many tools; overkill for a single lookup.
- Verify outcomes against objective signals (tests, schema checks) rather than trusting that the code did the right thing.
