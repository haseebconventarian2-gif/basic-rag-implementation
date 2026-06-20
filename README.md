<div align="center">

# Basic Banking RAG Implementation

Basic banking RAG implementation with FAISS retrieval, Python chat interfaces, and WhatsApp integration.

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)
![Status](https://img.shields.io/badge/Status-Reference%20Implementation-6366F1)

</div>

---

## Overview

Basic banking RAG implementation with FAISS retrieval, Python chat interfaces, and WhatsApp integration.

## Highlights

- PDF and JSON ingestion
- Semantic FAISS retrieval
- English and Urdu responses
- Web and messaging interfaces

## Tech Stack

Python · FastAPI · LangChain · FAISS · Azure OpenAI

## Getting Started

```bash
git clone https://github.com/haseebconventarian2-gif/basic-rag-implementation.git
cd basic-rag-implementation
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
```

## Configuration

Configure Azure OpenAI chat and embedding deployments in `.env`.

> Store credentials in `.env` and never commit secrets.

## Run

```bash
uvicorn routes:app --host 0.0.0.0 --port 8000
```

## Project Status

This is a learning and reference implementation. Review security, validation, monitoring, and deployment settings before production use.
