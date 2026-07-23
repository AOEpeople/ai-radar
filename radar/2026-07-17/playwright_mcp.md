---
title: "Playwright MCP & CLI"
ring: trial
segment: tools
tags: [automation, harness]
---

[Playwright MCP](https://github.com/microsoft/playwright-mcp) is Microsoft's official [MCP](/architecture-pattern/mcp_model_context_protocol/) server that gives agents a real browser. Its key idea: the agent sees **accessibility-tree snapshots** instead of screenshots - structured, deterministic and far more token-efficient than vision-based control. It has become the default way to connect coding agents (Claude Code, Copilot & co.) to a browser, e.g. to verify web UIs they just built.

- **Playwright CLI**: since mid-2026 Microsoft recommends the CLI variant for coding agents - each action runs as a shell command, artifacts go to disk instead of the model context (~4x fewer tokens). MCP remains the fit for long autonomous browser loops.
- **Playwright Test Agents** (planner / generator / healer) generate and self-heal Playwright tests - promising, but expect to review everything they produce.

Distinction from [Browser Use](/data-features/browser-use/): Playwright MCP/CLI is a deterministic tool layer that *your* agent drives - you own the loop and the harness. Browser Use is an opinionated agent library with its own loop and cloud offering, geared towards scraping and extraction.


## Team Insights

We use Playwright MCP in coding-agent workflows to let agents verify frontend changes themselves (open page, click through, check the result) - a feedback loop that improves results in the sense of [Harness Engineering](/architecture-pattern/harness_engineering/).

## Recommendation

Default choice when an agent needs a browser. Treat visited pages as untrusted input ([Prompt Injection Awareness](/architecture-pattern/prompt_injection_awareness/)) and prefer the CLI variant for token-sensitive coding-agent setups.
