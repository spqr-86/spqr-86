# Hi, I'm Petr 👋

## AI Engineer · Reliable LLM Systems · RAG · Document Intelligence

I build AI systems where **LLMs handle interpretation, while application code owns validation, permissions, state changes, and other deterministic decisions**.

My focus is moving beyond demos: measurable retrieval, grounded answers, explicit failure modes, controlled workflows, evaluation, latency and cost.

📫 `petr.baldaev.ds@gmail.com` · Telegram: `@PetrBaldaev`  
💼 Open to AI Engineer / LLM Engineer roles

---

## Featured projects

### 🏭 Water Treatment Analyzer — real-world document intelligence

Commercial pilot for automated comparison of technical specifications against supplier proposals.

`PDF → parsing/OCR → requirement extraction → per-requirement retrieval → gap analysis → deterministic validation → PDF/Excel report`

- BM25 retrieval per requirement instead of whole-document prompting
- structured LLM outputs and citation validation
- deterministic comparison of engineering values and units
- evaluated on expert annotations from domain engineers
- **96.3% (105/109)** on the strongest reviewed benchmark

**Signal:** applied AI on real technical documents, with domain-expert evaluation and deterministic checks around the LLM.

> Private commercial repository; a sanitized public showcase is planned.

---

### 🔎 [Regulatory RAG](https://github.com/spqr-86/regulatory-rag) — reliable retrieval & evaluation

Evidence-gated RAG for regulatory and corporate knowledge where an unsupported confident answer is worse than an explicit abstention.

- hybrid BM25 + dense retrieval + CrossEncoder reranking
- deterministic routing and evidence sufficiency gates
- two-stage retrieval with explicit abstention
- retrieval and generation evaluated separately
- documented failed experiments and known limitations
- FastAPI + Streamlit + Postgres/Grafana observability

| Metric | Result |
|---|---:|
| Retrieval HR@12 | **0.81** |
| MRR | **0.50** |
| In-scope correctness | **7.91 / 10** |
| Faithfulness | **0.926** |
| Answer relevance | **0.887** |
| OOS abstention | **100% on current test subset** |
| Cost | **~$0.0066/query** |

**Signal:** I can design, evaluate and debug retrieval systems instead of treating RAG as a black box.

---

### 🧩 Enterprise Employee Agent — controlled LLM workflows

Enterprise HR assistant combining grounded knowledge retrieval with a deterministic business workflow.

`grounded answer → clarification → typed command → versioned preview → explicit confirmation → idempotent mutation → audit event`

- strict Pydantic contracts
- role-based access control
- deterministic state machine
- version-bound confirmation
- idempotent commands and atomic SQLite transactions
- append-only audit history
- structured LLM answer and citation contracts
- extensive unit, integration and smoke testing

**Signal:** the LLM can assist with interpretation, but authorization and state changes remain owned by code.

> Private while the integrated application layer and demo interface are being completed.

---

### 🤖 [Corporate Knowledge Assistant](https://github.com/spqr-86/corporate-knowledge-assistant) — agents, MCP & HITL

Enterprise knowledge/action agent built as a Google AI Agents capstone.

- coordinator + domain agent
- MCP knowledge retrieval
- deterministic context and denial-of-wallet guardrails
- permission-aware retrieval
- action tools for PTO drafts and HR tickets
- human-in-the-loop escalation
- cross-session memory
- golden-set agent evaluation

The eval suite found a real jurisdiction-guardrail bug caused by substring matching; it was fixed and covered with a regression test.

**Signal:** agents and tools are useful when they add controlled actions and escalation — not just more orchestration.

---

## Smaller engineering projects

- [research-state-mcp](https://github.com/spqr-86/research-state-mcp) — model-free MCP server for research state, page fragments and local FTS5 search
- [erc3-agents](https://github.com/spqr-86/erc3-agents) — agent implementations for the Enterprise RAG Challenge, including a 103/103 benchmark run
- [customer-support-chatbot](https://github.com/spqr-86/customer-support-chatbot) — FastAPI/React AI support system with MCP, A2A, YDB and Yandex Cloud

---

## How I approach AI systems

**Measure retrieval separately from generation.**  
A single end-to-end score does not tell whether the failure came from missing evidence or bad reasoning over good evidence.

**Keep deterministic logic deterministic.**  
Authorization, state transitions, calculations and irreversible actions should not depend on model confidence.

**Prefer abstention over unsupported confidence.**  
For enterprise and regulatory use cases, refusing with a clear reason is often the correct behavior.

**Test failure modes, not only happy paths.**  
Out-of-scope queries, weak evidence, permissions, invalid structured outputs and adversarial inputs belong in the eval set.

**Treat latency and cost as system metrics.**  
Model quality matters, but so do retrieval latency, number of model calls, token usage and operational complexity.

---

## Stack

**LLM systems:** Python · OpenAI · DeepSeek · Gemini · LangGraph · Google ADK · MCP  
**Retrieval:** BM25 · dense embeddings · ChromaDB · CrossEncoder reranking  
**Backend:** FastAPI · Pydantic · PostgreSQL · SQLite  
**Infrastructure:** Docker · GitHub Actions · Google Cloud · Grafana  
**Quality:** pytest · Ruff · IR metrics · golden datasets · LLM-as-judge

---

### Current focus

Building **measurable, debuggable and controllable LLM applications** for real workflows — especially RAG, document intelligence and AI systems with deterministic safety boundaries.
