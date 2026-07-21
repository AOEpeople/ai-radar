---
title: "CubeSandbox"
ring: assess
segment: tools
tags: [harness]
---

CubeSandbox (Tencent Cloud, Apache 2.0) is a self-hostable sandbox infrastructure for securely running LLM-generated code - the isolation layer behind the [Code Execution](/architecture-pattern/code_execution/) pattern. It uses microVMs (rust-vmm + KVM, own guest kernel per sandbox) with eBPF-based network isolation, and its API is E2B-SDK-compatible.

- Reported <60ms cold start and thousands of sandboxes per node (vendor figures, not independently verified).
- **Very young** (public since ~July 2026, still 0.x with a high release churn) - production-readiness claims warrant caution.
- Self-hosted on own KVM hardware it is data-friendly; the Chinese-hyperscaler origin is a supply-chain/compliance consideration for some, so audit before production use. Needs Linux/KVM bare-metal or nested virtualization.

The de-facto reference in this space is E2B (Firecracker-based, OSS core); CubeSandbox is worth watching as a self-hosted alternative.

## Resources

- [GitHub Repository](https://github.com/TencentCloud/CubeSandbox)
