# 📡 3GPP Document Processor & Visualizer

> ⚠️ **Private Project**: This project was developed as part of a company development project. The codes are private and not publicly accessible.

A full-stack application to process, extract, and visualize **procedural state machines** from [3GPP](https://www.3gpp.org/) specification documents (e.g., TS 24.501).  
The backend parses `.docx` documents, extracts procedures using LLMs, stores structured graph data in databases, and the frontend displays these procedures as interactive **flow diagrams**.

---

## 🎥 Demo

👉 Watch the recorded walkthrough of the frontend in action:

**[📺 Watch Demo Video on YouTube](https://youtu.be/jBZAEIh_FJU)**

---

## 🧠 What This App Does

- Ingests 3GPP `.docx` specification documents in the backend
- Converts them into structured Markdown
- Extracts procedures using LLM-based prompt chain
- Validates outputs using **semantic similarity**
- Stores graph data in PostgreSQL & Neo4j
- Displays results in a **React UI** with Mermaid diagrams & JSON viewers

---

## 🧩 Application Architecture

### 🖥️ Frontend (React JS)

- Built with **React + CSS**
- Fetches:
  - Extracted graph JSON
  - Procedure metadata
- Displays:
  - Selectable procedures
  - Mermaid flowcharts
  - JSON node/edge viewer
  - Source Document viewer
- Designed for usability & clarity in navigating complex procedures

---

### 🧪 Backend (Python)

- Python + `uv` for fast dependency management
- Tools & Tech:
  - **PostgreSQL** – stores sections, metadata, extraction results
  - **OpenAI / Gemini APIs** – LLMs for multi-stage extraction
  - **SBERT** – accuracy comparison (cosine similarity)

#### Key Capabilities

- DOCX to Markdown (preserving structure & tables)
- Content filtering (excludes annexes, glossary, etc.)
- Markdown chunking by headings and hierarchy
- Procedure extraction pipeline:
  - Initial Extraction → Evaluation → Correction → Enrichment
  - Multi-model extraction (3 runs)
  - Accuracy scoring & best-result selection
- Graph + metadata storage

---
