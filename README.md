
# 📜 Sanskrit Document Retrieval-Augmented Generation (RAG) System

# 📌 Project Overview
This project implements a Retrieval-Augmented Generation (RAG) system capable of answering user queries based on Sanskrit documents.
The system integrates semantic retrieval with a CPU-based Large Language Model (LLM) to generate context-grounded responses, ensuring factual correctness and reduced hallucination.
The entire pipeline is designed to run without GPU support, making it lightweight, reproducible, and compliant with CPU-only constraints.

# 🎯 Objectives
Ingest Sanskrit documents in Unicode format

Preprocess and index documents for efficient retrieval

Accept queries in Sanskrit (Devanagari)

Retrieve relevant context from the corpus

Generate accurate, grounded answers using a CPU-based LLM

# 🧠 System Architecture
User Query (Sanskrit)
        ↓
Query Embedding
        ↓
FAISS Vector Retrieval
        ↓
Relevant Sanskrit Chunks
        ↓
Prompt Construction
        ↓
CPU-based LLM (mT5)
        ↓
Generated Answer

# 🛠️ Tech Stack
Component	Technology
Programming Language	Python 3
Document Parsing	python-docx
Text Chunking	LangChain Text Splitters
Embeddings	Multilingual MiniLM
Vector Store	FAISS (CPU)
Language Model	mT5-small
Deployment	Google Colab / Local CPU
📂 Project Structure
RAG_Sanskrit_<YourName>/
│
├── code/
│   └── Sanskrit_RAG_System.ipynb
│
├── data/
│   └── Rag-docs.docx
│
├── report/
│   └── Sanskrit_RAG_Report.pdf
│
└── README.md

# 🚀 Setup Instructions
🔹 1. Clone the Repository
git clone https://github.com/<your-username>/RAG_Sanskrit_<YourName>.git
cd RAG_Sanskrit_<YourName>

🔹 2. Environment Requirements

Python 3.9+

CPU-only environment (no GPU required)

🔹 3. Install Dependencies

If running locally:

pip install torch transformers sentence-transformers faiss-cpu \
langchain langchain-community langchain-text-splitters python-docx


For Google Colab:

Use CPU runtime

Install dependencies inside the notebook

# ▶️ How to Run

Open the notebook:

code/Sanskrit_RAG_System.ipynb

Run cells sequentially:

Library installation

Document upload

Preprocessing & chunking

FAISS indexing

Query execution

Enter a Sanskrit query, for example:

शंखनादः किम् कृतवान् ?


The system retrieves relevant context and generates an answer grounded in the document.

# ⚙️ CPU Optimization Notes

No GPU or CUDA usage

Lightweight multilingual embedding model

Small LLM (mT5-small)

FAISS-CPU vector indexing

Minimal memory footprint

# 📊 Performance Observations

Retrieval latency: ~40–70 ms

Generation latency: ~1.5–2.5 seconds

RAM usage: ~2–3 GB

High answer relevance for document-based queries

# ⚠️ Limitations

No sandhi splitting

Limited Sanskrit-specific LLM availability

Transliteration normalization not included

# 🔮 Future Enhancements

Hybrid BM25 + vector retrieval

Sandhi and morphological analysis

Transliteration (IAST ↔ Devanagari)

Web UI using Streamlit

Sanskrit-fine-tuned LLM

# 📄 Report

A detailed technical report describing system architecture, preprocessing, retrieval, generation, and performance analysis is available in:

/report/Sanskrit_RAG_Report.pdf
