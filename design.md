# VaaniSetu AI – System Design Document

## 1. System Overview

VaaniSetu AI is built using a Retrieval-Augmented Generation (RAG) architecture to provide accurate, document-backed responses from public welfare datasets.

The system integrates speech processing, language detection, vector search, and LLM reasoning.

---

## 2. High-Level Architecture

User (Voice/Text)
        ↓
Speech-to-Text (Whisper)
        ↓
Language Detection
        ↓
Preprocessing & Query Structuring
        ↓
RAG Pipeline
    - Document Embedding
    - Vector Database (FAISS / Chroma)
        ↓
LLM Reasoning Engine (Llama 3 / GPT)
        ↓
Response Generator
        ↓
Text-to-Speech
        ↓
User Interface

---

## 3. Technology Stack

### Frontend
- React.js
- Tailwind CSS
- Simple chat-style UI

### Backend
- FastAPI / Flask
- Python

### Databases
- MongoDB (structured scheme data)
- FAISS / Chroma (vector database for embeddings)

### AI Components
- Whisper (Speech-to-Text)
- Sentence Transformers (Embeddings)
- Llama 3 / GPT API
- gTTS or equivalent for Text-to-Speech

---

## 4. RAG Workflow

1. Government scheme PDFs are converted into text.
2. Text is chunked into smaller sections.
3. Each chunk is converted into embeddings.
4. Embeddings are stored in a vector database.
5. User query is embedded and matched with relevant chunks.
6. Retrieved context is passed to LLM.
7. LLM generates structured, accurate response.

---

## 5. Data Flow

- User sends voice/text query.
- Query processed and language detected.
- Relevant scheme data retrieved.
- Personalized filtering applied.
- Response generated and returned.

---

## 6. Eligibility Filtering Module

Structured filtering based on:

- State
- Income range
- Age
- Occupation
- Category (optional)

Implemented using rule-based filtering over structured JSON dataset.

---

## 7. Security & Privacy

- No personal data permanently stored.
- HTTPS secure communication.
- Public and synthetic data only.
- No external sharing of user inputs.

---

## 8. Deployment Strategy

- Backend deployed on Render / Railway
- Frontend hosted on Vercel
- MongoDB Atlas for structured data
- Vector DB hosted locally or cloud

---

## 9. Scalability Plan

- Stateless backend APIs
- Load-balanced deployment
- Modular AI pipeline
- Easy language expansion

---

## 10. Future Enhancements

- WhatsApp integration
- Offline SMS-based query mode
- Regional language expansion
- Integration with official government APIs
