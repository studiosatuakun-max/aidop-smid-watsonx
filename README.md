# AI-DOP & SMID – Seangkatan.id (IBM watsonx Agentic AI Hackathon)

**AI-DOP (AI Deep Observation Pipeline)** is an agentic AI workflow prototype for **Seangkatan.id**, a social edutech platform for students.

The goal is to turn raw student text from channels like **ConfessWall, RoomChat, and Virtual Homeroom (Wali Kelas Virtual)** into:

- **3C signals**
  - **C1 – Core Competency**
  - **C2 – Career Compass**
  - **C3 – Contextual Capacity**
- **SMID** – Student Measurement Impact Dashboard
- An **early-warning risk index** (LOW / MEDIUM / HIGH) for bullying and emotional distress.

Built for the **Agentic AI Hackathon with IBM watsonx Orchestrate** on lablab.ai.

---

## Architecture Overview

- **Frontend:** Streamlit app (`/ui/app.py`)
  - Tab 1 – *Analyze Text (AI-DOP)*
  - Tab 2 – *SMID Dashboard*
- **Backend:** FastAPI (`/backend/main.py`)
  - `POST /analyze_text` – NLP + 3C mapping + risk engine
  - `GET /smid/{student_id}` – aggregations for SMID
- **Agentic / AI Layer (designed for IBM watsonx):**
  - `backend/ibm_client.py` – client stub for **watsonx.ai**
  - Future: orchestrated by **watsonx Orchestrate** to:
    - Ingest events from Seangkatan.id channels
    - Call watsonx.ai models
    - Persist events into Cloudant
- **Storage (MVP):**
  - In-memory Python dict
  - Cloudant instance already provisioned for future integration

---

## Features

- NLP analysis (sentiment, emotion, toxicity, topics)
- 3C scoring:
  - **C1 – Core Competency**
  - **C2 – Career Compass**
  - **C3 – Contextual Capacity** (wellbeing / social signals)
- Risk engine:
  - Continuous risk index `[0.0 – 1.0]`
  - Category: **LOW / MEDIUM / HIGH**
  - Human-readable reason string
- SMID dashboard:
  - Events count per student
  - Average C1 / C2 / C3
  - Last risk index & category
  - Alert list for MEDIUM / HIGH risks

---

## Running locally

```bash
# 1. Create & activate virtual env
python -m venv venv
# Windows:
venv\Scripts\activate

# 2. Install dependencies
pip install -r backend/requirements.txt

# 3. Run FastAPI backend
cd backend
uvicorn main:app --reload --host 0.0.0.0 --port 8000

# 4. Run Streamlit UI (new terminal)
cd ../ui
streamlit run app.py
