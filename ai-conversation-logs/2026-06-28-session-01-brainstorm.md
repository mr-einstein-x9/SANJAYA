# AI Conversation Log — Session 01
### Topic: SANJAYA — Brainstorm, Planning & Architecture
### Date: 2026-06-28
### Duration: ~45 minutes

---

## 🎯 Session Goal
Turn the idea of "Instagram but for tech/AI news, run by AI agents" into a concrete, buildable plan.

---

## 💡 The Idea (In My Own Words)

An app called **SANJAYA** that:
- Looks and feels like Instagram (vertical feed, cards, likes, saves)
- Posts content automatically — no human writes anything
- AI agents crawl trusted websites (arXiv, OpenAI, etc.) and find news
- AI writes a crisp, clear summary of the news (like a smart friend explaining it)
- Instead of a comment section → curated links to original sources, papers, and explainers
- Users can like (improves recommendation), save, share, open external links

---

## 🤖 Key Decisions Made (and WHY)

### 1. Web First
**Decision:** Build a web app (mobile-web optimized) before a native mobile app.
**Why:** Faster to iterate. Same codebase for mobile + desktop. Next.js is the right tool.

### 2. Dark Mode Only
**Decision:** The entire app is dark mode, non-negotiable.
**Why:** Dark = futuristic, tech-focused, easier on eyes during late-night research. Matches the "command center for curious minds" aesthetic.

### 3. AI 🤖 Niche Only at Launch
**Decision:** Start with just AI news. One post per day. Best story wins.
**Why:** Better to do one thing perfectly than four things poorly. Quality over quantity. AI is also the most popular niche for the target audience.

### 4. Google Sign-In Only
**Decision:** No email/password, no Apple Sign-In. Google only.
**Why:** Fastest user experience. No password to forget. One click. Target audience (CS/AI students, tech folks) all have Google accounts.

### 5. User Interactions: Like · Save · Share · Link
**Decision:** These 4 interactions only. No commenting.
**Why:** Likes feed the recommendation engine. Save = personal library. Share = growth loop. External link = the whole point (get people to the real source). No comments = keeps SANJAYA clean and knowledge-focused.

### 6. Free Now, Monetize Later
**Decision:** No ads, no paywall at launch.
**Why:** Build audience first. Monetization options stay open. The right business model emerges from real user behavior.

### 7. Python + FastAPI + LangChain for Backend
**Decision:** Python ecosystem for the AI agent pipeline.
**Why:** Python is THE language for AI/ML. LangChain is the standard abstraction layer for LLM apps. FastAPI is modern, fast, and well-documented. As a CS/AI student — this is exactly what industry uses.

### 8. Supabase for Database + Auth
**Decision:** Supabase over Firebase, PlanetScale, or raw Postgres.
**Why:**
- Open-source Postgres (skills transfer everywhere)
- Built-in Google OAuth
- Python SDK
- Free tier
- Real-time subscriptions (useful for feed later)
- Best learning investment for a student

### 9. Build Agent Backend First
**Decision:** Before any UI, make the AI pipeline work.
**Why:** If the AI output is bad, the whole product is bad. Validate the core before building the shell.

---

## 🔄 The /grill-me Q&A (Compressed)

| Question | My Answer |
|---|---|
| Agent refresh cycle? | Once per day — 1 best post. Enhance later. |
| Sign-in method? | Google only |
| Monetization? | Free now |
| Dark or light? | Dark only |
| Web layout target? | Mobile-web first |
| How many niches? | Just one |
| Which niche? | AI 🤖 |
| Backend stack? | Python + FastAPI + LangChain |
| Database? | Something beginner-friendly but production-ready |
| First thing to build? | Agent pipeline — make the AI work first |

---

## 🧠 Key Shift: Learning-First Philosophy

**Late in the session, I clarified my real goal:**
> I want to learn different frameworks and skills while building, not just ship code fast. The communication log with AI during the build is important too.

**This changed everything.** The plan became:
1. Build the product (real, working, deployed)
2. Learn the craft deeply at each step (understand WHY, not just HOW)
3. Keep a dev journal per phase
4. Log every AI conversation (like this file)
5. Understand concepts before moving on

The analogy that works for me:
> Learning to cook vs. ordering takeout. Takeout is faster. But cooking teaches you to feed yourself forever.

---

## 📋 What's Planned Next

**Phase 1** — Python Backend Agent Pipeline:
1. Project setup (virtual env, requirements, .env)
2. RSS feed fetching from trusted AI sources
3. Crawler Agent → Filter Agent → Writer Agent → Publisher Agent
4. Supabase database setup + schema
5. FastAPI endpoints
6. Daily scheduler

**Phase 2** (later) — Next.js frontend, then React Native mobile

---

## 💭 What Confused Me / Open Questions
- How does LangChain actually differ from calling the Gemini API directly?
- What exactly is pgvector and when do I need it?
- How does Supabase Row Level Security work?

*(These will be answered in the Phase 1 dev journal)*

---

## 🔗 Key Resources to Bookmark
- [Supabase Docs](https://supabase.com/docs)
- [FastAPI Docs](https://fastapi.tiangolo.com)
- [Google AI Studio (Gemini API)](https://aistudio.google.com)
- [LangChain Docs](https://python.langchain.com)
- [arXiv RSS Feeds](https://arxiv.org/help/rss)

---

## 🕉️ The Most Important Thing Said This Session — The Name

At the very end of the session, I shared something that reframes everything:

> *"I am curious and explore the internet but still feel like I'm not managing to get every information. Then I was reminded of an idea from the Bhagavad Gita — there is a character named Sanjaya who was a charioteer given Divya Drishti (divine vision) and could see everything, anywhere, and then concisely and precisely explain real talks and things without ambiguity and with true words. We are like Dhritarashtra — wanting to know what is happening in Kurukshetra. Sanjaya will find and tell us what we need to know only — not garbage information."*

### Why This Changes Everything

This isn't just a clever name. It's a **design philosophy** encoded into the product name:

| Principle from Sanjaya (Gita) | Design Rule for the App |
|---|---|
| Divya Drishti — sees everything | Agents crawl ALL trusted sources, nothing missed |
| Speaks without bias | AI summaries are neutral, factual, not sensational |
| Only what Dhritarashtra needs | 1 post/day — the BEST story only, no flood |
| No embellishment, no noise | Clean UI, no comment toxicity, no clickbait |
| Narrates with precision | Crisp 3–5 sentence summaries, one key insight |
| The king trusts him completely | Users trust SANJAYA because it earns it, every day |

### The Product Vision, Rewritten

**Before:** "An Instagram-like app for AI news."

**After:** "You are Dhritarashtra — you want to know what is happening in the Kurukshetra of technology and science. You cannot see it yourself — there is too much noise, too many sources, too much chaos. SANJAYA has Divya Drishti. Every day, it watches the entire battlefield and tells you only what you truly need to know."

### This Becomes the App's Mission Statement

> *"In a world drowning in information, be the Sanjaya — see everything, speak only truth."*

---

*Next session: Setting up the Python project structure and understanding what a virtual environment actually is.*
