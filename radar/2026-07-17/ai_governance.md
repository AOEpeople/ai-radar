---
title: "Automation & AI Governance"
ring: trial
segment: architecture-pattern
tags: [security, patterns]
---

As AI automation and agents move into production, governance shifts from a compliance afterthought to an engineering concern. The EU AI Act becomes fully applicable on **2 August 2026** - most companies are affected as *deployers* (not providers), including Article 50 transparency duties for agents that interact with people or generate content.

Four building blocks worth establishing:

- **EU AI Act readiness as deployer**: role clarification, an AI inventory, transparency obligations.
- **Agent governance**: identity, permissions, audit trails and explicit human-in-the-loop boundaries for agents that act (see [Harness Engineering](/architecture-pattern/harness_engineering/) and the [OWASP Agentic Top 10](/architecture-pattern/owasp_llm_top_10/)).
- **Policies for coding agents**: allowed tools/models, code provenance, review duties, secrets handling.
- **Shadow-AI management**: governed enablement instead of prohibition - unmanaged AI use is widespread and costly when it goes wrong.

Established reference frameworks are **ISO/IEC 42001** (certifiable AI management system) and the **NIST AI RMF** (voluntary, risk-based); agent-specific runtime governance (identity/authorization standards) is emerging but not yet standardized.
