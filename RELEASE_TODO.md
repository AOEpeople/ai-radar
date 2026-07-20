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
- [x] CLAUDE.md aktualisiert (neuester Ordner = 2026-07-17, Update-Konvention dokumentiert)
- [x] **Segmente erweitert** (2026-07-19): `tools` umgewidmet zu **"Tools & Coding Agents"**
      (Id bleibt `tools`, keine Link-Brüche; Radar ist auf 6 Segmente begrenzt). Neue
      Coding-CLI-/Harness-Einträge kommen ins Segment `tools`

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
- [x] `browser-use.md` assess → **trial** (freigegeben 2026-07-19)
- [x] `crawl4ai.md` assess → **trial** (freigegeben 2026-07-19)
- [x] `mem0.md` assess → **trial** (freigegeben 2026-07-19)
- [x] `ragas.md` trial → **hold** (freigegeben 2026-07-19)
- [x] `langchain_evaluation.md` trial → **hold** + `featured: false` (freigegeben 2026-07-19)
- [x] `kotaemon.md` assess → **hold** + `featured: false` (freigegeben 2026-07-19)

## 2. Inhaltliche Updates (Ring bleibt)

Hohe Priorität (faktisch falsch geworden):
- [x] `llamaindex.md` — Update (freigegeben 2026-07-19, Titel jetzt "LlamaIndex & LlamaParse")
- [x] `langchain.md` — 1.0/1.x-Update (freigegeben 2026-07-19)
- [x] `langgraph.md` — 1.0-Update (freigegeben 2026-07-19)
- [x] `azure_openai.md` — ausgeblendet (`featured: false`), abgelöst durch neuen Eintrag
      `microsoft_foundry.md` (Entwurf, wartet auf Freigabe)
- [x] `openweb_ui.md` — Lizenzabschnitt (freigegeben 2026-07-19)
- [x] `gitleaks.md` — Feature-complete + Betterleaks-Verweis (freigegeben 2026-07-19)
- [x] `stackit-model-serving.md` — GA, neuer Name, Links (freigegeben 2026-07-19)
- [x] `model_leaderboards.md` — Sättigungs-These, AA-Index v4.1, METR, DeepSWE (freigegeben 2026-07-19)

Mittlere Priorität (wesentliche Lücken):
- [x] `prompt_injection_awareness.md` — Lethal Trifecta, architektonische Defenses, HITL,
      MCP-Risiken, NSA/CISA (freigegeben 2026-07-19)
- [x] `owasp_llm_top_10.md` — Agentic Top 10 mit ASI-Auszügen (freigegeben 2026-07-19)
- [x] `rag.md` — Agentic RAG als etabliertes Muster, Long-Context-Hybrid (freigegeben 2026-07-19)
- [x] `smart_vector_db_usage.md` — Hybrid+Reranking Default, agentisches Retrieval (freigegeben 2026-07-19)
- [x] ~~aws-bedrock, huggingface, ollama~~ — verworfen 2026-07-20: unsignifikant, alte Einträge bleiben
- [x] `replicate.md` — Cloudflare-Übernahme + Roadmap-Risiko (freigegeben 2026-07-20)
- [ ] `librechat.md` — ClickHouse-Übernahme, bleibt MIT (Eigentümerwechsel = entscheidungsrelevant)
- [x] ~~n8n.md~~ — übersprungen 2026-07-20 (unsignifikant nach neuer Messlatte)
- [ ] `multi_agent_system.md` — Framework-Liste ist irreführend geworden (AutoGen abgelöst, llama-agents tot)
- [ ] `evaluation_driven_development.md` — verweist auf Legacy "LangChain Evaluation" (jetzt hold); Agent-Evals
- [x] ~~prompt_engineering.md~~ — übersprungen 2026-07-20 (Grundlagen weiter gültig)
- [x] `garak.md` — Agent-Breaker-Probe, NVIDIA-Repo-Link (freigegeben 2026-07-19)
- [x] ~~phoenix.md~~ — übersprungen 2026-07-20 (unsignifikant nach neuer Messlatte)
- [x] `chroma-db.md` — Rust-Rewrite, Hybrid Search, Chroma Cloud (freigegeben 2026-07-19)
- [x] `weaviate.md` — v1.36/1.37, eingebauter MCP-Server (freigegeben 2026-07-19)
- [x] `sensitive_data_scanning.md` — PII-Guardrail-Pattern, Presidio (freigegeben 2026-07-19)
- [x] ~~llm-limitations.md, model_discovery.md, tool-finders.md~~ — übersprungen 2026-07-20
      (unsignifikant nach neuer Messlatte; alte Einträge bleiben)

## 3. Model News (neu: halbjährlich)

- [ ] Neu: `model_news_h2_25.md` — H2 2025 (GPT-5, gpt-oss-120b/20b, Opus 4.1/Sonnet 4.5, Grok 4,
      DeepSeek-V3.1, Kimi K2; GPT-5.1/5.2, Gemini 3 Pro/Flash, Opus 4.5, Kimi K2 Thinking)
- [ ] Neu: `model_news_h1_26.md` — H1 2026 (Opus 4.6, Gemini 3.1/3.5, GPT-5.5/5.6, DeepSeek V4,
      Sonnet 5, Qwen 3.5)
- [ ] Bestehende Q1/Q2-25-Artikel: im neuen Ordner konsolidieren oder ausblenden — Mechanik fürs
      Ausblenden im Radar-Tool prüfen und mit Daniel abstimmen

## 4. Neue Einträge (Auswahl durch Daniel)

- [x] Betterleaks (assess) — freigegeben 2026-07-19; 2026-07-20 ins Segment evaluation verschoben
- [x] **Segment `evaluation` erweitert** zu "Evaluation, Observability & Security";
      gitleaks + betterleaks verschoben, Pfade angepasst (freigegeben 2026-07-20)
- [x] Opik (evaluation, trial) — freigegeben 2026-07-20
- [x] Promptfoo (evaluation, assess) — freigegeben 2026-07-20
- [x] Inspect / UK AISI (evaluation, assess) — freigegeben 2026-07-20
- [x] **Coding-/Harness-Tools als separate Einträge** (freigegeben 2026-07-19):
      Claude Code (adopt), OpenAI Codex (adopt), OpenCode (adopt), Antigravity (trial);
      Tag `harness` in Readme.md + CLAUDE.md aufgenommen
- [x] **"Harness Engineering"** (architecture-pattern, trial) — inkl. Loops, Memory/Self-Improvement,
      HITL-Abschnitt (freigegeben & committet 2026-07-19)
- [ ] **LLM-Proxy/-Gateway (LiteLLM)** — gehört ins Radar; Segment noch offen
      (tools vs. models-platforms), Umfang klären (LiteLLM als Eintrag oder Pattern "LLM Gateway")

- [ ] Langfuse (evaluation, trial/adopt)
- [ ] Agentische Coding-CLIs: Claude Code, Codex, Gemini CLI (tools)
- [ ] Docling (data-features)
- [ ] OWASP Agentic Top 10 / Agentic Security (architecture-pattern)
- [ ] Microsoft Agent Framework (frameworks)
- [ ] Pydantic AI und/oder Mastra (frameworks)
- [ ] OpenRouter (models-platforms)
- [ ] **Mistral AI** (models-platforms, ggf. **trial**) — EU-Frontier-Anbieter/La Plateforme;
      im Eintrag auch kurz die Tools erwähnen (Vibe Box etc. — vor dem Schreiben recherchieren)
- [ ] IONOS AI Model Hub (models-platforms, EU-Sovereignty)
- [ ] Google Vertex AI (models-platforms — dritter Hyperscaler fehlt)
- [ ] **Text-to-SQL** (architecture-pattern) — neuer Artikel: was es kann (NL-Queries auf
      strukturierte Daten), Best Practices (Schema-Kontext, Views/Semantic Layer, Read-only-Zugriff,
      Validierung/Guardrails, Evaluation z. B. BIRD/Spider), Grenzen; vor dem Schreiben recherchieren
- [ ] Code Execution / "Code Mode" für Agent-Tools (architecture-pattern)
- [ ] Agent Memory als Pattern (architecture-pattern)

## 5. Abschluss

- [ ] Alle Links im neuen Release prüfen (Build lokal: `npm run serve`)
- [ ] Build-Check: CI schlägt fehl, wenn Workspace nach `npm run build` dirty ist
- [ ] Commit & Push (erst nach Gesamt-Freigabe)
