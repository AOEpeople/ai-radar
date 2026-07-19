---
title: "OpenAI Codex"
ring: adopt
segment: tools
tags: [harness, automation]
---

OpenAI Codex is OpenAI's agentic coding system: an open-source CLI (Apache 2.0, written in Rust) plus IDE extensions, cloud agents and integration into the ChatGPT desktop app. Powered by the GPT-5.x model family.

## Key Features

- **OS-level sandboxing by default** (macOS Seatbelt, Linux Landlock/seccomp, network off unless allowed) - Codex's main differentiator.
- Feature set on par with [Claude Code](/tools/claude_code/): subagents, hooks, MCP support, auto-review.
- **Cloud handoff**: start tasks locally, delegate long-running work to cloud agents and review results asynchronously.
- Headless execution (`codex exec`) for CI and automation.

## Assessment

The open-source CLI lowers the entry barrier, but model usage requires a ChatGPT plan or API access. Strong choice for teams standardized on OpenAI models or with strict process-isolation requirements.

Related: [Claude Code](/tools/claude_code/), [OpenCode](/tools/opencode/), [Harness Engineering](/architecture-pattern/harness_engineering/)

## Resources

- [Codex CLI Repository](https://github.com/openai/codex)
- [Codex Documentation](https://developers.openai.com/codex/)
