---
title: "E2B Sandbox"
ring: assess
segment: tools
tags: [harness]
---

E2B is the de-facto reference for securely running LLM-generated code: Firecracker-based microVM sandboxes with an SDK (Python/TS) that spins up isolated environments in ~150ms - the isolation layer behind the [Code Execution](/architecture-pattern/code_execution/) pattern. Its API has become the standard others emulate (e.g. [CubeSandbox](/tools/cubesandbox/) advertises E2B compatibility).

- OSS core plus a managed cloud; microVM isolation is the accepted security bar for untrusted agent code ("a container is not a sandbox").
- Alternatives by requirement: Daytona (fastest provisioning), Modal (GPU in the sandbox), microsandbox / CubeSandbox (self-hosted).

## Resources

- [Website](https://e2b.dev/)
- [GitHub Repository](https://github.com/e2b-dev/E2B)
