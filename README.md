🚀 AI-DOP & SMID – Seangkatan.id
IBM watsonx Agentic AI Hackathon Project (2025)

AI-DOP (AI Deep Observation Pipeline) is an agentic AI workflow built using IBM watsonx Orchestrate to power student wellbeing intelligence for Seangkatan.id, a social edutech platform for Indonesian middle & high school students.

This system transforms raw student text from social-learning channels into actionable, structured insights—supporting teachers, counselors, and parents in early detection of bullying, emotional distress, strengths, and talent indicators.

🌐 About Seangkatan.id

Seangkatan.id is a social edutech platform designed to build healthy digital school communities.
It includes multiple student-generated data channels:

ConfessWall — anonymous emotional expression
RoomChat — classroom & group discussions
Interactive Quizzes — self-reflection & micro-assessment
Digital Mading — student creativity board
Virtual Homeroom Teacher (Wali Kelas Virtual) — an evolving AI mentor
These channels produce rich natural-language data that feed directly into the AI-DOP & SMID analysis pipeline.

🧠 What the AI-DOP & SMID Agent Does
The agent produces a structured 4-section wellbeing intelligence report for every input:
1. NLP Analysis
Sentiment
Emotion
Toxicity
Keyword & topic extraction

2. 3C Strength Model (Triangulation)
C1 – Cognition
C2 – Character
C3 – Competence
Flags for psychological or contextual signals

3. SMID Early-Warning Indicators
SMID = Student Measurement Impact Dashboard
Includes:
Bullying risk score (Low / Medium / High)
Emotional distress indicators
Safety & crisis cues
Peer conflict & avoidance patterns

4. Talent Signals
Detected from linguistic patterns:
Leadership
Communication
Empathy
Problem-solving
Creativity
Teamwork

5. Career Interest Cues
Themes extracted from text (education, social, STEM, arts, etc.)

🔥 Why It Matters
AI-DOP & SMID enables:
Early detection of bullying & emotional distress
Data-driven insights for teachers & parents
Longitudinal wellbeing tracking
Class-wide & individual-level analytics
AI-powered support for the Virtual Homeroom Teacher
Foundation for a scalable, nationwide wellbeing dashboard
It transforms everyday student conversations into actionable wellbeing intelligence.

🏆 Real-World Traction (Pre-Hackathon)
Seangkatan.id already has meaningful recognition:

✔ 1:1 Investor Matchmaking – TIACon 2025
Invited to private investor meetings.
✔ 11th NextDev Scouting
Selected as a promising early-stage Indonesian edutech startup.
✔ Signed LOI with a school (300 students)
Pilot implementation agreement underway.
These validate both market demand and real-world relevance of AI-DOP & SMID.

🧩 Architecture Overview
This MVP runs entirely inside IBM watsonx Orchestrate:
Custom AI Agent: AI-DOP & SMID Agent
Custom Tool: run_ai_dop_analysis
Behavior rules: safety, override logic, stateless patterns
Agent reasoning: auto-detect missing inputs
LLM Model: llama-3-2-90b-vision-instruct (Granite-compatible)
No backend required during the hackathon
Optional: Local Streamlit UI to visualize how the results will appear on Seangkatan.id

⚙️ How It Works (End-to-End Flow)
Student → Seangkatan.id Channels → AI-DOP & SMID Agent → Tool → SMID Report → Teachers / Parents / Dashboar

Step-by-step:

A student writes a message (ConfessWall, RoomChat, quizzes, etc.).
The message is sent to the AI-DOP & SMID Agent.
The agent triggers the tool run_ai_dop_analysis.
The backend logic returns NLP → 3C → SMID → Talent indicators.
The agent applies safety + override behavior.
The final structured SMID Report is produced.
(Future) This report is consumed by the Virtual Homeroom Teacher and teacher dashboards.

🔗 Future Integration via IBM watsonx Orchestrate API
After the hackathon, Seangkatan.id will connect to this agent programmatically:
Frontend: Seangkatan.id platform
Backend: FastAPI
Orchestrate API: Triggers agent workflow
Analysis: SMID report returned to platform
Dashboard: Real-time wellbeing monitoring
This enables district-wide scalability across Indonesian schools.

🖥 Optional UI Prototype (Streamlit Demo)
To demonstrate future integration with the Seangkatan.id ecosystem, we built a local-only Streamlit demo that includes:
AI-DOP Text Analyzer (NLP + 3C + SMID)
Risk assessment page
SMID Dashboard (longitudinal data mock)
Teacher alert console
This is optional and not required by the hackathon, but helps judges visualize how schools will use the system.
Run locally:
pip install -r requirements.txt
streamlit run streamlit_app.py

🚀 Demo Instructions (For Judges)
Main Demo (Required)

🔗 https://us-south.watson-orchestrate.cloud.ibm.com/chat

Because this is a managed IBM Cloud environment, the link does not contain an agentId.
Judges will log in using the provided IBM Cloud credentials and select:
AI-DOP & SMID Agent → Start Chat

Paste any student message to get a full SMID Report.

🧪 Sample Prompts (Copy & Paste)
Positive

"I enjoy organizing study groups and explaining lessons to my classmates."

Bullying / Distress

"I'm tired of being mocked every day. It makes me scared to go to school."

Neutral Reflection

"I like helping my friends, but sometimes I doubt myself when I make mistakes."

Anxiety

"I don’t know why, but lately I feel nervous talking to people, even though nothing bad ever happened."

Each message will return the full:
NLP → 3C → SMID → Key Themes structure.

📊 Limitations & Next Steps
Current Limitations (MVP)
Single-message analysis only
Risk calibration not yet validated with real school counselors
No multi-student aggregation in production yet
No live API integration (hackathon environment restriction)

Next Steps
Full API pipeline (FastAPI → Orchestrate → SMID)
Population-level dashboard
Longitudinal wellbeing timeline
Automated alerts for teachers & parents
Integration with the Virtual Homeroom Teacher

Multi-channel multimodal analysis (text + behavioral metadata)

📘 License

This project is developed exclusively for the
IBM watsonx Agentic AI Hackathon (Nov 2025).
