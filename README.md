# Hi, I'm Petr 👋

## AI Engineer · Reliable LLM Systems · RAG · Document Intelligence

I build AI systems for **document-heavy and enterprise workflows** — with measurable quality, explicit failure modes, and deterministic controls around LLM behavior.

**LLMs interpret. Code owns permissions, validation, state changes, and irreversible actions.**

📫 `petr.baldaev.ds@gmail.com` · Telegram: `@PetrBaldaev`  
💼 Open to AI Engineer / LLM Engineer roles

---

## Selected systems

| System | Problem | Engineering evidence |
|---|---|---|
| 🏭 **Water Treatment Analyzer** | Technical specification vs supplier proposal | Commercial pilot · expert-reviewed evaluation · deterministic numeric/unit validation |
| 🧩 **[Enterprise Employee Agent](https://github.com/spqr-86/enterprise-employee-agent)** | Knowledge + controlled enterprise actions | RBAC · typed commands · versioned confirmation · idempotency · transactions · audit |
| 🔎 **[Regulatory RAG](https://github.com/spqr-86/regulatory-rag)** | Evidence-grounded regulatory & corporate Q&A | HR@12 **0.81** · MRR **0.50** on held-out practitioner questions · explicit abstention |
| 🛠 **[Research State MCP](https://github.com/spqr-86/research-state-mcp)** | Research context, state & citation infrastructure | Model-free MCP · 272 tests · real MCP E2E · measured retrieval & citation evals |

---

### 🏭 Water Treatment Analyzer

Applied document intelligence for automated comparison of technical specifications against supplier proposals.

`PDF → parsing/OCR → requirement extraction → retrieval → gap analysis → deterministic validation → report`

Built for a commercial pilot. On the first site the client's process engineer reviewed the system's report and confirmed **105 of 109** requirement statuses; all four misses were over-cautious flags, not missed gaps. A harder site with cross-section references scored 72% in April; after fixes an approximate re-count gives 82–85% (requirement splitting changed, so not an exact comparison). Remaining failures are tracked by category.

**Why it matters:** the LLM handles document interpretation, while numeric/unit comparison and validation remain deterministic.

> Private commercial code and data. A sanitized public showcase is planned.

---

### 🧩 [Enterprise Employee Agent](https://github.com/spqr-86/enterprise-employee-agent)

An LLM-assisted enterprise workflow where the model can interpret requests, but **cannot authorize actions or mutate state**.

`user request → structured intent → authorization → versioned preview → explicit confirmation → idempotent mutation → audit event`

Built around strict Pydantic contracts, RBAC, deterministic state transitions, version-bound confirmation, atomic SQLite transactions and append-only audit history.

**Why it matters:** model behavior is constrained by software invariants rather than trusted to enforce business rules.

End-to-end employee → HR → manager flow with a server-rendered FastAPI demo; **464 tests**. Educational project on the public GitLab Handbook, not production.

---

### 🔎 [Regulatory RAG](https://github.com/spqr-86/regulatory-rag)

Evidence-gated RAG for regulatory and corporate knowledge where unsupported confidence is worse than explicit abstention.

Hybrid retrieval, reranking and evidence sufficiency gates are evaluated separately from generation. Retrieval: **HR@12 0.81, MRR 0.50** on 90 practitioner questions never used for tuning. Out-of-scope questions: abstained on 7/7. Generation faithfulness to retrieved sources (LLM judge): **0.974**. A 28 Sep legal audit found the generation golden set partly wrong, so the earlier correctness score is withdrawn and a new baseline is pending — the audit itself is part of the story.

**Why it matters:** failures can be attributed to retrieval, evidence sufficiency or generation instead of being hidden behind one end-to-end score.

---

### 🛠 [Research State MCP](https://github.com/spqr-86/research-state-mcp)

A **model-free** MCP layer for research state, relevant page fragments and citation-aware context.

Uses SQLite and FTS5 instead of adding embeddings or another LLM where they are not required. The suite includes **272 tests**, with end-to-end smoke scenarios through the real FastMCP client/server protocol. Retrieval and citation evals have directly changed implementation invariants, including ellipsis handling and minimum quote length.

**Why it matters:** architecture is driven by the problem and measured trade-offs, not by adding AI components by default.

---

## Engineering principles

- **Measure components separately.** Retrieval, generation, tool use and workflow behavior fail differently.
- **Keep deterministic logic deterministic.** Authorization, calculations, state transitions and irreversible actions belong in code.
- **Turn failures into tests.** Weak evidence, OOS queries, permissions, malformed outputs and adversarial inputs belong in evals.
- **Treat latency and cost as system metrics.** Quality alone is not enough for a usable AI system.

---

## Other work

[AI Agents Security Week (Yandex SHAD)](https://github.com/spqr-86/shad-security-week) — red team + blue team guardrail, certificate 179/200.

---

## Stack

**Python · FastAPI · Pydantic · PostgreSQL · SQLite · OpenAI · DeepSeek · Gemini · LangGraph · MCP · BM25 · dense retrieval · CrossEncoder reranking · Docker · GitHub Actions · pytest · Ruff**

---

Building **measurable, debuggable and controllable LLM systems** for real workflows.
