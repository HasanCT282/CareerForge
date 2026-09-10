<div align="center">

# 🔥 CareerForge

### AI-Powered Career Guidance & Interview Platform

Upload your CV. Discover your path. Walk into every interview ready.

<br/>

![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-Frontend-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-Frontend-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-Agents-1C3C3C?style=for-the-badge)
![Gemini](https://img.shields.io/badge/Gemini-API-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-Database-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Deployment-2496ED?style=for-the-badge&logo=docker&logoColor=white)

![License](https://img.shields.io/badge/license-MIT-8A2BE2?style=flat-square)
![Status](https://img.shields.io/badge/status-in%20development-9370DB?style=flat-square)
![PRs](https://img.shields.io/badge/PRs-welcome-6A5ACD?style=flat-square)

</div>

<br/>

<div align="center">
  <img src="https://raw.githubusercontent.com/Ileriayo/markdown-badges/master/svg/line-break.svg" width="0" height="1"/>
</div>

## 🧭 Overview

**CareerForge** is an AI-powered platform that helps students and job seekers figure out which career path fits them — and then get them ready to land it. Upload a CV, and the system analyzes skills and experience, surfaces gaps, recommends careers, builds a personalized learning plan, and runs realistic, adaptive mock interviews with real feedback.

It's two products in one: a **career compass** and an **interview simulator** — built on a single agentic pipeline so the guidance you get and the interview you practice are always grounded in the same understanding of who you are.

> Most students don't fail interviews because they're unprepared for the *job*. They fail because they never knew which job to prepare for. CareerForge closes that loop.

<br/>

## ❓ The Problem

- Students graduate unsure which careers actually fit their skill set.
- Skill gaps stay invisible until a rejection makes them obvious.
- Interview prep is generic — not tailored to *your* CV or the *specific* role.
- Feedback loops are slow, vague, or nonexistent.

**CareerForge** turns a CV into a personalized roadmap — and a realistic dry run of the interview at the end of that roadmap.

<br/>

## ✨ Features

| | |
|---|---|
| 📄 **CV Upload & AI Analysis** | Parses your CV and extracts structured signal from unstructured text |
| 🧠 **Skill & Experience Identification** | Identifies what you actually know, not just what you listed |
| 🎯 **Career Recommendations** | Suggests roles that map to your real skill profile |
| 📊 **Skill Gap Analysis** | Shows exactly what's missing between where you are and where you want to be |
| 🗺️ **Personalized Learning Plan** | A concrete, sequenced plan to close the gap |
| 🎙️ **Real-Time AI Mock Interview** | Adaptive interview sessions powered by an agentic pipeline |
| 🧩 **CV & Job-Role Based Questions** | Questions generated from *your* CV and the *target* role — not a generic bank |
| 🔁 **Follow-Up Questions & Answer Evaluation** | The AI probes weak answers the way a real interviewer would |
| 📈 **Interview Feedback & Improvement Suggestions** | Actionable, structured feedback after every session |

<br/>

## 🔄 Core Flow

```
  CV Upload
      │
      ▼
  AI Analysis
      │
      ▼
  Skills & Career Recommendations
      │
      ▼
  Skill Gap Analysis
      │
      ▼
  Personalized Learning Plan
      │
      ▼
  AI Mock Interview
      │
      ▼
  Answer Evaluation
      │
      ▼
  Feedback & Improvement Suggestions
```

<br/>

## 🏗️ Architecture

```
┌─────────────────────┐        ┌──────────────────────────┐        ┌──────────────────┐
│  React + TypeScript  │ ─────▶ │      FastAPI Backend      │ ─────▶ │   LangGraph Agent  │
│  (Upload · Chat UI)  │ ◀───── │  (REST API · Auth · CRUD) │ ◀───── │   Pipeline (Gemini) │
└─────────────────────┘        └──────────────┬────────────┘        └─────────┬─────────┘
                                               │                               │
                                               ▼                               ▼
                                   ┌───────────────────────┐        ┌──────────────────────┐
                                   │         MySQL          │        │   PyMuPDF CV Parser   │
                                   │   (users, sessions,     │        │  (text extraction)   │
                                   │    interviews, plans)   │        └──────────────────────┘
                                   └───────────────────────┘
```

<br/>

## 🛠️ Tech Stack

<div align="center">

| Layer | Technology |
|---|---|
| **Frontend** | React + TypeScript |
| **Backend** | FastAPI |
| **AI / LLM** | Gemini API |
| **Agent Orchestration** | LangGraph |
| **CV Processing** | PyMuPDF |
| **Database** | MySQL |
| **Deployment** | Docker · Render / Railway |

</div>

<br/>

## 📂 Project Structure

```
CareerForge/
├── backend/
│   ├── app/
│   │   ├── agents/          # LangGraph agent graphs (analysis, interview, evaluation)
│   │   ├── api/              # FastAPI route definitions
│   │   ├── core/             # Config, security, settings
│   │   ├── models/           # DB models & schemas
│   │   ├── services/         # CV parsing, career matching, feedback generation
│   │   └── utils/            # Shared helpers
│   ├── tests/
│   ├── main.py
│   └── requirements.txt
├── frontend/
│   ├── src/
│   │   ├── pages/             # Route-level views
│   │   ├── components/        # Reusable UI components
│   │   ├── api/                # API client / axios calls to the backend
│   │   ├── hooks/              # Custom React hooks
│   │   └── App.tsx
│   ├── public/
│   ├── package.json
│   └── tsconfig.json
├── docs/                     # Architecture notes, API docs
├── .github/workflows/        # CI pipelines
├── docker-compose.yml
├── .env.example
└── README.md
```

<br/>

## 🚀 Getting Started

### Prerequisites
- Python 3.11+
- Node.js 18+ and npm/yarn
- MySQL instance
- A Gemini API key
- Docker (optional, for containerized setup)

### 1. Clone the repo
```bash
git clone https://github.com/<your-username>/CareerForge.git
cd CareerForge
```

### 2. Backend setup
```bash
cd backend
python -m venv venv
source venv/bin/activate          # Windows: venv\Scripts\activate
pip install -r requirements.txt
cp ../.env.example .env           # fill in your GEMINI_API_KEY and DB credentials
uvicorn main:app --reload
```

### 3. Frontend setup
```bash
cd frontend
npm install
npm run dev
```

### 4. Or run everything with Docker
```bash
docker compose up --build
```

<br/>

## 🗺️ Roadmap

- [ ] CV upload & parsing pipeline
- [ ] Career recommendation engine
- [ ] Skill gap analysis module
- [ ] Personalized learning plan generator
- [ ] Real-time AI mock interview agent
- [ ] Answer evaluation & feedback engine
- [ ] Deployment to Render / Railway

<br/>

## 🤝 Contributing

Contributions, issues, and feature requests are welcome. Feel free to open a PR or start a discussion.

## 📄 License

This project is licensed under the [MIT License](LICENSE).

<br/>

<div align="center">

**CareerForge** — helping you understand your path, and proving you're ready to walk it.

</div>