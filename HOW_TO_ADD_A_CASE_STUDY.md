# How to Add the Next Case Study (Portfolio Maintenance Habit)

**Assignment:** General AI Fluency · Impact Project (`FL`) · Week 6  
**Student:** Jezreal Momoh  
**Live Portfolio:** [https://jezreal-momoh-portfolio.netlify.app](https://jezreal-momoh-portfolio.netlify.app)  
**Repository:** [https://github.com/jezreal-dev/portfolio](https://github.com/jezreal-dev/portfolio)  
**Calendar Reminder File:** [`reminders/add-next-case-study.ics`](./reminders/add-next-case-study.ics)

---

## 1. Exactly Where the Next Case Study Goes

- **Primary slot (Project Card):** [`site/index.html`](./site/index.html) inside `<div class="project-grid">` (under `<section id="work">`).
- **Optional deep-dive link (Write-up):** [`site/index.html`](./site/index.html) inside `<ul class="notes-list">` (under `<section id="notes">`).
- **Grid rule:** The grid uses a clean 2-column desktop layout (`repeat(2, minmax(0, 1fr))` in [`site/styles.css`](./site/styles.css)) and stacks to 1 column on mobile. Add a new `<article class="project-card">` (or replace the oldest hackathon project if keeping a tight 4-card 2×2 grid).

### Copy-Paste Card Template
```html
<article class="project-card">
  <div class="project-topline">
    <span class="project-number">05</span>
    <span class="tag">Stack · Domain</span>
  </div>
  <h3>Project Name</h3>
  <p>Two plain sentences distilled from the three-beat draft: what broke, what I built/decided, and the verified outcome.</p>
  <a class="text-link" href="https://github.com/jezreal-dev/REPO-URL" target="_blank" rel="noopener noreferrer">View repository <span aria-hidden="true">↗</span></a>
</article>
```

---

## 2. Steps to Add a New Case Study (10-Minute Habit)

1. **Open the preserved Claude Project** (`FlyRank Portfolio & Brand`) — it already holds my Voice Card, technical stack, and design tokens so drafting takes one short conversation instead of a rebuild.
2. **Draft in the Week 2 three-beat shape** (from `Frame_It_As_Cases_Jezreal_Momoh.pdf`):
   - **The Problem:** What concrete pain or failure existed before the build.
   - **What I Did & Decided:** The architecture and the specific engineering trade-off I made.
   - **What Came of It:** Measurable result, test score, or verified live proof.
3. **Condense to 2 plain sentences** matching the Voice Card (*Direct, warm, plain, zero buzzwords*) and insert a new `<article class="project-card">` inside `<div class="project-grid">` in `site/index.html`.
4. **Add a write-up link (optional):** If the project has a detailed README or architecture doc, add one `<li><a class="note-item" ...>` entry inside `<ul class="notes-list">` in `site/index.html`.
5. **Verify before deploy:** Open `site/index.html` locally, check mobile width (`375px`) for overflow/tap targets, and verify the new GitHub/demo URL returns HTTP `200`.
6. **Commit, push, and deploy:**
   ```bash
   cd "/home/jmomoh/FlyRank AI/portfolio"
   git add site/index.html
   git commit -m "feat(work): add case study 05"
   git push origin main
   ```
   Then drag `portfolio/site/` into the existing Netlify site's **Deploys** page (`https://app.netlify.com/projects/jezreal-momoh-portfolio/deploys`).

---

## 3. Named Next Real Piece of Work & Concrete Reminder

- **Named Next Case Study:** **FlyRank Source-Grounded Study Coach Agent (`FL-07`)** — n8n + Fireworks GLM 5.3 Flash + Dockerized Python local tool server (`Week 5/agent/study_coach_server.py`). *(Queued next after that: the Week 7 Durable Background Job & Async Report Pipeline.)*
- **Three-Beat Seed Ready for Drafting:**
  - **The Problem:** Standard AI chat tools hallucinate lecture details and misquote speaker names when quizzing you on personal study notes.
  - **What I Did & Decided:** Built a self-hosted n8n agent powered by Fireworks GLM 5.3 Flash connected over a private Docker network to a local Python tool server. Rather than dumping whole transcripts into context, I gave the agent targeted read/search endpoints returning exact sentence IDs, and locked file writes behind an explicit human approval gate.
  - **What Came of It:** End-to-end runs explain Week 5 concepts with verifiable sentence citations, recover autonomously from zero-match searches, and never modify files without manual confirmation.
- **Concrete Reminder Set:**
  - **Date & Time:** Friday, November 27, 2026 at 10:00 AM (Africa/Lagos, GMT+1)
  - **Recurrence:** Monthly on the 27th for 6 months (standing portfolio hygiene check)
  - **Alert:** 30 minutes prior
  - **Calendar Artifact:** [`reminders/add-next-case-study.ics`](./reminders/add-next-case-study.ics)

---

## 4. Preserved Build Context (Claude Project Identity Kit)

Preserved in my Claude Project (and mirrored here in Git so it is never lost):

- **Voice Card:** Direct, warm, plain, zero buzzwords. No "synergizes", "cutting-edge", or "leveraging".
- **Proof Statement:** I build backend systems and practical AI tools with Go and Python, backed by production-tested APIs, multi-agent reviewers, resilient scrapers, and live serverless integrations.
- **Core Stack:** Go, Python, FastAPI, PostgreSQL, LangGraph, MCP, n8n, Pydantic, Docker, Netlify.
- **Visual System (`site/styles.css`):** Light editorial palette (`--page: #faf9f6`, `--surface: #ffffff`, `--ink: #18181b`, `--muted: #52525b`, `--accent-dark: #1d4ed8`), zero build pipeline, semantic HTML + single CSS file, 44px+ mobile touch targets, 16px form inputs.
- **Contact / One Action CTA:** Direct Netlify contact form (`#contact`) + 15-minute Calendly intro call (`https://calendly.com/laerzej/15-minute-intro-call`).
