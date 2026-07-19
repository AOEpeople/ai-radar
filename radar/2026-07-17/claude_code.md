---
title: "Claude Code"
ring: adopt
segment: tools
tags: [harness, automation]
---

Claude Code is Anthropic's agentic coding tool - and currently the most complete [harness](/architecture-pattern/harness_engineering/) ecosystem. It runs as terminal CLI, IDE extension (VS Code/JetBrains), desktop app and on the web, with CI integrations for GitHub Actions and GitLab.

## Key Features

- **Layered extension system**: subagents with isolated context windows, deterministic hooks on lifecycle events (usable as programmable security policy), reusable skills, plugins and MCP client support.
- **Versioned project memory** via CLAUDE.md files - project knowledge lives in the repository, not in the tool.
- **Headless mode** (`claude -p`) as first-class citizen for CI and automation (PR review, issue triage, scheduled jobs).
- **Application-layer permission model**: allow/ask/deny rules per tool, optional OS sandbox.
- The engine is available as **Claude Agent SDK** for building custom agents.

## Assessment

Proprietary; usage requires a Claude subscription or API pay-per-token.

Related: [OpenAI Codex](/tools/openai_codex/), [OpenCode](/tools/opencode/), [Harness Engineering](/architecture-pattern/harness_engineering/)

## Resources

- [Documentation](https://code.claude.com/docs)
