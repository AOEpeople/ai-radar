# Release 2026-07-17 — ToDo

Arbeitsmodus: Claude erstellt pro Punkt einen Entwurf im neuen Release-Ordner `radar/2026-07-17/`,
**Daniel gibt jede Änderung frei**, erst dann gilt der Punkt als erledigt.
Gearbeitet wird auf Branch **`v2`**, Merge nach `main` per Pull Request.

Mechanik: Das Frontend zeigt die **Historie** eines Artikels (alter Eintrag, danach der neue).
Update-Dateien in `radar/2026-07-17/` wiederholen den Artikel daher NICHT, sondern enthalten nur
Frontmatter (ggf. mit neuem Ring), die Änderungen und eine kurze Begründung
(Einstieg z. B. `**Update 07/2026 (trial → adopt):** …`). Komplett neue Artikel entstehen als
Volltext direkt dort ("New"). Der alte Ordner `radar/2025-03-14/` bleibt unangetastet — Artikel
verschwinden im Radar nicht, sie werden im neuen Ordner aktualisiert (ggf. auch Ausblenden).

## 0. Setup & Entscheidungen

- [x] Neuen Release-Ordner `radar/2026-07-17/` anlegen
- [x] Branch `v2` angelegt (PR nach `main` am Ende)
- [x] Gestagte `radar/2025-03-14/model_news_q3_25.md` unstaged und entfernt — Inhalt wird korrekt
      recherchiert neu geschrieben (siehe Abschnitt 3)
- [x] Modell-News-Format entschieden: **halbjährliche Sammel-Artikel**, die im jeweiligen
      Release-Ordner aktualisiert werden
- [ ] CLAUDE.md aktualisieren (neuester Ordner = 2026-07-17, Branch-/PR-Workflow)

## 1. Ring-Änderungen (Kopie + Frontmatter + kurzer Update-Absatz)

- [x] `mcp_model_context_protocol.md` trial → **adopt** (freigegeben 2026-07-18)
- [x] `context-engineering.md` trial → **adopt** (freigegeben 2026-07-18)
- [x] `vercel-ai-sdk.md` trial → **adopt** (freigegeben 2026-07-18)
- [ ] ~~`deepeval.md` trial → adopt~~ **zurückgestellt** (2026-07-18): aktuell schlechte Erfahrungen
      mit der Confident-AI-Plattform — Update erst, wenn Team-Einschätzung wieder klar ist
- [x] `qdrant.md` trial → **adopt** (freigegeben 2026-07-19)
- [x] `a2a.md` assess → **trial** (freigegeben 2026-07-19)
- [x] `crew-ai.md` assess → **trial** (freigegeben 2026-07-19)
- [x] `docker-model-runner.md` assess → **trial** (freigegeben 2026-07-19)
- [ ] `browser-use.md` assess → **trial** (+ CDP statt Playwright — Kernaussage korrigieren)
- [ ] `crawl4ai.md` assess → **trial** (+ v0.8/0.9, Docker-API, Security-Hinweise)
- [ ] `mem0.md` assess → **trial** (+ v2.0, Breaking-Changes-Hinweis, Series A)
- [ ] `ragas.md` trial → **hold** (+ Repo-Umzug zu vibrantlabsai, v0.4)
- [ ] `langchain_evaluation.md` trial → **hold** ODER Rewrite zu "LangSmith / OpenEvals / AgentEvals"
- [ ] `kotaemon.md` assess → **hold** (keine Releases seit Mai 2025)

## 2. Inhaltliche Updates (Ring bleibt)

Hohe Priorität (faktisch falsch geworden):
- [ ] `llamaindex.md` — Rewrite (Workflows als Kern-Abstraktion, llama_deploy, Links)
- [ ] `langchain.md` — 1.0/1.x-Update (create_agent, Middleware, docs.langchain.com)
- [ ] `langgraph.md` — 1.0-Update, Rolle als Runtime, tote Links
- [ ] `azure_openai.md` — GPT-5.x, Retirement-Hinweis, "Microsoft Foundry"-Branding
- [ ] `openweb_ui.md` — Lizenzabschnitt ergänzen (nicht mehr OSI-konform, White-Label kostenpflichtig)
- [ ] `gitleaks.md` — Feature-complete-Status, Nachfolger Betterleaks erwähnen
- [ ] `stackit-model-serving.md` — GA statt Beta, neuer Name, Link fixen (utm-Parameter raus)
- [ ] `model_leaderboards.md` — HF Open LLM Leaderboard raus; SWE-bench Verified, Terminal-Bench,
      OSWorld, ARC-AGI-2, BFCL V4 rein; Hinweis Benchmark-Sättigung; Tippfehler

Mittlere Priorität (wesentliche Lücken):
- [ ] `prompt_injection_awareness.md` — Lethal Trifecta, architektonische Defenses, MCP-Risiken, NSA/CISA-Guidance
- [ ] `owasp_llm_top_10.md` — Verweis auf OWASP Agentic Top 10 (ASI01–ASI10)
- [ ] `rag.md` — Agentic RAG relativieren, Long-Context-Hybrid
- [ ] `smart_vector_db_usage.md` — Hybrid Search + Reranking als Default, agentisches Retrieval
- [ ] `aws-bedrock.md` — AgentCore statt "Bedrock Agents", Modellliste
- [ ] `huggingface.md` — Zahlen aktualisieren, Inference Providers
- [ ] `ollama.md` — Cloud-Angebot, Sovereignty-Einordnung, Modellliste
- [ ] `replicate.md` — Cloudflare-Übernahme + Roadmap-Risiko
- [ ] `librechat.md` — ClickHouse-Übernahme (bleibt MIT), 2026-Roadmap
- [ ] `n8n.md` — SAP-Investment, Series C, Integrations-Zahl
- [ ] `multi_agent_system.md` — Framework-Liste (MS Agent Framework, OpenAI/Claude/Google SDKs), Supervisor-Pattern
- [ ] `evaluation_driven_development.md` — Agent-Evaluation ergänzen, Tool-Verweise
- [ ] `prompt_engineering.md` — Reasoning-Modelle, Verzahnung mit Context Engineering
- [ ] `garak.md` — Agent-Breaker-Probe, NVIDIA-Repo-Link
- [ ] `phoenix.md` — v17, Phoenix Intelligence, Doku-Link
- [ ] `chroma-db.md` — Rust-Rewrite, Hybrid Search, Chroma Cloud
- [ ] `weaviate.md` — v1.36/1.37, eingebauter MCP-Server
- [ ] `sensitive_data_scanning.md` — PII-Guardrail-Pattern (Gateway/Proxy), Presidio
- [ ] `llm-limitations.md` — Hallucination-Paper 2025, Reasoning-Halluzinationen, LinkedIn-Link ersetzen
- [ ] `model_discovery.md` — Gateways/Router, agentische Kriterien, EU AI Act
- [ ] `tool-finders.md` — Liste kuratieren (agentische Coding-Tools, Sora/Veo, Lovable)

## 3. Model News (neu: halbjährlich)

- [ ] Neu: `model_news_h2_25.md` — H2 2025 (GPT-5, gpt-oss-120b/20b, Opus 4.1/Sonnet 4.5, Grok 4,
      DeepSeek-V3.1, Kimi K2; GPT-5.1/5.2, Gemini 3 Pro/Flash, Opus 4.5, Kimi K2 Thinking)
- [ ] Neu: `model_news_h1_26.md` — H1 2026 (Opus 4.6, Gemini 3.1/3.5, GPT-5.5/5.6, DeepSeek V4,
      Sonnet 5, Qwen 3.5)
- [ ] Bestehende Q1/Q2-25-Artikel: im neuen Ordner konsolidieren oder ausblenden — Mechanik fürs
      Ausblenden im Radar-Tool prüfen und mit Daniel abstimmen

## 4. Neue Einträge (Auswahl durch Daniel)

- [ ] Langfuse (evaluation, trial/adopt)
- [ ] Agentische Coding-CLIs: Claude Code, Codex, Gemini CLI (tools)
- [ ] Docling (data-features)
- [ ] OWASP Agentic Top 10 / Agentic Security (architecture-pattern)
- [ ] Microsoft Agent Framework (frameworks)
- [ ] Pydantic AI und/oder Mastra (frameworks)
- [ ] OpenRouter (models-platforms)
- [ ] Mistral La Plateforme / IONOS AI Model Hub (models-platforms, EU-Sovereignty)
- [ ] Google Vertex AI (models-platforms — dritter Hyperscaler fehlt)
- [ ] Code Execution / "Code Mode" für Agent-Tools (architecture-pattern)
- [ ] Agent Memory als Pattern (architecture-pattern)

## 5. Abschluss

- [ ] Alle Links im neuen Release prüfen (Build lokal: `npm run serve`)
- [ ] Build-Check: CI schlägt fehl, wenn Workspace nach `npm run build` dirty ist
- [ ] Commit & Push (erst nach Gesamt-Freigabe)
