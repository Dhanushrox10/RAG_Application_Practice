# 📚 RAG Application with ChromaDB

## 🚀 Overview

This project implements a **Retrieval-Augmented Generation (RAG)** pipeline that processes PDF documents, performs text chunking, stores embeddings in a vector database, and enables efficient semantic retrieval.

The system leverages **ChromaDB** for vector storage with persistence, allowing reuse of indexed data without recomputation.

---

## 🧠 Features

* 📄 PDF ingestion and processing
* ✂️ Intelligent text chunking
* 🔍 Embedding generation for semantic search
* 🗂️ Storage using ChromaDB
* 💾 Persistent vector database
* ⚡ Fast similarity search for relevant context retrieval

---

## 🏗️ Project Structure

```
├── .venv/                         # Virtual environment
├── docs/                          # Source documents
│   ├── fabric-admin.pdf
│   └── fabric-onelake.pdf
├── vector/                        # Persistent ChromaDB storage
│
├── .env                           # Environment variables
├── .env-example                   # Example env file
├── .env-ignore                    # Ignored env configs
│
├── 1.0_RAG_With_Own_Text.ipynb    # RAG with custom text
├── 2.0_RAG_PDF.ipynb              # RAG with PDF processing
├── 3.0_RAG_Local_Persist.ipynb    # RAG with persistent DB
├── 4.0_RAG_Add_Docs.ipynb         # Add new docs to DB
│
├── main.py
├── README.md
├── requirements.txt
└── uv.lock
```

---

## ⚙️ Installation

```bash
git clone <your-repo-url>
cd <your-repo-name>

pip install -r requirements.txt
```

---

## ▶️ Usage

### 1. Add PDFs

Place your PDF files inside the `data/` directory.

### 2. Run Ingestion

```bash
python main.py
```

This will:

* Load PDFs
* Split text into chunks
* Generate embeddings
* Store them in ChromaDB

---

## 💾 Persistent Vector Database

* The vector database is stored locally (e.g., `db/` folder).
* Once created, embeddings are reused.
* Avoids recomputation on every run.

---

## 🔍 Querying

You can retrieve relevant chunks using semantic search:

```python
results = retriever.query("your question here")
```

---

## 🧩 Tech Stack

* Python
* ChromaDB (Vector Database)
* PDF Processing Libraries
* Embedding Models (configurable)

---

## 📌 Key Concepts

### 🔹 RAG (Retrieval-Augmented Generation)

Combines:

* **Retriever** → Fetch relevant context
* **Generator** → Produce final response

### 🔹 Chunking

Splitting large text into smaller segments for:

* Better embedding quality
* Efficient retrieval

### 🔹 Persistence

Stores embeddings locally so:

* No need to reprocess documents
* Faster subsequent runs

---

## 🛠️ Future Improvements

* Add LLM integration for answer generation
* API endpoint for querying
* UI for document upload and chat
* Support for multiple file formats

---

## 🤝 Contribution

Feel free to fork this repository and improve it. Pull requests are welcome.

---

## 📄 License

This project is open-source and available under the MIT License.
