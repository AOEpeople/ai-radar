---
title: "Ollama"
ring: trial
segment: models-platforms
tags: [sovereignty]
---

[Ollama](https://ollama.com/) is a developer-focused platform for running large language models locally, with an emphasis on simplicity, portability, and data sovereignty. It abstracts away the complexity of model orchestration and provides a CLI and programmatic interface for running and managing open models—such as Llama 3, Llama 4, Mistral, Gemma 3, and more — on local machines.

## Key Features

- **Local-first execution**: Ollama enables developers to run models entirely on their own hardware, eliminating the need to rely on cloud-based APIs or remote inference endpoints. This is particularly relevant for use cases with strict data privacy or air-gapped environments.
- **Single-command model setup**: Models can be downloaded and run with a single command (`ollama run mistral`), making prototyping and experimentation straightforward.
- **Custom model support**: Developers can customize models using a lightweight `Modelfile`, similar in spirit to Dockerfiles. This encourages reproducible builds and easier sharing across environments.
- **GPU support**: Ollama takes advantage of local GPU hardware for accelerated inference, with fallback to CPU where necessary.
- **Function calling/tools**: Models can utilize tools to perform external functions and access external data sources, enabling more complex workflows.
- **OpenAI compatibility**: The platform offers compatibility with the OpenAI Chat Completions API, allowing developers to use existing OpenAI-based tooling with local models.
- **Python and JavaScript libraries**: Official libraries are available for seamless integration with applications in these languages.
- **Structured outputs**: Models can be constrained to produce output in specific formats defined by JSON schema.

## Engineering Considerations

While Ollama lowers the entry barrier to working with open models, there are caveats:

- **Limited scalability**: It is best suited for individual developer use or edge deployments. For production-scale inference, engineers may prefer orchestration platforms like [vLLM](https://github.com/vllm-project/vllm) or [TGI](https://github.com/huggingface/text-generation-inference).
- **Model compatibility**: Ollama focuses on optimized models in GGUF format and other compatible architectures, though the range of supported models has expanded significantly.

## Links

- [Ollama GitHub](https://github.com/ollama/ollama)
- [List of supported models](https://ollama.com/library)
- [Python Library](https://github.com/ollama/ollama-python)
- [JavaScript Library](https://github.com/ollama/ollama-js)
