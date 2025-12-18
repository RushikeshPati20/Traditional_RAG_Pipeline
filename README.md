# 📚 End-to-End RAG System (Local, Modular, Production-Ready)

This repository contains a **fully local, modular Retrieval-Augmented Generation (RAG) pipeline** built using Python.  
It supports **multi-format document ingestion**, **semantic search with FAISS**, and **LLM-powered summarization using Ollama (llama2)**.

---

## 🚀 Features

### 📂 Multi-format document ingestion
- PDF  
- TXT  
- CSV  
- Excel  
- Word  
- JSON  

### ✂️ Smart document chunking
- Recursive character-based splitting

### 🧠 Dense embeddings
- SentenceTransformers (`all-MiniLM-L6-v2`)

### 📦 FAISS vector database
- Persistent local storage

### 🔍 Semantic retrieval
- Top-k similarity search

### 🤖 Local LLM inference
- Ollama (`llama2:latest`)

### 🔒 Fully local & private
- No cloud APIs  
- No data leakage

---

## 🏗️ Project Structure
Project Root
│
├── data/  
│   └── Raw documents (PDF, CSV, TXT, Excel, Word, JSON)
│
├── faiss_store/  
│   └── Persistent FAISS index and metadata
│
├── src/  
│   ├── data_loader.py        - Multi-format document ingestion  
│   ├── embedding.py          - Document chunking and embedding pipeline  
│   ├── vectorstore.py        - FAISS vector store implementation  
│   └── search.py             - RAG search and summarization logic  
│
├── requirements.txt          - Project dependencies  
└── README.md                 - Project documentation


## 🔄 Architecture Overview

Documents
↓
Data Loader
↓
Text Chunking
↓
Embeddings (SentenceTransformers)
↓
FAISS Vector Store
↓
Semantic Retrieval
↓
Ollama (llama2)
↓
Answer / Summary



## ⚙️ Setup Instructions

### 1️⃣ Clone the Repository
git clone https://github.com/RushikeshPati20/Traditional_RAG_Pipeline

### 2️⃣ Install Dependencies
Copy code
pip install -r requirements.txt

### 3️⃣ Install & Run Ollama
Copy code
ollama pull llama2

### ▶️ Usage
Build Vector Store & Query
Copy code
python src/search.py
Example query:

text
Copy code
"What is attention mechanism?"
The system retrieves relevant document chunks and generates a concise summary using a local LLM.

### 🧪 Example Use Cases
Document Q&A
Knowledge base search
Research paper summarization
Internal document assistant
Local GenAI experimentation

### 🔮 Future Improvements
Hybrid search (BM25 + embeddings)
Metadata filtering
Better chunking strategies
Streaming LLM responses
API / Web UI integration

### 🛠️ Tech Stack
Python
LangChain
SentenceTransformers
FAISS
Ollama (llama2)
NumPy

### 📌 Why This Project?
This project demonstrates how real-world RAG systems are structured:
Clear separation of concerns
Reusable components
Local-first GenAI architecture
Production-style vector search
