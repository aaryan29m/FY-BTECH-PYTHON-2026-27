# VIVA Prep — B.Tech CSE Preparation Platform

An AI-powered full-stack web application built for **B.Tech Computer Science & Engineering** students to prepare for university vivas, written exams, technical interviews, and hackathons.

---

## Features

- **Mandatory Authentication Gate:** Strict Email/Password Login & Sign Up powered by **Firebase Authentication** with a show/hide password eye toggle; unauthenticated users cannot access any page or backend API endpoint.
- **Student Command Center Dashboard:** Tracks **XP**, **Daily Study Streak**, **AI Tokens Used**, **Overall Progress**, **6 Unlockable Achievements**, and a **7-Day Activity Chart**, all synced to **Cloud Firestore**.
- **Profile & Settings Slider Drawer:** Compact top-right profile avatar button opens a slide-out drawer to **upload a custom profile picture** (or pick a preset avatar), edit your display name, switch Dark/Light mode, set your default Prep AI model, and log out.
- **3 Focused Preparation Tracks:**
  - **B.Tech CSE** (Core, AI & ML, Data Science, Cyber Security, Cloud Computing)
  - **Interview & Placement** (System Design, Advanced DSA, DBMS, Quantitative Aptitude)
  - **Hackathons & Projects** (Blockchain & Smart Contracts, LLM Prompt Engineering, SIH Pitching & Viva)
- **Permanent Shared Study Knowledge Base:** All 16 B.Tech CSE subjects come pre-populated with **Lessons & Concepts**, **Quick Revision**, and **Question-Wise Viva Q&A**. Clicking **Fetch More with AI** pulls additional notes from Groq AI and saves them permanently in `content_cache.json` for every student.
- **Questions & Live CS (Question-Wise Answers):** Displays subject viva questions with answers directly beneath each question, plus **Live CS Questions** pulled from Open Trivia DB.
- **Accurate Connected Overview:** Tracks real completion across the 6 study sections (starts at `0%` until viewed) with a clickable checklist per subject.
- **Practice Quiz, PDF Syllabus Viva & AI Mock Interview:** Auto-generated multiple-choice quizzes, PyMuPDF-powered PDF syllabus viva generation, and AI answer grading out of 10.
- **Prep AI Floating Assistant:** Always-available AI chat supporting **Super Mode** (`openai/gpt-oss-20b`) and **God Mode** (`openai/gpt-oss-120b`), plus quick-prompt chips.

---

## Tech Stack

| Layer | Technology |
| :--- | :--- |
| **Frontend** | HTML5, CSS3, Vanilla JavaScript |
| **Backend** | Python 3, FastAPI, Uvicorn, HTTPX |
| **Authentication & Database** | Firebase Authentication, Cloud Firestore |
| **Shared Content Store** | JSON (`backend/content_cache.json`) |
| **AI Provider** | Groq API (`openai/gpt-oss-20b` & `openai/gpt-oss-120b`) |
| **PDF Processing** | PyMuPDF (`fitz`) |
| **Deployment** | Docker |

---

## Repository Structure

```text
mini-project/
├── README.md
├── .gitignore
├── screenshot/
│   ├── login.png
│   ├── dashboard.png
│   ├── workspace.png
│   ├── profile.png
│   └── prep-ai.png
└── source-code/
    ├── Dockerfile
    ├── backend/
    │   ├── main.py
    │   ├── content_cache.json
    │   ├── requirements.txt
    │   └── .env.example
    └── frontend/
        ├── index.html
        ├── style.css
        └── script.js
```

---

## Screenshots

### Login & Sign Up Gate
![Login Screen](screenshot/login.png)

### Student Command Center Dashboard
![Dashboard](screenshot/dashboard.png)

### B.Tech CSE Workspace
![Workspace](screenshot/workspace.png)

### Profile & Settings Drawer
![Profile Drawer](screenshot/profile.png)

### Prep AI Chatbot
![Prep AI](screenshot/prep-ai.png)

---

## How to Run Locally

### 1. Clone the repository
```bash
git clone https://github.com/aaryan29m/mini-project.git
cd mini-project/source-code/backend
```

### 2. Configure your Groq API Key
Create a `.env` file inside `source-code/backend/` (or copy `.env.example`):
```env
GROQ_API_KEY_1=your_groq_api_key_here
GROQ_API_KEY_2=
```

### 3. Install dependencies & start the server
```bash
python3 -m pip install -r requirements.txt
python3 -m uvicorn main:app --reload
```
*(On Windows PowerShell, use `python` instead of `python3`.)*

### 4. Open in Browser
Visit **`http://127.0.0.1:8000`**, create an account or log in, and start preparing.

---

## Author

**Aaryan Chandrakant Mahalle**  
B.Tech Computer Science & Engineering — MIT World Peace University  
GitHub: [@aaryan29m](https://github.com/aaryan29m)
