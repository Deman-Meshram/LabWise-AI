# LabWise AI — Lab Report Analyzer

> AI-powered lab report analysis for patients and clinicians.



![Status](https://img.shields.io/badge/Status-Complete-brightgreen)



---

## What It Does

- **Abnormality detection** — HIGH / LOW / BORDERLINE / CRITICAL flags
- **Plain language summary** — explains results in simple terms
- **Gmail HTML report** — formatted report delivered to email
- **Multi-report memory** — Pinecone stores past reports for trend tracking
- **Health Score** — overall score calculated from results

---

## Tech Stack

| Layer | Tool |
|---|---|
| Frontend | Lovable (teal + white UI) |
| Automation | n8n webhook workflow |
| PDF Parsing | LlamaParse |
| Vector Memory | Pinecone (3072 dims) |
| LLM | Gemini 2.5 Flash |
| Email | Gmail HTML |

---

## Key Features

- PDF upload via drag-and-drop
- Borderline / High / Low / Critical detection
- Gmail HTML report with color-coded results
- Pinecone vector memory for multi-report tracking
- AI chat for follow-up questions
- Health score dashboard

---

*Built by Deman Meshram | BSc Biotechnology + AI Automation*
