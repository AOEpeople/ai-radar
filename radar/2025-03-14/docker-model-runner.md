---
title: "Docker Model Runner (Beta)"
ring: assess
segment: models-platforms
tags: [model-serving, sovereignty]
---

Docker has released [Model Runner](https://docs.docker.com/desktop/features/model-runner/), a CLI tool that standardizes local inference of AI models. (Any maybe also for production in the future)

With a single `docker model run <<modelname>> "Hi"` command, developers can launch a model as simple as launching a container.

Simelar to [Ollama](models-platforms/ollama/), it uses [llama.cpp](https://github.com/ggml-org/llama.cpp)

Model Runner is ideal for:

- Local testing before deployment.
- Working with OpenAI-compatible API.

## Links
- [Docker Model Runner](https://docs.docker.com/desktop/features/model-runner/)
- [Docker Gen AI Catalog](https://hub.docker.com/catalogs/gen-ai)
- [Model Runner GitHub](https://github.com/docker/model-runner)
