---
title: "Evaluation Driven AI Development"
ring: adopt
segment: architecture-pattern
tags: [evaluation]
---

Evaluation Driven AI Development is a recommended development practice for building and improving robust AI applications, emphasizing continuous evaluation and testing throughout the development lifecycle.

These evaluations—or “evals”—act as end-to-end tests for AI behavior. They measure output quality across defined dimensions such as relevance, correctness, helpfulness, or even fairness, using automated assertions, human judgments, and AI-assisted grading.

For us it is the **Test-driven-development** equivalent for AI systems.

## Motivation

Developing AI applications often involves trade-offs: improving quality for one question or use case can degrade results for others. Unlike traditional software, binary pass/fail testing is rarely possible. Instead, continuous benchmarking, trend analysis, and integration of real user feedback are required to evaluate and improve AI system quality.

## A new "AI-Native" development cycle

![EBAD](/images/evaluation-based-dev.png)

* Data
* Agent Development & Model selection
* Feedback: Implement Feedback that improve your evals. (Use "Red Teaming" to test "bad" cases. Collect real-world or test-user responses to outputs.)
* Evals: Define and measure evaluation criteria (e.g., accuracy, helpfulness, consistency). Track them over time to get a trend.

## Recommendation
Teams building AI products should treat evals as first-class development artifacts. Maintain them in version control, run them in CI/CD pipelines, and iterate against them as you would unit or integration tests in conventional systems. Evaluation Driven AI Development doesn’t eliminate subjectivity—it manages it.

## Tools

* [LangChain Evaluation](/evaluation/langchain_evaluation/)
* [Ragas](/evaluation/ragas/)
* [Deepeval](/evaluation/deepeval/)

