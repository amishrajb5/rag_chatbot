# RAG-Based Chatbot Project

Welcome! This is a Retrieval‑Augmented Generation (RAG) chatbot I've built, designed to answer user questions using external documents for context.

## ✨ What It Is

My chatbot processes a collection of Markdown or text documents, indexes them using embeddings and a vector store, and responds to user queries based on relevant data found. It's built using Python, leverages an open‑source LLM (like LLaMA via llama_cpp_python), and delivers answers through a simple Streamlit interface.

## 🛠️ Key Project Highlights

- **Document Ingestion & Chunking**: Splits and embeds document content into semantically searchable chunks.
- **Vector Store Retrieval**: Uses FAISS (or optional alternatives) to store and search embeddings effectively.
- **RAG Workflow**: Retrieves top‑k relevant chunks for each query, constructs a prompt, and feeds it to the language model using composition strategies like `async-tree-summarization` to generate precise and contextual answers.
- **Interactive GUI**: User-friendly Streamlit (or similar) interface to upload documents, chat, and view responses live.
- **Memory Index & Inference Pipeline**: Built offline via a builder script, then served from the app for lightweight, repeated queries.

## 🚀 Setup & Usage

1. Clone the project and install dependencies (Poetry or pip).
2. Prepare your document folder (e.g. `docs/` containing `.md` files).
3. Build the index, e.g.:
   ```bash
   python memory_builder.py --chunk-size 1000 --chunk-overlap 50
