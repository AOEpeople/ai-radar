---
title: "OWASP Top 10 for LLM"
ring: adopt
segment: architecture-pattern
tags: [security, evaluation]
---

**Update 07/2026:** The 2025 LLM Top 10 described in our previous entry is still the current version. The important addition: in December 2025 OWASP published the separate **[Top 10 for Agentic Applications 2026](https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications-for-2026/)** (ASI01-ASI10) covering agent-specific risks.

Selected entries most relevant for our projects:

- **ASI01 Agent Goal Hijack** - attackers redirect the agent's objective via manipulated instructions, tool outputs or external content (the agentic escalation of prompt injection).
- **ASI02 Tool Misuse & Exploitation** - agents misuse legitimate tools through injection, misalignment or unsafe delegation.
- **ASI03 Identity & Privilege Abuse** - exploitation of inherited/cached credentials, delegated permissions and agent-to-agent trust.
- **ASI05 Unexpected Code Execution** - agents generate or execute attacker-controlled code (highly relevant for coding agents and code-executing tools).
- **ASI06 Memory & Context Poisoning** - persistent corruption of agent memory, RAG stores or contextual knowledge that silently degrades future sessions.
- **ASI09 Human-Agent Trust Exploitation** - a hijacked, fluent agent persuades the user to approve malicious actions or share sensitive data - approval flows are themselves an attack surface.

(Full list additionally covers agentic supply chain, insecure inter-agent communication, cascading failures and rogue agents.)

For agentic systems, apply **both** lists: the LLM Top 10 for the model/application layer, the ASI Top 10 for agency, tools and orchestration. See [Prompt Injection Awareness](/architecture-pattern/prompt_injection_awareness/) and [Harness Engineering](/architecture-pattern/harness_engineering/) for the architectural side of these mitigations.
