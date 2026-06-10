# LabWise AI — Lab Report Analyzer

> AI-powered lab report analysis for patients and clinicians.



![Status](https://img.shields.io/badge/Status-Complete-brightgreen)



---

## What It Does

LabWise AI analyzes medical lab reports (PDFs) and returns structured AI summaries. Built for patients and clinicians who need fast, intelligent interpretation of lab results.

- **Abnormality detection** — HIGH / LOW / BORDERLINE / CRITICAL flags per biomarker
- **Plain language summary** — explains results in simple terms
- **Gmail HTML report** — color-coded formatted report delivered to email
- **Multi-report memory** — Pinecone stores past reports for trend tracking
- **AI chat** — ask follow-up questions about your results

---

## Frontend (Lovable)

- Clean teal + white UI built on Lovable
- PDF upload via drag-and-drop
- AI summary displayed after analysis
- Borderline / High / Low / Critical flags shown per biomarker
- AI chat interface for follow-up questions
- Fully responsive web application

---

## Tech Stack

| Layer | Tool |
|---|---|
| Frontend | Lovable (teal + white UI) |
| Automation | n8n webhook workflow |
| PDF Parsing | LlamaParse |
| Vector Memory | Pinecone (3072 dims) |
| LLM | Gemini 2.5 Flash |
| Embeddings | Gemini Embeddings |
| Email | Gmail HTML |

---

## Architecture

```
User uploads PDF (Lovable frontend)
        ↓
n8n Webhook receives file
        ↓
LlamaParse extracts text from PDF
        ↓
Gemini 2.5 Flash analyzes biomarkers
        ↓
Results stored in Pinecone (patient memory)
        ↓
Gmail sends formatted HTML report
        ↓
Frontend displays AI summary + flags
```

---

## Key Features

- PDF upload via drag-and-drop
- Borderline / High / Low / Critical detection
- Gmail HTML report with color-coded results
- Pinecone vector memory for multi-report tracking
- AI chat for follow-up questions

---

## Technical Notes

- Pinecone dimensions: 3072 (Gemini embeddings)
- PDF sent as binary to LlamaParse
- Session ID used for multi-report patient memory
- Gemini used for both LLM and embeddings

---

*Built by Deman Meshram | BSc Biotechnology + AI Automation*
