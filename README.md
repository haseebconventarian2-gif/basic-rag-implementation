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

<!-- code-audit-details -->

## 🔄 Runtime Flow

`Text/audio → STT → retrieval → Azure chat → TTS/text → messaging channel`

This flow is derived from the current entry points and service calls.

## 🗂 Code Map

| Path | Responsibility |
| --- | --- |
| `bank.json` | Supporting resource |
| `bankislami_voice_config.json` | Supporting resource |
| `important.txt` | Supporting resource |
| `rag_pipeline.py` | Retrieval and generation pipeline |
| `requirements.txt` | Python dependencies |
| `routes.py` | HTTP routes and orchestration |
| `ui.py` | Supporting resource |
| `vector_database.py` | Document indexing and vector storage |
| `whatsapp.py` | WhatsApp integration |

## 🔐 Environment Variables

No environment-variable reads were detected.

## 🌐 Detected API Routes

| Method | Endpoint |
| --- | --- |
| `GET` | `/` |
| `GET` | `/health` |
| `GET` | `/media/{media_id}` |
| `GET` | `/tts` |
| `GET` | `/webhook` |
| `GET` | `/whatsapp/diagnose` |
| `POST` | `/audio` |
| `POST` | `/text` |
| `POST` | `/webhook` |
| `POST` | `/whatsapp/push` |

## 🧪 Validation Guide

1. Install dependencies in a clean virtual environment.
2. Start the documented entry point and test the root or health route.
3. Exercise one valid and one invalid request.
4. Verify external-service errors are handled clearly.
5. Confirm secrets, private data, indexes, and model artifacts are ignored.

## 🔒 Production Checklist

- Use managed secret storage and rotate exposed credentials.
- Add authentication, authorization, rate limiting, and request-size limits.
- Add automated tests, structured logging, monitoring, and health checks.
- Pin and audit dependencies.
- Define retention and privacy controls for audio and customer data.

## ⚠️ Code-Audit Notes

- Documentation reflects the current repository code and may expose integrations that need separate cloud accounts, model assets, or channel approval.
- Treat the project as a reference implementation until its security and deployment configuration are hardened.
- `routes.py` currently uses package-relative imports; adjust the package layout or imports before starting the API.
