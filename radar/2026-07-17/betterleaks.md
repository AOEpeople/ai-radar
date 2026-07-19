---
title: "Betterleaks"
ring: assess
segment: data-features
tags: [security]
---

Betterleaks is the successor of [Gitleaks](/data-features/gitleaks/), started in February 2026 by the original Gitleaks author (who no longer controls the Gitleaks repository and declared it feature-complete). MIT-licensed, backed by Aikido Security.

## What is different from Gitleaks

- **Token-efficiency detection instead of Shannon entropy**: uses BPE tokenization to distinguish real credentials from random-looking strings - the author reports significantly higher recall on CredData (self-reported, not independently verified yet).
- **Secret validation**: CEL-based HTTP checks whether found secrets are still active, reducing noise from revoked credentials.
- Recursive decoding (base64/hex/percent/unicode) by default and parallelized git scanning (reported 4-5x faster).
- **Drop-in replacement**: existing Gitleaks configs and CLI flags work unchanged.

## Assessment

Very fast release cadence (v1.0 to v1.6 within five months) and an experienced maintainer, but the project is young and the community/rule ecosystem is still small compared to Gitleaks. Recommended approach: run Betterleaks in parallel to Gitleaks on a pilot repository and compare findings - no urgent migration needed as long as Gitleaks receives security patches.

## Resources

- [GitHub Repository](https://github.com/betterleaks/betterleaks)
- [Website](https://betterleaks.com/)
