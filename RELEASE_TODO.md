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
      `microsoft_foundry.md` (freigegeben 2026-07-19)
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
- [x] `librechat.md` — ClickHouse-Übernahme, bleibt MIT (freigegeben 2026-07-20)
- [x] ~~n8n.md~~ — übersprungen 2026-07-20 (unsignifikant nach neuer Messlatte)
- [x] `multi_agent_system.md` — Framework-Liste korrigiert, Supervisor-Pattern (freigegeben 2026-07-20)
- [x] `evaluation_driven_development.md` — Agent-Evals, Tool-Verweise korrigiert (freigegeben 2026-07-20)
- [x] ~~prompt_engineering.md~~ — übersprungen 2026-07-20 (Grundlagen weiter gültig)
- [x] `garak.md` — Agent-Breaker-Probe, NVIDIA-Repo-Link (freigegeben 2026-07-19)
- [x] ~~phoenix.md~~ — übersprungen 2026-07-20 (unsignifikant nach neuer Messlatte)
- [x] `chroma-db.md` — Rust-Rewrite, Hybrid Search, Chroma Cloud (freigegeben 2026-07-19)
- [x] `weaviate.md` — v1.36/1.37, eingebauter MCP-Server (freigegeben 2026-07-19)
- [x] `sensitive_data_scanning.md` — PII-Guardrail-Pattern, Presidio (freigegeben 2026-07-19)
- [x] ~~llm-limitations.md, model_discovery.md, tool-finders.md~~ — übersprungen 2026-07-20
      (unsignifikant nach neuer Messlatte; alte Einträge bleiben)

## 3. Model News (neu: halbjährlich)

- [x] `model_news_h2_25.md` — Trends-fokussiert, nach Playern gruppiert (freigegeben 2026-07-20)
- [x] `model_news_h1_26.md` — dito (freigegeben 2026-07-20)
- [x] Q1/Q2-25-Artikel per `featured: false` ausgeblendet (freigegeben 2026-07-20)
- [x] Neu: `model_news_h2_26.md` — laufender Artikel, Start mit Juli-Releases (freigegeben 2026-07-21)

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
- [x] LiteLLM/Presidio-Referenzen in `sensitive_data_scanning.md` internalisiert (2026-07-21)
- [x] Recherche Pseudonymisierung erledigt: kein klarer OSS-Leader — als Abschnitt im
      Presidio-Eintrag umgesetzt (LLM-Guard als Referenz-Implementierung)

- [x] Langfuse (evaluation, trial) — freigegeben 2026-07-21
- [x] Docling (data-features, trial) — freigegeben 2026-07-21
- [x] LiteLLM (tools, trial, mit Security-Caveat) — freigegeben 2026-07-21
- [x] Presidio (evaluation, trial; inkl. reversible Pseudonymisierung/LLM-Guard) — freigegeben 2026-07-21
- [x] Mistral AI (models-platforms, trial; Sovereign-Stack-Fokus) — freigegeben 2026-07-21
- [x] Text-to-SQL (architecture-pattern, trial) — freigegeben 2026-07-21
- [x] ~~OWASP Agentic Top 10 als eigener Artikel~~ — abgelehnt 2026-07-21 (in owasp_llm_top_10 referenziert)
- [x] ~~Microsoft Agent Framework~~ — abgelehnt 2026-07-21
- [x] **Pydantic AI** (frameworks, trial) — Entwurf, wartet auf Freigabe
- [x] **Context Hub** (architecture-pattern, trial) — Pattern-Entwurf (Daniel-Wunsch trotz nicht etabliertem Begriff)
- [x] **Open Knowledge Format (OKF)** (architecture-pattern, assess) — Entwurf
- [x] **Automation & AI Governance** (architecture-pattern, trial) — Entwurf
- [x] **CubeSandbox** (tools, assess) + **E2B Sandbox** (tools, assess) — Entwürfe
- [x] **AI-Assisted Penetration Testing** (evaluation, assess) — Sammelartikel: CAI, PentAGI, PentestGPT
- [x] ~~CloakBrowser~~ — weggelassen 2026-07-21 (primär Detection-Evasion, Dual-Use, passt nicht)
- [x] **Headroom** (tools, assess) — Entwurf
- [x] **Graphify** (tools, assess) — Entwurf
- [x] **SearXNG** (tools, trial) — Entwurf
- [x] **Graphiti** (Zep) (data-features, assess) — freigegeben 2026-07-21 (Review-Edits übernommen)
- [x] OpenRouter (models-platforms, trial) — freigegeben 2026-07-21
- [x] ~~IONOS AI Model Hub~~ — abgelehnt 2026-07-21
- [x] ~~Google Vertex AI~~ — abgelehnt 2026-07-21
- [x] **Segment `data-features` umbenannt** zu "Data, Extraction, Storage & Context"
      (2026-07-21; Id bleibt, Beschreibung modernisiert, Tippfehler "theire" gefixt)
- [x] **Code Execution / "Code Mode"** (architecture-pattern, trial) — Entwurf, wartet auf Freigabe
- [x] ~~Agent Memory als Pattern~~ — gestrichen 2026-07-21 (abgedeckt durch Harness Engineering,
      Context Engineering, mem0)
- [x] **Playwright MCP & CLI** (tools, trial) — freigegeben 2026-07-23
      (Nachzügler: Gegenstück zu Browser Use)
- [x] **pgvector** (data-features, trial) — freigegeben 2026-07-23, von Daniel gekürzt
      (im Einsatz in Kundenprojekten; Ops-Argument vs. dedizierte Vector-DBs)

## 5. Abschluss

- [x] Alle internen Links geprüft (2026-07-21): 2 Segment-Fehler im neuen Release gefixt
      (`/evaluation/` → `/architecture-pattern/` für evaluation_driven_development), plus 6 seit
      langem kaputte Links im Ordner 2025-03-14 repariert (mem0-, mcp-, gitleaks-,
      context-engineering-, evaluation_driven_development-Pfade)
- [x] Build-Check bestanden (2026-07-21): `npm run build` läuft durch, Workspace danach clean
- [x] Push `v2` → origin + PR nach `main` (2026-07-21)
