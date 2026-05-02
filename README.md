# 🔗 LangChain-Splitting-Mastery

> *Master the art of text splitting for high-performance RAG pipelines and LLM applications.*

---

## 📌 Project Overview

Large Language Models operate within fixed **context windows** — feeding them raw, unprocessed documents leads to truncation, hallucination, and degraded retrieval quality. **Text splitting** is the foundational preprocessing step that bridges raw data and intelligent retrieval.

This repository is a comprehensive, hands-on tutorial covering every major text splitting strategy available in LangChain. Whether you're building a **Retrieval-Augmented Generation (RAG)** pipeline, a document Q&A system, or a semantic search engine, understanding *how* and *when* to split your text is critical to achieving:

- ✅ Higher retrieval precision
- ✅ Reduced context overflow
- ✅ Better embedding quality
- ✅ Improved LLM response coherence

---

## 🗺️ Technical Roadmap

This tutorial is structured around five core splitting paradigms:

| # | Method | Description |
|---|--------|-------------|
| 1 | 🔤 **Character Splitting** | Splits text by a single delimiter (e.g., `\n\n`). Simple and fast — best for uniform plain text. |
| 2 | 📏 **Length-Based Splitting** | Divides text by token or character count. Ensures chunks conform to model context limits. |
| 3 | 🧱 **Text-Structure Splitting** | Uses recursive delimiters (`\n\n`, `\n`, ` `) to respect natural language boundaries. The most commonly used general-purpose splitter. |
| 4 | 📄 **Document-Structure Splitting** | Format-aware splitting for Markdown, HTML, code, and PDFs — preserves semantic structure. |
| 5 | 🧠 **Semantic Splitting** | Embedding-based splitting that groups sentences by meaning. Ideal for nuanced, content-aware chunking. |

---

## ⚙️ Prerequisites

Before getting started, ensure you have the following:

### 🐍 Python
- Python **3.9+** recommended
- A virtual environment is strongly advised (`venv` or `conda`)

### 📦 Core Libraries
- [`langchain`](https://github.com/langchain-ai/langchain) — Core framework
- [`langchain-text-splitters`](https://pypi.org/project/langchain-text-splitters/) — Dedicated splitter module
- [`langchain-openai`](https://pypi.org/project/langchain-openai/) or [`langchain-huggingface`](https://pypi.org/project/langchain-huggingface/) — Embeddings backend

### 🔑 API Keys
You will need **at least one** of the following:

| Provider | Environment Variable | Use Case |
|----------|---------------------|----------|
| OpenAI | `OPENAI_API_KEY` | Embeddings + LLM calls |
| HuggingFace | `HUGGINGFACEHUB_API_TOKEN` | Open-source embeddings |

> 💡 **Tip:** Store your API keys in a `.env` file and load them with [`python-dotenv`](https://pypi.org/project/python-dotenv/). Never commit secrets to version control.

---

## 🛠️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/GautamSutar/LangChain-Text-Splitter-Mastery.git
cd LangChain-Text-Splitter-Mastery
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate           # Windows
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```