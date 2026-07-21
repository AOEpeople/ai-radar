---
title: "Prompt Injection Awareness"
ring: adopt
segment: architecture-pattern
tags: [security, prompting]
---

**Update 07/2026:** Prompt injection remains unsolved - but the defense thinking has matured beyond the filter-based mitigations in our previous entry. Input validation and guardrails are still important but alone are now considered insufficient for critical guards. You need **architectural** defense, enforced by the [harness](/architecture-pattern/harness_engineering/) - not by the model.

## The "Lethal Trifecta"

The now-standard mental model for agent exfiltration risk. An agent is exfiltration-prone **by construction** when it combines all three:

1. **Access to private data** - like sensitive files, databases, internal APIs, user context
2. **Exposure to untrusted content** - web pages, incoming mails/issues/tickets, third-party tool results
3. **An external communication channel** - HTTP requests, mail sending, writing to public locations

Design rule: **break at least one leg** per agent. Examples:
- A research agent that reads the web should not hold private credentials.
- An agent with database access should not be able to call arbitrary URLs.

## Architectural defense patterns

- **Plan-then-execute**: the agent fixes its plan *before* reading untrusted content - later content may influence parameters, but cannot add new actions.
- **Dual-LLM / quarantined model**: a model without any tool access processes untrusted content and returns only structured, constrained results to the privileged agent.
- **Capability policies in the harness**:
  - least-privilege tool access, allow/ask/deny rules
  - read-only defaults for tools that consume external content
  - separate agents/contexts per trust level instead of one agent with all permissions
- **Human-in-the-loop approvals** for critical actions (irreversible operations, external communication, credential use) - see the approval section in [Harness Engineering](/architecture-pattern/harness_engineering/). Beware approval fatigue: reserve approvals for genuinely critical actions, or users will click through them.

## New attack surfaces since our last entry

- **MCP-based injection**: tool descriptions and tool results of third-party [MCP](/architecture-pattern/mcp_model_context_protocol/) servers are untrusted input; a malicious or compromised server can steer the agent. Restrict allowed servers and review what they expose.
- **Web content targeting agents**: malicious injections placed in public web pages increased measurably since late 2025 - browsing agents are now an explicit target group.
- **Memory poisoning**: injected content that persists into agent memory silently compromises future sessions (see ASI06 in the [OWASP Agentic Top 10](/architecture-pattern/owasp_llm_top_10/)).

## Official guidance & testing

- [NSA/CISA guidance on MCP security (May 2026)](https://media.defense.gov/2026/Jun/02/2003943289/-1/-1/0/CSI_MCP_SECURITY.PDF)
- [OWASP Agentic Top 10](/architecture-pattern/owasp_llm_top_10/)
- Continuous red-teaming with [Garak](/evaluation/garak/) (now including agent-tool attack probes)
