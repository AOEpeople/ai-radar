---
title: "Advanced & Modular RAG"
ring: adopt
segment: architecture-pattern
tags: [retrieval]
---

**RAG** ("Retrieval-Augmented Generation") is a now well established technique to use the cababilities of Large Language Model (LLM) together with information from external data stores (like custom knowlege). It enables LLMs to access external, up-to-date and specific informations. It also reduces "hallucinations" and enables domain-specific knowledge integration.


The implementation of advanced RAG and modular RAG systems have prooven to produce good results. 
When we talk about "advanced RAG" and "modular RAG", we are referring to the different RAG Paradigms, that are introduced in [Source (Gao et al.)](https://arxiv.org/pdf/2312.10997).

![ RAG compared with other model optimization. RAG Paradigms.](/images/rag-paradigms.png)

The following graphic also illustrates the different RAG paradigms:

![RAG Paradigms - technical details](/images/rag-paradims-insides.png)

## Advanced RAG

In an advanced RAG paradigm, pre-retrieval and post-retrieval phases are added to the naive RAG paradigm.

The phases of an advanced RAG system:

- Pre-retrieval — Query rewriting, query entity extraction, query expansion, etc.
- Retrieval of relevant context
- Post-retrieval: Reranking, pruning, extending, etc.
- Answer generation

## GraphRAG

Utilizes knowledge graphs during indexing and retrieval. See the extra article on [GraphRAG](/architecture-pattern/graph_rag/) for a deep dive.

## Modular RAG

A modular RAG system contains more complex patterns which involve orchestration and routing of the user query. Modular RAG and AI Agent pattern overlap.


## Agentic RAG

Agentic RAG introduces a reasoning agent that actively evaluates, reconciles, and refines retrieved information to provide more accurate data for the final response.

So instead of just retrieving and augmenting, an *agent like component* has access to retrieval tools (e.g. function calls) - and takes the task to retrieve and refine the knowlege - before it is passed to the main LLM call. 

This can be powerful - but the agentic layer is a significant increase in complexity and cost, and managing the retrieval, tool access and decision-making requires substantial engineering effort. This extra steps also lead to increased latency and the additional component is another source for potential misinterpretation and halluzination in the overall system.


## Related AI Radar articles:

* [Do not use Naive RAG for Large Knowledge Bases](/architecture-pattern/naive_rag_for_large_kb/)
* [Prompt Engineering](/architecture-pattern/prompt_engineering/) and [Context Engineering](/architecture-pattern/context_engineering/)
* [Evaluation Based Development](/architecture-pattern/evaluation_based_development/) as basis methods
