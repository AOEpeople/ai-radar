---
title: "Harness Engineering"
ring: trial
segment: architecture-pattern
tags: [patterns, harness]
---

A **harness** is the scaffolding around an LLM that turns it into a working agent: the tool loop, file/shell/browser access, permission system, context management and feedback cycle. "Harness engineering" is the emerging discipline of designing this layer deliberately - the 2026 counterpart to [Context Engineering](/architecture-pattern/context-engineering/) on the execution side. The quality of an agent is determined at least as much by its harness as by the underlying model.

## Core concerns

- **Tool and permission design**: least-privilege tool access, allow/ask/deny policies, hooks as programmable checkpoints. The harness is your enforcement point against [prompt injection](/architecture-pattern/prompt_injection_awareness/) - the model itself cannot be one.
- **Isolation strategy**: two established philosophies - OS-level sandboxing (default-deny kernel isolation, e.g. Codex) vs. application-layer permissions (rules + hooks, e.g. Claude Code). Choose per threat model; combine for untrusted inputs.
- **Human in the loop & approvals**: critical tool access (irreversible operations, external communication, credential use, production systems) gets an explicit approval gate - synchronous prompts in interactive use, asynchronous review queues in headless setups. Most harnesses support this natively (allow/ask/deny rules, tool-approval APIs like `needsApproval`, MCP elicitation). Two design rules: reserve approvals for genuinely critical actions (approval fatigue turns gates into rubber stamps), and treat the approval UI itself as attack surface - a hijacked agent can phrase requests persuasively (see ASI09 in the [OWASP Agentic Top 10](/architecture-pattern/owasp_llm_top_10/)).
- **Context files as portable knowledge**: project conventions live in versioned files (CLAUDE.md/AGENTS.md), custom commands and MCP servers - not in tool-specific settings. This keeps the harness **exchangeable** and avoids lock-in.
- **Headless operation**: design agent workflows to run non-interactively (CI, scheduled jobs, PR automation) with explicit budgets and gates instead of interactive approvals.
- **Feedback quality**: agents are only as good as the signals the harness feeds back - fast tests, linters, typed errors and structured tool outputs beat raw logs. See [Evaluation Driven AI Development](/evaluation/evaluation_driven_development/) for measuring agent workflows.

## Loops and loop engineering

The agent loop itself is a design surface, not a given. Loop engineering means deciding deliberately:

- **Loop shape**: a single generate→verify→fix cycle, a plan-then-execute split, or fan-out to subagents whose results are verified and merged. The shape determines cost, latency and reliability more than the model choice.
- **Termination and budgets**: explicit stopping conditions (tests green, N iterations, token budget) instead of "until the model thinks it is done" - unbounded loops burn budget and drift.
- **Verification inside the loop**: every iteration should end against an objective signal (test run, build, schema validation). A loop that only re-reads its own output converges on confident nonsense.
- **Long-running loops**: combine compaction (see [Context Engineering](/architecture-pattern/context-engineering/)) with externalized state - progress files or issue trackers the agent reads back - so work survives context resets.

## Memory and self-improvement

Harnesses increasingly persist knowledge across sessions:

- **Project memory**: conventions, decisions and known pitfalls in versioned context files - curated by humans, updated after retrospectives.
- **Agent-maintained memory**: the agent writes back what it learned (failed approaches, environment quirks). Powerful, but treat it as untrusted input to future sessions - poisoned or stale memory silently degrades every following run.
- **Self-improvement loops**: agents updating their own instructions, skills or tool configurations. Emerging practice with real leverage, but govern it like code: memory and instruction changes belong in version control and code review, not applied silently.

## Recommendation

Treat the harness as an architecture decision, not a tool preference: define the permission/isolation model, the shared context-file conventions and the CI patterns once - then concrete tools ([Claude Code](/tools/claude_code/), [OpenAI Codex](/tools/openai_codex/), [OpenCode](/tools/opencode/)) become swappable implementations.

## Resources

- [Effective harnesses for long-running agents (Anthropic)](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [MCP](/architecture-pattern/mcp_model_context_protocol/) as the interoperability layer across harnesses
