# 📄 PDF RAG using LangChain, Hugging Face & FAISS

A practice Retrieval-Augmented Generation (RAG) project that allows a user to upload a PDF, retrieve relevant information from the document, and generate answers using a Hugging Face language model.

The project demonstrates the complete basic RAG pipeline: PDF loading, text chunking, embeddings, vector similarity search, retrieval, prompt construction, and LLM-based answer generation.

---

## 🚀 Project Overview

This project implements a basic **PDF Question Answering system using RAG**.

The user uploads a PDF document, which is then:

1. Loaded using `PyPDFLoader`
2. Split into smaller chunks
3. Converted into vector embeddings
4. Stored in a FAISS vector store
5. Retrieved using similarity search when a question is asked
6. Passed as context to a Hugging Face LLM
7. Converted into a final answer using an output parser

### RAG Pipeline

```text
PDF Upload
    ↓
PyPDFLoader
    ↓
Document Extraction
    ↓
Text Chunking
    ↓
Hugging Face Embeddings
    ↓
FAISS Vector Store
    ↓
Retriever
    ↓
Relevant Document Chunks
    ↓
Prompt Template
    ↓
Hugging Face LLM
    ↓
StrOutputParser
    ↓
Final Answer
