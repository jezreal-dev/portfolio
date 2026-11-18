# Survive the Crit — Portfolio Design & Proof Review

**Assignment:** Survive the Crit · Week 6 (Build+) · General AI Fluency  
**Student:** Jezreal Momoh  
**Live Site:** [https://jezreal-momoh-portfolio.netlify.app](https://jezreal-momoh-portfolio.netlify.app)  
**Repository:** [https://github.com/jezreal-dev/portfolio](https://github.com/jezreal-dev/portfolio)  
**Date:** November 18, 2026

---

## 1. Proof Statement Submitted to Reviewer

> *"I build backend systems and practical AI tools with Go and Python. I prove this through production-tested systems: multi-agent security reviewers, structured LLM APIs with schemas and evals, resilient scraping pipelines, and a live serverless contact pipeline."*

---

## 2. Raw Reviewer Feedback (Collected Without Defending)

**Reviewer:** Senior Backend AI Engineering Critique (structured design & technical proof audit)

### Question 1: In ten seconds, what do I do?
> *"You are a Backend AI Engineer working in Go and Python who builds APIs, data pipelines, and practical model integrations. The eyebrow ('Backend AI Engineer · Ilorin, Nigeria') and headline communicate this immediately without fluff."*

### Question 2: Would you believe I'm good at it?
> *"Mostly yes, because the code links are public and the technical scope is specific—not buzzwords. However, two gaps hurt credibility right now:*
> 1. *Your strongest backend AI proof (the FastAPI LLM Enrichment endpoint with Pydantic schemas, repair retries, quarantine logs, timeouts, and 8/8 passing evals) isn't even on the page! You're claiming practical LLM integration as a core strength while leaving your best production API out of the Selected Work section.*
> 2. *The 'Notes' dark panel at the bottom is an empty promise box ('I'll add project notes here as they're ready') with a big arrow pointing nowhere. Clicking 'Notes' in the nav lands on a dead end. That reads like an unfinished template.*
> 3. *In the Contact section, having the form plus three secondary buttons right below it creates slight action clutter; it isn't obvious whether you prefer the form or clicking Email.*
> 4. *Later on, it would be nice to see an interactive demo or availability badge in the hero, and maybe a dark mode toggle."*

---

## 3. Honest Feedback Sort: Must-Fix vs. Nice-to-Have

| Feedback Item | Category | Why It Belongs Here |
| :--- | :--- | :--- |
| **Missing Flagship Backend API (`POST /enrich`)** | **Must-Fix** | Directly weakens the proof statement. Claiming LLM integration mastery without showing the production FastAPI + Pydantic + Evals service leaves the strongest evidence off the page. |
| **Dead-End "Notes" Placeholder Box** | **Must-Fix** | Hurts trustworthiness immediately. An unclickable arrow and "coming soon" text make a finished portfolio look incomplete. |
| **Action Clutter in Contact Section** | **Must-Fix** | Hurts the single primary action. Having a "Direct Email" button immediately below an active email contact form confuses visitors on which path to take. |
| **Interactive Terminal / Live Demo Widget** | **Nice-to-Have** | Great addition for a future capstone iteration, not required for the core proof to land today. |
| **"Available for Roles" Status Badge** | **Nice-to-Have** | Helpful visual cue for recruiters, easy to add later when actively interviewing. |
| **Dark / Light Theme Toggle** | **Nice-to-Have** | Pure preference polish; current light palette already passes WCAG AA/AAA contrast cleanly. |

---

## 4. Must-Fixes Implemented & Reply to Reviewer

### Reply Sent Back
> *"Thank you for the direct feedback—you caught two blind spots I had stopped noticing after staring at the page. I didn't realize how unfinished the empty 'Notes' panel looked until you pointed it out, and leaving the LLM Enrichment API off the homepage was a clear miss. Here is what I fixed:"*

### Concrete Changes Applied to the Site
1. **Added Flagship Backend AI Proof (`site/index.html`, `site/styles.css`):**
   - Added **02 · LLM Enrichment API** (`FastAPI · Pydantic · Evals`) to Selected Work, linking directly to [`BE-01-crud-api`](https://github.com/jezreal-dev/flyrank-backend-ai-engineering/tree/main/BE-01-crud-api) with its `POST /enrich` contract, repair loop, quarantine log, 12s timeout, kill switch, and 8/8 eval score.
   - Updated `.project-grid` from a 3-column layout to a balanced 2×2 grid on desktop (stacking cleanly to 1 column on mobile) so all 4 projects have generous visual space.
2. **Replaced Dead-End Notes Box With Live Technical Writing (`site/index.html`, `site/styles.css`):**
   - Removed the "coming soon" copy and unclickable arrow.
   - Rebuilt `#notes` as **Engineering notes & write-ups** with three live, clickable links to real technical documentation:
     - *Putting an LLM Behind a Production API* (schemas, repair loops, quarantine & 8/8 evals)
     - *From Static Poster to Working Tool* (serverless edge forms & end-to-end data flow)
     - *Mobile-First Audit & Fix Log* (iOS input zoom, 44px touch targets & contrast)
3. **Clarified Primary vs. Secondary Contact Actions (`site/index.html`, `site/styles.css`):**
   - Kept the working Netlify contact form as the unmistakable primary action (*"Send a direct message below—it lands straight in my inbox"*).
   - Separated Calendly and LinkedIn below a clean hairline divider labeled *"Prefer to talk live or connect elsewhere?"* and removed the redundant "Direct Email" button (email remains accessible in the footer).

---

## 5. Additional Peer / Friend Check (Optional Follow-Up Template)

To double-check the updated live site with friends or fellow interns, send this exact prompt:

> *"Hey, could you open `https://jezreal-momoh-portfolio.netlify.app` for 10 seconds and tell me two honest things? (1) In ten seconds, what do I do? (2) Would you believe I'm good at it—and did anything feel confusing or unfinished?"*
