# Agentic RAG System with LangGraph

An advanced **Agentic Retrieval-Augmented Generation (RAG)** system built using **LangGraph, LangChain, FAISS, and HuggingFace** — designed to intelligently decide when to retrieve information and generate accurate responses.

---

##  Project Overview

This project implements a **conditional RAG pipeline** where the system behaves like an intelligent agent:

* Decides whether external knowledge is needed
*  Retrieves relevant documents using vector similarity
*  Generates context-aware answers using a local LLM

Unlike basic RAG systems, this uses **LangGraph** to create a structured, decision-based workflow.

---

##  Key Features

* ⚡ **Agentic Decision Making**

  * Dynamically decides whether retrieval is required

* 🔎 **Semantic Search with FAISS**

  * Fast and efficient vector similarity search

* 🧠 **HuggingFace Embeddings (FREE)**

  * `all-MiniLM-L6-v2` for high-quality embeddings

* 🤖 **Local LLM (FREE)**

  * Runs fully offline using HuggingFace (`flan-t5`)

* 🔄 **LangGraph Workflow**

  * Implements:

    ```
    DECIDE → RETRIEVE → GENERATE
    ```

* 💸 **Zero API Cost**

  * No OpenAI or paid APIs required

---

## 🏗️ Project Structure

```
AgenticRAG/
│
├── app/                # Core logic (RAG + LangGraph)
├── data/               # Documents / datasets
├── notebooks/          # Experimentation (Jupyter)
│   └── agenticrag.ipynb
│
├── .env                # Environment variables (ignored)
├── .gitignore
├── requirements.txt
└── README.md
```

---

## ⚙️ Tech Stack

* **LangGraph** → Workflow orchestration
* **LangChain** → RAG pipeline
* **FAISS** → Vector database
* **HuggingFace** → Embeddings + LLM
* **Python** → Core language

---

## 🔄 Workflow Explained

```
User Query
   ↓
[DECIDE]
   ↓
YES → [RETRIEVE] → [GENERATE]
NO  →            [GENERATE]
   ↓
Final Answer
```

### 🧩 Nodes:

* **Decide** → Determines if retrieval is needed
* **Retrieve** → Fetches relevant documents
* **Generate** → Produces final answer

---

## 🚀 How to Run

### 1. Clone the repository

```
git clone https://github.com/YOUR_USERNAME/AgenticRAG.git
cd AgenticRAG
```

### 2. Create virtual environment

```
uv venv
source .venv/bin/activate
```

### 3. Install dependencies

```
uv pip install -r requirements.txt
```

### 4. Run the notebook

```
cd notebooks
jupyter notebook
```

---

## 📌 Example Query

```
What is LangGraph?
```

### ✅ Output:

* Retrieves relevant documents
* Generates contextual answer using LLM

---

## 💡 Key Learnings

* Built a **modular RAG pipeline**
* Understood **LangGraph state-based workflows**
* Implemented **local LLM inference (no API)**
* Solved real-world issues like:

  * CUDA errors
  * LangChain version changes
  * Environment configuration

---

## 🔐 Security

* `.env` file is excluded via `.gitignore`
* No API keys are exposed

---

## 🚀 Future Improvements

* 🔝 Add reranking for better retrieval accuracy
* 🌐 Build a frontend (React / Streamlit)
* ⚡ Deploy as an API (FastAPI)
* 🧠 Replace heuristic decision with LLM-based routing

---

## 👨‍💻 Author

**Pratik**
Aspiring AI Engineer | RAG & Agent Systems Enthusiast

---

## ⭐ If you like this project

Give it a ⭐ on GitHub — it motivates further development!
