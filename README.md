# Decentralized-Multi-Agent-RAG-System

 A decentralized, multi‑agent RAG system that lets you:
- Ingest and summarize YouTube videos  
- Scrape and index web content by keyword  
- Chat with and perform CRUD on custom databases  
- Fact‑check retrieved information  

Built with LangChain/Llama‑Index, FastAPI, Streamlit, and deployable via Docker & Kubernetes or serverless platforms (TBD).

---

## 🚀 Features

- **YouTube Agent**: Fetch transcripts via YouTube API or `pytube`, chunk, embed (OpenAI), and store in a vector DB.  
- **Web‑scraper Agent**: Crawl URLs or use NewsAPI, extract text, chunk, embed, and store.  
- **Database‑chat Agent**: Natural‑language CRUD on MongoDB/PostgreSQL via FastAPI + LangChain chains.  
- **Fact‑Checker Agent**: Validate claims using Google Fact Check API or LLM retrieval chains.  

---

## 📦 Architecture

```
[Streamlit UI]
      ↓
[FastAPI Orchestration]
      ↓
[LangChain/Llama‑Index Agents]
      ↓
┌──────────────┬───────────────┐
│ Vector DB    │ NoSQL/SQL DB  │
│ (Weaviate,   │ (MongoDB,     │
│  Chroma)     │  PostgreSQL)  │
└──────────────┴───────────────┘
```

---

## 🛠️ Tech Stack

| Layer            | Tools / Libraries                                      |
|------------------|---------------------------------------------------------|
| **Orchestration**| LangChain, Llama‑Index                                  |
| **Embeddings**   | OpenAI Embeddings, Weaviate, Chroma                     |
| **YouTube**      | `pytube` / YouTube Data API, Whisper                    |
| **Web Scraping** | BeautifulSoup, Scrapy, Newspaper3k                      |
| **Fact Check**   | Google Fact Check API, custom LLM chains                |
| **DB‑Chat**      | FastAPI, Pydantic, MongoDB, SQLAlchemy                  |
| **Frontend**     | Streamlit                                               |
| **CI/CD**        | GitHub Actions, Docker                                  |
| **Deployment**   | AWS ECS/EKS, GCP Cloud Run, Azure Container Apps        |

---
