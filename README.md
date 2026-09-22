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
| 🧩 **Enterprise Employee Agent** | Knowledge + controlled enterprise actions | RBAC · typed commands · versioned confirmation · idempotency · transactions · audit |
| 🔎 **[Regulatory RAG](https://github.com/spqr-86/regulatory-rag)** | Evidence-grounded regulatory & corporate Q&A | HR@12 **0.81** · MRR **0.50** · faithfulness **0.926** · explicit abstention |
| 🛠 **[Research State MCP](https://github.com/spqr-86/research-state-mcp)** | Research context, state & citation infrastructure | Model-free MCP · SQLite/FTS5 · measured context/citation trade-offs |

---

### 🏭 Water Treatment Analyzer

Applied document intelligence for automated comparison of technical specifications against supplier proposals.

`PDF → parsing/OCR → requirement extraction → retrieval → gap analysis → deterministic validation → report`

Built for a commercial pilot using domain-expert annotations. The strongest reviewed dataset reached **105/109 (96.3%)**; other evaluated document sets were approximately **75–85%**, with remaining failures tracked by category.

**Why it matters:** the LLM handles document interpretation, while numeric/unit comparison and validation remain deterministic.

> Private commercial code and data. A sanitized public showcase is planned.

---

### 🧩 Enterprise Employee Agent

An LLM-assisted enterprise workflow where the model can interpret requests, but **cannot authorize actions or mutate state**.

`user request → structured intent → authorization → versioned preview → explicit confirmation → idempotent mutation → audit event`

Built around strict Pydantic contracts, RBAC, deterministic state transitions, version-bound confirmation, atomic SQLite transactions and append-only audit history.

**Why it matters:** model behavior is constrained by software invariants rather than trusted to enforce business rules.

> Private while the integrated application layer and demo are being completed.

---

### 🔎 [Regulatory RAG](https://github.com/spqr-86/regulatory-rag)

Evidence-gated RAG for regulatory and corporate knowledge where unsupported confidence is worse than explicit abstention.

Hybrid retrieval, reranking and evidence sufficiency gates are evaluated separately from generation. Current evaluation includes **HR@12 0.81, MRR 0.50, in-scope correctness 7.91/10, faithfulness 0.926**, plus explicit out-of-scope and failure analysis.

**Why it matters:** failures can be attributed to retrieval, evidence sufficiency or generation instead of being hidden behind one end-to-end score.

---

### 🛠 [Research State MCP](https://github.com/spqr-86/research-state-mcp)

A **model-free** MCP layer for research state, relevant page fragments and citation-aware context.

Uses SQLite and FTS5 instead of adding embeddings or another LLM where they are not required. Experiments measure context-recall and citation-validation trade-offs and feed results back into design decisions.

**Why it matters:** architecture is driven by the problem and measured trade-offs, not by adding AI components by default.

---

## Engineering principles

- **Measure components separately.** Retrieval, generation, tool use and workflow behavior fail differently.
- **Keep deterministic logic deterministic.** Authorization, calculations, state transitions and irreversible actions belong in code.
- **Turn failures into tests.** Weak evidence, OOS queries, permissions, malformed outputs and adversarial inputs belong in evals.
- **Treat latency and cost as system metrics.** Quality alone is not enough for a usable AI system.

---

## Other engineering work

[Corporate Knowledge Assistant](https://github.com/spqr-86/corporate-knowledge-assistant) ·
[ERC3 Agents](https://github.com/spqr-86/erc3-agents) ·
[Customer Support Chatbot](https://github.com/spqr-86/customer-support-chatbot)

---

## Stack

**Python · FastAPI · Pydantic · PostgreSQL · SQLite · OpenAI · DeepSeek · Gemini · LangGraph · MCP · BM25 · dense retrieval · CrossEncoder reranking · Docker · GitHub Actions · pytest · Ruff**

---

Building **measurable, debuggable and controllable LLM systems** for real workflows.
