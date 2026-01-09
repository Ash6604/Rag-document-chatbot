# RAG-based Document Q&A Chatbot

This project demonstrates a **Retrieval-Augmented Generation (RAG)** based
AI chatbot built using **n8n**, **OpenAI**, and **Pinecone**.

The system allows users to upload documents and ask questions about their
content using natural language.

> 🔹 Demo data: A document containing rules of Golf  
> 🔹 The workflow is generic and works for any text-based document

---

## Features

- Automatic document ingestion from Google Drive
- Text chunking using Recursive Character Text Splitter
- OpenAI embeddings for semantic search
- Pinecone vector database for retrieval
- AI Agent for context-aware answers
- Chat-based question answering

---

## How It Works (High Level)

1. A document is uploaded to a Google Drive folder
2. n8n detects the upload and downloads the file
3. The document is split into chunks
4. Embeddings are generated using OpenAI
5. Vectors are stored in Pinecone
6. User questions retrieve relevant chunks
7. The AI agent generates a final answer

---

## Example Questions

- What are the basic rules of golf?
- Summarize the uploaded document
- Explain this section in simple terms

---

## How to Use

1. Import `n8n-workflow.json` into n8n
2. Configure credentials:
   - OpenAI
   - Pinecone
   - Google Drive
3. Set environment variables (see `.env.example`)
4. Upload a document to the configured Drive folder
5. Ask questions using the chat trigger

---

## Security Notes

- This repository does **not** contain API keys or secrets
- All credentials must be configured locally in n8n
- `.env.example` is provided as a reference only

---

## Why This Project?

This project showcases:
- RAG architecture
- Vector databases
- AI workflow orchestration
- Real-world LLM system design

---

## License

MIT
