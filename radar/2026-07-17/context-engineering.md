---
title: "Context Engineering"
ring: adopt
segment: architecture-pattern
tags: [prompting, patterns]
---

**Update 07/2026 (trial → adopt):** Context engineering has moved from an emerging term to an established core practice in AI engineering. Anthropic, Google and most agent framework vendors have published formal guidance - the guiding principle: find the smallest set of high-signal tokens that maximizes the likelihood of the desired outcome.

Additions to our previous entry:

- **Compaction:** For long-running agents, summarize the conversation state when the window fills up and restart with the summary plus the most recent messages. Test compaction carefully - badly tuned summaries silently drop constraints and task state.
- **Context isolation via sub-agents:** Delegate self-contained subtasks to separate agent contexts and return only condensed results to the main context, instead of letting one context accumulate everything.
- **Context windows have grown** (typically 200k tokens, up to millions for some models) - but long contexts degrade attention ("context rot") and increase latency and cost, so careful curation remains essential even with large windows.

Further reading: [Effective context engineering for AI agents (Anthropic)](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents)
