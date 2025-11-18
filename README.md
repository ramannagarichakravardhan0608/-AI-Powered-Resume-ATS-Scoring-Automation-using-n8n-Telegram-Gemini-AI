<img width="2880" height="1412" alt="image" src="https://github.com/user-attachments/assets/411311e7-e356-40bd-aeaf-89c12c72f9d9" />

🤖 AI-Powered Resume ATS Scoring & Automation using n8n, Telegram & Gemini AI

🚀 This project is an end-to-end AI-powered automation system built using n8n, Telegram, Google Gemini AI, Google Sheets, Gmail, and PDF Extraction, that:

✔ Accepts resume PDFs from Telegram
✔ Extracts candidate details (Name, Email, Skills)
✔ Uses Gemini AI to generate ATS Score & structured JSON
✔ Stores data automatically into Google Sheets
✔ Sends personalized confirmation emails
✔ Supports bulk resume processing

🛠️ Tech Stack

| Component            | Purpose                     |
| -------------------- | --------------------------- |
| 🚀 n8n               | Workflow Automation         |
| 💬 Telegram          | Resume Upload (Trigger)     |
| ⚙ PDF Extract module | Extract text from resumes   |
| 🧠 Google Gemini AI  | ATS Score & Data Extraction |
| 🐍 Python in n8n     | Data Processing & Cleaning  |
| 📄 Google Sheets     | Resume Data Storage         |
| 📧 Gmail             | Automated Email Responses   |

🌐 Workflow Overview (Based on Screenshot)

Telegram Trigger → IF Check → Switch Node
  ├─ Send Message
  ├─ Extract PDF → Gemini AI → Python Code → Edit Fields → Append to Sheet1 & 2
  └─ Compression → Split Out → Loop Items → Extract PDF (Batch)
        → Gemini AI → Python → Edit → Append Sheets → Send Gmail → Merge → Wait

⚙️ Features

✔ Fully automated resume processing
✔ ATS score generation using Google Gemini AI
✔ JSON formatted output:

{
  "name": "John Doe",
  "email": "john@gmail.com",
  "ats_score": 78,
  "skills": ["Python", "SQL", "Machine Learning"]
}

✔ Saves candidate info into Google Sheets
✔ Sends email notifications to candidate or HR
✔ Batch resume support through Looping & Split Nodes

📸 Workflow Preview

(Add your workflow image here — the one you shared)


🚀 How to Use
1️⃣ Setup Telegram Bot

Use BotFather to create new bot and get API Token.

2️⃣ Create n8n Workflow

Import this n8n JSON workflow file into your dashboard.

3️⃣ Connect Credentials

Add credentials for:

Telegram

Gmail

Google Sheets

OpenAI / Google Gemini API

4️⃣ Enable Workflow

Send resume in Telegram chat, and it will:
✔ Extract → ✔ Analyze → ✔ Score → ✔ Save → ✔ Notify

📬 Email Notification Example

Hi John Doe,

Thank you for sharing your resume!  
📊 Your ATS Score: 78/100  
You are a strong fit for Machine Learning Engineer.

We will contact you if shortlisted.

Regards,  
HR Automation Bot 🤖
⭐ Future Enhancements

Automatic job fit recommendations

HR dashboard for resume ranking

LinkedIn profile analysis

Skill gap detection
