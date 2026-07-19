---
title: "replicate.ai"
ring: trial
segment: models-platforms
tags: [platform, model-serving]
---

**Update 07/2026:** **Cloudflare acquired Replicate** (announced November 2025, closed early 2026). Replicate continues as its own brand and the API is unchanged, with ongoing integration into Cloudflare Workers AI ([announcement](https://blog.cloudflare.com/replicate-joins-cloudflare/)).

What this means practically:

- Short term: business as usual; the model catalog and Cog-based custom deployments work as before.
- Medium term: the product roadmap (standalone vs. Workers-AI convergence, pricing) is not yet settled - factor this uncertainty into new platform decisions and avoid deep coupling to Replicate-specific APIs where cheap to do.
