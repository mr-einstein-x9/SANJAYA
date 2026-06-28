# SANJAYA 🤖
> *"Sanjaya uvāca..." — The one who sees all, speaks truth.*

---

## 🕉️ Why SANJAYA?

In the **Bhagavad Gita**, as the great war of Kurukshetra began, King Dhritarashtra — blind, unable to witness the battlefield — turned to his minister and charioteer **Sanjaya**.

The sage Vyasa had gifted Sanjaya with **Divya Drishti** — *divine vision* — the ability to see and hear everything happening on the battlefield, across all distances, without distortion.

Sanjaya didn't exaggerate. He didn't editorialize. He didn't give Dhritarashtra gossip or noise. He watched everything and then spoke only what was true, precise, and necessary.

> *"And so Sanjaya narrated — not what he wished to be true — but what was."*

---

### The Metaphor That Built This App

| Bhagavad Gita | SANJAYA App |
|---|---|
| **Dhritarashtra** — the blind king, wanting to know | **You** — overwhelmed by information, wanting signal |
| **Kurukshetra** — the vast, chaotic battlefield | **The Internet** — AI news, research, breakthroughs happening everywhere |
| **Sanjaya** — granted divine vision, narrates truth | **SANJAYA AI** — crawls all trusted sources, writes only what matters |
| **Divya Drishti** — the ability to see all | **The Agent Pipeline** — arXiv, DeepMind, OpenAI, Nature... all at once |
| **The narration** — crisp, unambiguous, true | **The Post** — one story, clearly explained, no garbage |

> We are all Dhritarashtra — wanting to know what is happening in the Kurukshetra of technology and science, but unable to see it ourselves.
>
> SANJAYA sees it for us. Precisely. Honestly. Without noise.

---

An autonomous AI-powered knowledge feed — Instagram-style UX, no human editors, only trusted intelligence about AI, Tech, Science, and Robotics.

---

## 🧭 Project Philosophy

This project exists on two tracks simultaneously:

| Track 1: Build the Product | Track 2: Learn the Craft |
|---|---|
| Ship real, working features | Understand WHY every decision was made |
| End-to-end functional app | Build transferable, industry-grade skills |
| Deployed and accessible | Document the entire journey |

> **This is not just an app. It's an engineering education roadmap.**

---

## 🏗️ Architecture Overview

```
┌──────────────────────────────────────────────────┐
│              SANJAYA SYSTEM                      │
│                                                  │
│  🕷 Crawler Agent   → Fetches AI news daily      │
│  🧹 Filter Agent    → Picks the best story       │
│  ✍️  Writer Agent   → LLM writes the post        │
│  📤 Publisher Agent → Saves to Supabase          │
│                                                  │
│  📱 Next.js Frontend → Beautiful dark feed UI    │
│  🔐 Supabase Auth   → Google Sign-In             │
│  🗄️  Supabase DB    → PostgreSQL                 │
└──────────────────────────────────────────────────┘
```

---

## 📁 Folder Structure

```
SANJAYA/
├── backend/                    # Python AI agent pipeline
│   ├── agents/                 # The 4 AI agents
│   ├── core/                   # Config, DB, scheduler
│   ├── sources/                # Trusted news sources
│   ├── main.py                 # FastAPI app
│   ├── pipeline.py             # Orchestrator
│   └── requirements.txt
│
├── frontend/                   # Next.js web app (Phase 2)
│
├── ai-conversation-logs/       # Every AI session documented
│   └── 2026-06-28-session-01-brainstorm.md
│
├── dev-journal/                # Learning notes per phase
│
└── README.md
```

---

## 🛠️ Tech Stack

| Layer | Technology | Why |
|---|---|---|
| AI Agents | Python 3.11 + FastAPI | Industry standard for AI/ML |
| LLM | Google Gemini (via LangChain) | Free tier, high quality |
| Database | Supabase (PostgreSQL) | Open-source, transferable skills |
| Authentication | Supabase Auth + Google OAuth | One-click sign-in |
| Frontend | Next.js 14 (App Router) | Dominant React framework |
| Styling | Vanilla CSS (dark theme) | Full control, no magic |
| Hosting | Railway (backend) + Vercel (frontend) | Developer-friendly |

---

## 🗺️ Phases

| Phase | Focus | Status |
|---|---|---|
| **Phase 1** | Python Agent Pipeline Backend | 🔄 In Progress |
| **Phase 2** | Next.js Frontend + Feed UI | ⏳ Planned |
| **Phase 3** | Auth + User Interactions (Like/Save/Share) | ⏳ Planned |
| **Phase 4** | Recommendation Engine | ⏳ Planned |
| **Phase 5** | Deployment + DevOps | ⏳ Planned |
| **Phase 6** | Mobile App (React Native) | 🔮 Future |

---

## 🔑 Environment Variables

Copy `.env.example` to `.env` and fill in your keys:

```bash
cp backend/.env.example backend/.env
```

Required:
- `GEMINI_API_KEY` — from [aistudio.google.com](https://aistudio.google.com) (free)
- `SUPABASE_URL` — from your Supabase project settings
- `SUPABASE_ANON_KEY` — from your Supabase project settings

---

## 🚀 Running the Pipeline (Phase 1)

```bash
# 1. Create virtual environment
cd backend
python -m venv venv
venv\Scripts\activate      # Windows
# source venv/bin/activate   # Mac/Linux

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the pipeline manually
python pipeline.py

# 4. Start the API server
uvicorn main:app --reload
```

---

## 📓 Dev Journal

Every phase has a learning journal in `/dev-journal/`. After each phase:
- What we built (plain English)
- 3 things I learned
- 1 analogy that helped
- What confused me

---

## 🤖 AI Conversation Logs

Every significant AI session is logged in `/ai-conversation-logs/` with:
- Session goal
- Decisions made and WHY
- Code written
- Concepts learned
- Questions that came up

---

*Built with curiosity. Documented with intent. Shipped with purpose.*
