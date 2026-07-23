---
title: "Google Antigravity"
ring: trial
segment: tools
tags: [harness]
---

Google Antigravity is Google's agentic development platform (launched November 2025, "Antigravity 2.0" since May 2026): an agent-first IDE, a standalone agent manager for parallel agents and scheduled tasks, a CLI (the official successor of the discontinued Gemini CLI free tier), a Python SDK and a managed-agents API.

## Key Features

- **Multi-agent orchestration** across editor, terminal and browser; agents produce verifiable "artifacts" (plans, screenshots, recordings).
- **Multi-model**: Gemini 3.x as default, plus Claude and open-weight models - models can be mixed per task.
- Free public preview with quotas tied to Google accounts/AI subscriptions.

## Assessment

Worth trialling, but with open eyes:

- **Closed source** (including the CLI) - a break from the Apache-2.0 Gemini CLI it replaces.
- **Security track record is mixed**: several prompt-injection/data-exfiltration findings since launch, a persistent code-execution issue via trusted workspaces and a critical RCE fixed in April 2026. If you trial it: enforce manual approval for terminal/browser actions and harden the browser allowlist.
- Rate limits in the free preview are intransparent; pricing after the preview is not final - do not build hard dependencies on current quotas.

Related: [Claude Code](/tools/claude_code/), [OpenAI Codex](/tools/openai_codex/), [OpenCode](/tools/opencode/), [Prompt Injection Awareness](/architecture-pattern/prompt_injection_awareness/)

## Resources

- [Website](https://antigravity.google/)
- [Google Developers Blog: Antigravity](https://developers.googleblog.com/build-with-google-antigravity-our-new-agentic-development-platform/)
