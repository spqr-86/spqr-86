# Hi, I'm Petr 👋

## AI Engineer · Reliable LLM Systems · RAG · Document Intelligence

I build AI systems for **document-heavy and enterprise workflows** — with measurable quality, explicit failure modes, and deterministic controls around LLM behavior.

**LLMs interpret. Code owns permissions, validation, state changes, and irreversible actions.**

📫 `petr.baldaev.ds@gmail.com` · Telegram: `@PetrBaldaev`  
💼 Open to AI Engineer / LLM Engineer roles

---

## What I build

- **Evidence-grounded retrieval systems** — hybrid search, reranking, explicit abstention and component-level evaluation.
- **Controlled LLM workflows** — the model interprets requests while permissions, validation, state transitions and irreversible actions stay deterministic.
- **Document intelligence pipelines** — extract, compare and validate information across complex enterprise documents, with failures tracked instead of hidden.

---

## Selected systems

| System | Problem | Engineering evidence |
|---|---|---|
| 🔎 **[Regulatory RAG](https://github.com/spqr-86/regulatory-rag)** | Evidence-grounded regulatory & corporate Q&A | HR@12 **0.81** · MRR **0.50** · faithfulness **0.926** · explicit abstention |
| 🛠 **[Research State MCP](https://github.com/spqr-86/research-state-mcp)** | Research context, state & citation infrastructure | Model-free MCP · 272 tests · real MCP E2E · measured retrieval & citation evals |
| 🧩 **[Enterprise Employee Agent](https://github.com/spqr-86/enterprise-employee-agent)** | Knowledge + controlled enterprise actions | In development · typed workflow architecture · deterministic authorization / confirmation boundaries |
| 🏭 **Water Treatment Analyzer** | Technical specification vs supplier proposal | Commercial pilot · expert-reviewed evaluation · deterministic numeric/unit validation |

---

### 🔎 [Regulatory RAG](https://github.com/spqr-86/regulatory-rag)

**Problem:** regulatory and corporate Q&A becomes unreliable when retrieval is weak but the model still answers confidently.

**Approach:** hybrid retrieval, reranking and evidence sufficiency gates are evaluated separately from generation, with explicit abstention when evidence is insufficient.

**Evidence:** current evaluation includes **HR@12 0.81, MRR 0.50, in-scope correctness 7.91/10 and faithfulness 0.926**, plus explicit out-of-scope and failure analysis.

**Why it matters:** failures can be attributed to retrieval, evidence sufficiency or generation instead of being hidden behind one end-to-end score.

---

### 🛠 [Research State MCP](https://github.com/spqr-86/research-state-mcp)

**Problem:** research agents need persistent state, relevant source fragments and reliable citations without adding another LLM or embedding layer by default.

**Approach:** a **model-free** MCP layer using SQLite and FTS5 for research state, retrieval and citation-aware context.

**Evidence:** **272 tests**, including end-to-end smoke scenarios through the real FastMCP client/server protocol. Retrieval and citation evals have directly changed implementation invariants, including ellipsis handling and minimum quote length.

**Why it matters:** architecture is driven by the problem and measured trade-offs, not by adding AI components by default.

---

### 🧩 [Enterprise Employee Agent](https://github.com/spqr-86/enterprise-employee-agent)

**Problem:** an LLM can interpret an employee request, but it should not be trusted to authorize actions or mutate enterprise state by itself.

**Approach:** a knowledge + typed workflow architecture for a controlled leave-of-absence flow, with deterministic boundaries around authorization, preview/confirmation, mutation and audit.

**Status:** public implementation is **in development**. The repository currently establishes the installable package, development framework, specification and local checks; product logic and the minimal corpus are being implemented.

**Target invariant:** the model interprets the request; software invariants own permissions and state-changing actions.

---

### 🏭 Water Treatment Analyzer

**Problem:** compare technical specifications against supplier proposals across document-heavy engineering workflows.

**Approach:**

`PDF → parsing/OCR → requirement extraction → retrieval → gap analysis → deterministic validation → report`

**Evidence:** built for a commercial pilot using domain-expert annotations. The strongest reviewed dataset reached **105/109 (96.3%)**; other evaluated document sets were approximately **75–85%**, with remaining failures tracked by category.

**Why it matters:** the LLM handles document interpretation, while numeric/unit comparison and validation remain deterministic.

> Private commercial code and data. A sanitized public showcase is planned.

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
