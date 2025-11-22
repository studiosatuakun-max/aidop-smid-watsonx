🚀 AI-DOP & SMID – Seangkatan.id
IBM watsonx Agentic AI Hackathon Project (2025)

AI-DOP (AI Deep Observation Pipeline) is an agentic AI workflow built using IBM watsonx Orchestrate to power student wellbeing intelligence for Seangkatan.id, a social edutech platform for Indonesian middle & high school students.

This system transforms raw student text from multiple school digital-community channels into structured wellbeing insights, supporting teachers, counselors, and parents in early detection of bullying, emotional distress, strengths, and talent indicators.

🌐 About Seangkatan.id

Seangkatan.id is a social edutech platform designed to build healthy digital school communities.
It includes multiple student-generated data channels:
ConfessWall — anonymous emotional expression
RoomChat — classroom & group discussions
Interactive Quizzes — self-reflection & micro-assessment
Digital Mading — student creativity board
Virtual Homeroom Teacher (Wali Kelas Virtual) — evolving AI mentor
These channels generate rich natural-language data which feed directly into the AI-DOP & SMID analysis pipeline.

🧠 What the AI-DOP & SMID Agent Does

The agent produces a structured 4-section wellbeing intelligence report for every student text input:
1. NLP Analysis
Sentiment
Emotion
Toxicity
Keywords & themes

2. 3C Strengths (Triangulation Model)
C1 – Cognition
C2 – Character
C3 – Competence

3. SMID Early-Warning Signals
(Student Measurement Impact Dashboard)
Bullying risk score (LOW / MEDIUM / HIGH)
Emotional distress indicators
Safety & crisis cues
Peer conflict signals

4. Talent Indicators
Detected from linguistic & behavioral cues:
Leadership
Communication
Empathy
Problem-solving
Creativity
Teamwork

5. Key Themes
Concise patterns extracted from the student’s message.

🏆 Real-World Traction (Before Hackathon)

Seangkatan.id has already received validation:

✔ 1:1 Investor Matchmaking – Tech In Asia Conference 2025
✔ Recognized in the 11th NextDev Telkom Scouting
✔ Signed LOI with a School (300 students) for pilot deployment

These milestones validate the demand for AI-powered wellbeing analytics.

🧩 Architecture Overview
This MVP is built entirely inside IBM watsonx Orchestrate, using:
Custom Agent: AI-DOP & SMID Agent
Custom Tool: run_ai_dop_analysis
Behavior Rules: Structured output, safety, anti-hallucination
Model: llama-3-2-90b-vision-instruct (Granite-compatible)
Zero External Backend — all execution happens within Orchestrate
Optional: local Streamlit UI prototype
No servers, no DevOps — pure agentic orchestration.

🖥 Optional Prototype UI (Streamlit Local Demo)
To visualize how the system would integrate into the Seangkatan.id platform, a lightweight Streamlit prototype is included:
AI-DOP text analyzer
Full NLP/3C/SMID breakdown
Risk classification
Historical SMID dashboard (simulated)
Alerts for medium/high-risk events
This is not required by the hackathon but demonstrates the product direction.

🚀 Demo Instructions (For Hackathon Judges)
Official Demo (watsonx Orchestrate)

🔗 https://us-south.watson-orchestrate.cloud.ibm.com/chat

⚠ Note:
Hackathon cloud accounts do not expose agentId in the URL.
To access the demo:
Log in using your IBM Cloud Hackathon credentials
Go to Agents
Select AI-DOP & SMID Agent
Paste any student text and run the analysis

🧪 Sample Messages to Test
🔵 Positive
“I enjoy organizing study groups and explaining lessons to my classmates.”

🔴 Bullying / Distress
“I’m tired of being mocked every day. It makes me scared to go to school.”

🟡 Self-reflection
“I like helping my friends, but sometimes I doubt myself when I make mistakes.”

🟣 Anxiety
"I don’t know why, but lately I feel nervous talking to people."

📸 Screenshots
1. Agent Welcome Screen

(AI-DOP & SMID Agent inside IBM watsonx Orchestrate)
<img width="2048" height="1118" alt="1" src="https://github.com/user-attachments/assets/e8756fd1-3fd5-403c-9990-254bbf8433d6" />

2. Custom Tool – run_ai_dop_analysis
<img width="2048" height="1159" alt="2" src="https://github.com/user-attachments/assets/1ee5772b-b9f9-443c-82be-9f79f45acbf3" />

3. Running the Agent with a Student Message & SMID Result Output
<img width="2048" height="1099" alt="3" src="https://github.com/user-attachments/assets/f9e2caa4-6522-40f9-9779-68529aa9cede" />

5. Streamlit UI (Optional Prototype)
<img width="2880" height="1580" alt="11" src="https://github.com/user-attachments/assets/8eb9eab0-4b68-4e33-b15a-120f44c6dd83" />
<img width="2876" height="1574" alt="22" src="https://github.com/user-attachments/assets/6ae39160-aac3-4745-97ae-f89d6924e9ae" />

📊 Future Roadmap
After the hackathon, AI-DOP & SMID will evolve into:
Full backend integration (FastAPI + watsonx.ai)
Real-time monitoring dashboard
Automated alerts to parents & teachers
Multi-student longitudinal wellbeing timeline
Deeper integration with the “Virtual Homeroom Teacher” agent

📘 License

This project is developed exclusively for the
IBM watsonx Agentic AI Hackathon 2025.
