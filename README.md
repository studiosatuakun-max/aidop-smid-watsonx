🚀 AI-DOP & SMID – Seangkatan.id
(IBM watsonx Agentic AI Hackathon Project)

AI-DOP (AI Deep Observation Pipeline) is an agentic AI workflow built with IBM watsonx Orchestrate to power the student wellbeing intelligence behind Seangkatan.id, a social edutech platform for Indonesian middle & high school students.
The system transforms raw student text from multiple social-learning channels into actionable insights—supporting teachers, parents, and counselors in early detection of bullying, emotional distress, strengths, and talent signals.

🌐 About Seangkatan.id

Seangkatan.id is a social edutech platform designed to help students express themselves, collaborate, and build healthy digital school communities. The platform includes:
ConfessWall — anonymous emotional expressions
RoomChat — class and group discussions
Interactive Quizzes — self-reflection & micro-assessments
Digital Mading — student creativity & announcements
Virtual Homeroom Teacher (Wali Kelas Virtual) — an evolving AI mentor that learns from student interactions
These channels generate rich natural language data that feeds the AI-DOP & SMID analysis pipeline.

🧠 What the AI-DOP & SMID Agent Does

The agent processes student text and produces structured wellbeing intelligence via:
1. NLP Analysis
Sentiment
Emotion
Toxicity

Keywords & themes
3. 3C Strengths (Triangulation Model)
C1 – Cognition
C2 – Character
C3 – Competence

3. SMID Early-Warning Signals
SMID = Student Measurement Impact Dashboard, which includes:
Bullying risk score (LOW / MEDIUM / HIGH)
Emotional distress indicators
Safety & crisis cues
Peer conflict and social pressure signals

4. Talent Indicators
Identified from behavioral cues in text:
Leadership
Communication
Empathy
Problem-solving
Creativity
Teamwork

5. Career Interest Cues
Extracted themes (education, arts, social, STEM, etc.)

6. Key Themes
Summaries of the underlying meaning of the message.
All results follow a consistent 4-section structured output:
NLP Analysis
3C Insights
SMID Early Warning Indicators
Key Themes

🔥 Why It Matters

AI-DOP & SMID enables:
Early detection of bullying & emotional distress
Data-driven insights for teachers and parents
Long-term student wellbeing monitoring
Class-wide and individual-level analytics
AI-powered support for the Virtual Homeroom Teacher
Foundation for a scalable, school-wide wellbeing dashboard
It transforms raw conversations into actionable guidance for real education stakeholders.

🏆 Real-World Traction (Before the Hackathon)
Seangkatan.id has already received recognition and validation:
✔ Selected for 1:1 Investor Matchmaking – TIACon 2025
Direct invitation to pitch in private investor sessions.

✔ Recognized in the 11th NextDev Scouting
Chosen among promising early-stage digital startups in Indonesia.

✔ Signed LOI with a School (300 students) for pilot deployment
Demonstrates strong real-world demand for wellbeing analytics.

These achievements validate the relevance and market need for AI-DOP & SMID.

🧩 Architecture Overview

This MVP is built entirely inside IBM watsonx Orchestrate using:
Custom AI agent: AI-DOP & SMID
Custom tool: run_ai_dop_analysis
Behavior rules for safety, consistency, and structured outputs
Agentic reasoning to determine required inputs
LLM model: llama-3-2-90b-vision-instruct (Granite-compatible)
Optional: Streamlit visualization for UI demos (local-only)
No backend or infrastructure is required for the hackathon version.

🖥 Optional Prototype UI (Local Streamlit Demo)
To visualize future integration with Seangkatan.id, we built an optional Streamlit UI prototype.

Features:
AI-DOP Text Analyzer
NLP, 3C, SMID breakdown
Risk classification
SMID Dashboard view (aggregated history per student)
Alerts for medium/high risk events
Simulation of teacher-facing and parent-facing insights
This UI is not required for the hackathon, but helps demonstrate future product direction.
Screenshots provided in the repo.

🚀 Demo Instructions (For Hackathon Judges)
Official Demo (watsonx Orchestrate):
https://us-south.watson-orchestrate.cloud.ibm.com/chat


⚠ Important Note
Because this is a hackathon-managed IBM Cloud environment, the chat URL does not contain an agent ID.

To access the project:
Log in using your IBM Cloud Hackathon account

Open Agents
Select AI-DOP & SMID Agent
Start a conversation and paste any student text

🧪 Sample Messages to Test
🔵 Positive
"I enjoy organizing study groups and explaining lessons to my classmates."

🔴 Bullying / Distress
"I'm tired of being mocked every day. It makes me scared to go to school."

🟡 Neutral Reflection
"I like helping my friends, but sometimes I doubt myself when I make mistakes."


The agent will return the full NLP → 3C → SMID → Key Themes structure.

📊 Future Roadmap
After the hackathon, AI-DOP & SMID will evolve into:
Backend integration (FastAPI + watsonx.ai)
Real-time multi-student dashboard
Automated alerts for teachers/parents
Longitudinal wellbeing timeline
Multi-channel observation (text, quiz metadata, interaction patterns)

Integration with the Virtual Homeroom Teacher agent

📘 License
This project is developed exclusively for the IBM watsonx Agentic AI Hackathon.
