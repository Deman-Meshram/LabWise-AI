# LabWise AI — Lab Report Analyzer

> AI-powered lab report analysis for patients and clinicians.



![Status](https://img.shields.io/badge/Status-Complete-brightgreen)



---

## The Problem

Lab reports are confusing. Medical jargon, reference ranges, abnormal flags — most patients don't understand what their results mean. They wait days for a doctor's appointment just to hear "everything looks normal" or "this value is slightly high."

For clinicians, manually reviewing and explaining multiple reports takes significant time.

---

## The Solution

LabWise AI instantly analyzes any lab report PDF and returns:
- Plain language explanation of every biomarker
- Clear HIGH / LOW / BORDERLINE / CRITICAL flags
- Personalized email report with color-coded results
- Memory of past reports for trend tracking over time

No medical jargon. No waiting. Just clear answers.

---

## Time & Effort Saved

| Task | Manual | LabWise AI |
|---|---|---|
| Understanding report | 1-2 days (doctor visit) | 30 seconds |
| Identifying abnormal values | Manual scanning | Instant AI detection |
| Getting a written summary | Not available | Auto-delivered to Gmail |
| Tracking trends over time | Manual comparison | Automatic via Pinecone memory |

---

## Final Output

- ✅ Color-coded HTML email report delivered to Gmail
- ✅ Each biomarker flagged — GOOD / BORDERLINE / HIGH / LOW / CRITICAL
- ✅ Plain language summary anyone can understand
- ✅ AI chat for follow-up questions about results

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

## Technical Notes

- Pinecone dimensions: 3072 (Gemini embeddings)
- PDF sent as binary to LlamaParse
- Session ID used for multi-report patient memory
- Gemini used for both LLM and embeddings

---

*Built by Deman Meshram | BSc Biotechnology + AI Automation*
