# Send the Link: Launch, Demo & Story — Capstone Deliverable

**Course Track:** General AI Fluency (Cross-cutting with Backend AI Engineering)  
**Milestone:** Week 8 / Week 10 Capstone (`FL-CAPSTONE`)  
**Assignment ID:** `CUSTOM-MQX0QS1O-B788D1AA`  
**Candidate:** Jezreal Momoh (`jezreal-dev`)  
**Live Portfolio URL:** [https://jezreal-momoh-portfolio.netlify.app](https://jezreal-momoh-portfolio.netlify.app)  
**GitHub Repository:** [https://github.com/jezreal-dev/portfolio](https://github.com/jezreal-dev/portfolio)  
**Verified Credential:** [FR-D11-556C8-0CB4D](https://internship.flyrank.ai/verify/FR-D11-556C8-0CB4D?first_name=Jezreal)  
**Deliverable PDF:** [`Week 8/submissions/Capstone_Send_the_Link_Launch_Demo_Story_Jezreal_Momoh.pdf`](file:///home/jmomoh/FlyRank%20AI/Week%208/submissions/Capstone_Send_the_Link_Launch_Demo_Story_Jezreal_Momoh.pdf)

---

## 1. Executive Summary: The Capstone Package

The difference between a transient student class artifact and an enduring career asset is **The Compounding Habit**. A static portfolio that never receives a second project goes stale within months. This capstone brings together all four foundational elements built across the FlyRank curriculum:

1. **The Launched Portfolio:** Live on a permanent domain over HTTPS (`https://jezreal-momoh-portfolio.netlify.app`), proving one clear engineering claim (*"I build backend systems and practical AI tools in Go and Python"*), with real production-grade code repositories and zero fluff.
2. **The Honest Build-in-Public Story:** A 250-word transparent account of building with AI—highlighting one real win and one real engineering failure caught during adversarial testing.
3. **The 3-to-5 Minute Demo & Walkthrough Script:** A structured, beat-by-beat screen walkthrough demonstrating the live site, the dynamic Netlify Forms contact system with client-side anti-spam defenses, and the verified FlyRank graduate badge.
4. **The Compounding Runbook & Named Next Piece:** A concrete 10-minute protocol to add the next case study, naming Case Study #05 (**LLM Usage Metering & Billing Engine**), backed by an active calendar reminder artifact (`add-next-case-study.ics`) and preserved Claude Project context.

---

## 2. The Launched Portfolio: Verification & Architecture

- **Domain & Hosting:** Deployed to Netlify Edge CDN with automated TLS certificates (`Let's Encrypt`) and HSTS enabled.
- **Speed & Weight:** 100% vanilla ES2022 JavaScript, clean semantic HTML5, and a single custom CSS file (`styles.css`). Zero build steps, zero bloated client-side frameworks, and sub-500ms initial paint.
- **Privacy-Friendly Telemetry:** Integrated with Cloudflare Web Analytics and GoatCounter—gathering visitor traffic and referral insights without intrusive cookie banners or GDPR tracking consent.
- **Social Sharing Hygiene:** High-resolution Open Graph (`og-card.png`, 1200×630px) and Twitter Card tags verified for intentional link preview rendering across LinkedIn, X, Slack, and email.
- **Accessibility:** Tested against WCAG 2.1 AA standards: skip-link navigation (`#main`), 44px+ mobile touch targets, semantic headings (`h1` through `h3`), and high contrast ratios (>7:1 on body text).
- **FlyRank Graduate Badge:** Official verified badge embedded in the site footer linking directly to credential `FR-D11-556C8-0CB4D`.

---

## 3. The Honest Build-in-Public Launch Story

> **Post Title:** How I Built My Backend AI Engineering Portfolio with AI (The Wins, The Cracks, and What Stuck)  
> **Target Channels:** LinkedIn, X, and the FlyRank Showcase  
> **Word Count:** 265 words  
> **Voice:** Direct, warm, plain, zero buzzwords (conforming to my Voice Card).

```markdown
I used to think a portfolio was something you put off until you had a dozen "perfect" projects. Ten weeks ago, I started the FlyRank Backend AI Engineering internship with one rule: don't study your way in—build your way in.

Today, my personal portfolio is live at https://jezreal-momoh-portfolio.netlify.app.

Here is the honest story of building it alongside an AI agent:

The Win:
AI did the heavy lifting where speed mattered most: generating responsive CSS scaffolding, scaffolding Pydantic schemas, and automating repetitive unit tests. That saved me dozens of hours of typing boilerplate, allowing me to focus my energy on architecture, system trade-offs, and adversarial error boundaries.

The Failure (and What I Learned):
During our "Break Your Own Site" testing, the site cracked. The contact form hung indefinitely when tested on simulated slow 3G networks because it lacked a network timeout. Rapid double-clicks triggered multiple webhook submissions, and blank whitespace inputs passed through silently. 

Rather than hiding the cracks, I hardened them: I added an AbortController with a 12-second timeout, locked the submit button during in-flight requests, implemented a 5-second cooldown, and added strict whitespace sanitization.

What Comes Next:
A portfolio that only showcases graduation work goes stale. I've set up a 10-minute protocol and a monthly calendar reminder to add my next production piece: an enterprise LLM Usage Metering & Billing Engine with integer microcents math and cryptographic Stripe webhooks.

Backend first. AI where it helps. Verified by code.
```

---

## 4. The 3-to-5 Minute Demo & Walkthrough Script

| Timecode | Visual / Screen Focus | Audio & Spoken Narration Script | Key Evaluator Objective |
| :--- | :--- | :--- | :--- |
| **0:00 – 0:45** | Hero section at `https://jezreal-momoh-portfolio.netlify.app` | *"Hi, I'm Jezreal Momoh, a Backend AI Engineer based in Ilorin, Nigeria. This is my live portfolio. The hero section makes my core proof statement clear in five seconds: I build Go and Python services, APIs, and model integrations with rigorous testing. Notice the direct actions: download my verified engineering CV or jump straight to selected work."* | Proves core claim in < 5 seconds; clean editorial hierarchy. |
| **0:45 – 1:45** | Scrolling through `#work` (Projects 01 to 04) | *"Section two shows my four core projects: Themis (multi-agent security reviewer using LangGraph), LLM Enrichment API (FastAPI with strict Pydantic schemas and 8/8 evals), GemmaRoute (dynamic model routing), and The Polite Scraper. Every single project card links directly to public GitHub source code and architectural documentation."* | Proves real work, GitHub source code, and absence of fake placeholders. |
| **1:45 – 3:00** | Interactive contact form testing (`#contact`) | *"Now, let's look at the one dynamic feature: the contact form. This isn't a static `mailto:` link. It connects to Netlify's edge form handler. Watch what happens when I type spaces and hit send: client-side validation catches it immediately. When I fill in real details and submit, the button disables to prevent double-submits, an AbortController enforces a 12-second timeout, and upon success, a clear confirmation appears without reloading the page."* | Demonstrates dynamic feature working on a fresh attempt + adversarial safety. |
| **3:00 – 3:45** | Footer: Graduate Badge & Code Audit | *"In the footer, you can see the official FlyRank Graduate Badge. Clicking 'Verify' opens my live credential record `FR-D11-556C8-0CB4D`. Here in the source code, you can see privacy-first analytics from Cloudflare and GoatCounter—zero cookies, zero banners, 100% respecting visitor privacy."* | Proves graduate badge integration, credential verification, and analytics. |
| **3:45 – 4:30** | Runbook & Calendar Reminder preview | *"Finally, to keep this platform compounding, I don't start from scratch for future projects. I have an active iCalendar reminder set for the 27th of every month, a 10-minute three-beat case study template, and my preserved Claude Project holding my voice card and design tokens. My next case study—an enterprise LLM metering engine—is already scheduled."* | Proves the compounding habit and preserved build context. |

---

## 5. The Compounding Habit: Runbook for Case Study #05

### Exactly Where the Next Case Study Goes
1. **Primary Project Card Slot:** `portfolio/site/index.html` inside `<div class="project-grid">` (under `<section id="work">`).
2. **Deep-Dive Write-Up Link Slot:** `portfolio/site/index.html` inside `<ul class="notes-list">` (under `<section id="notes">`).
3. **Card Grid Layout:** The project grid uses CSS Grid (`repeat(2, minmax(0, 1fr))` on desktop, collapsing to 1 column on mobile). Card #05 can be appended to create a 5th card or rotated into a tight 4-card showcase.

### Copy-Paste Card Template (Conforming to `site/styles.css`)
```html
<article class="project-card">
  <div class="project-topline">
    <span class="project-number">05</span>
    <span class="tag">FastAPI · SQLite WAL · Stripe</span>
  </div>
  <h3>LLM Usage Metering &amp; Billing Engine</h3>
  <p>An enterprise metering engine with pure integer microcents math, RFC Idempotency-Key deduplication, pre-action 429/402 quota barriers, and cryptographic HMAC-SHA256 Stripe webhook sync.</p>
  <a class="text-link" href="https://github.com/jezreal-dev/flyrank-capstone-metering-billing" target="_blank" rel="noopener noreferrer">View repository <span aria-hidden="true">↗</span></a>
</article>
```

### The 10-Minute 6-Step Publishing Loop
1. **Open Preserved Claude Project:** Open `FlyRank Portfolio & Brand`. It already holds the voice card, tech stack, and design tokens, reducing the draft to a single 2-minute conversation.
2. **Draft in the Week 2 Three-Beat Shape:**
   - *The Problem:* What broke or failed prior to building.
   - *What I Did & Decided:* Architectural trade-offs and tech decisions.
   - *What Came of It:* Measurable test results, benchmarks, or verified proof.
3. **Distill to 2 Sentences:** Enforce the Voice Card (*Direct, warm, plain, zero buzzwords*) and paste the HTML card into `site/index.html`.
4. **Link Architecture Notes:** Add an entry into `<ul class="notes-list">` pointing to the repository's `README.md` or `DESIGN.md`.
5. **Mobile & Link Sanity Check:** Preview locally at 375px mobile width to guarantee zero horizontal overflow and check that all external links return HTTP 200.
6. **Commit, Push & Deploy:**
   ```bash
   cd "/home/jmomoh/FlyRank AI/portfolio"
   git add site/index.html
   git commit -m "feat(work): add Case Study #05 (LLM Metering & Billing Engine)"
   git push origin main
   ```
   Netlify automatically deploys the updated `main` branch to edge CDN in under 30 seconds.

---

## 6. Named Next Real Piece of Work: LLM Metering & Billing Engine

- **Project Identifier:** Case Study #05
- **Repository:** [https://github.com/jezreal-dev/flyrank-capstone-metering-billing](https://github.com/jezreal-dev/flyrank-capstone-metering-billing)
- **Tech Stack:** Python 3.12, FastAPI, SQLite WAL, Cryptographic HMAC-SHA256, Pytest
- **The Three-Beat Case Formulation:**
  - **The Problem:** In multi-tenant LLM billing, IEEE-754 floating-point arithmetic introduces silent revenue leakage over millions of fractional-cent token requests. Furthermore, network retry storms cause double-billing and compute loss when post-billing checks discover limit breaches after expensive GPU inference has already finished.
  - **What I Did & Decided:** Built a deterministic billing engine using 64-bit integer microcents math ($1 = 100,000,000$ microcents) with zero float drift. Enforced strict RFC-compliant `Idempotency-Key` headers storing SHA-256 request hashes and cached response bodies. Implemented pre-action quota gatekeeping with honest status codes (HTTP 429 with `Retry-After: 3600`, and HTTP 402 for delinquent accounts), AI token discount rules (50% cache discount, reasoning tokens billed as output), and zero-dependency cryptographic HMAC-SHA256 Stripe webhook synchronization.
  - **What Came of It:** Achieved 100% test pass rate across 30 pytest unit and integration tests in 2.79s. Successfully verified all 5 Evaluator Acceptance Probes with zero double-counting, proven 429/402 boundary defenses, and zero dollar infrastructure cost.

---

## 7. Concrete Calendar Reminder Set & Evidence

To ensure the portfolio maintenance habit is permanent, a recurring calendar reminder is scheduled and distributed as an active iCalendar artifact:

- **Reminder Artifact:** [`portfolio/reminders/add-next-case-study.ics`](file:///home/jmomoh/FlyRank%20AI/portfolio/reminders/add-next-case-study.ics)
- **Summary:** `Add Case Study #05 to Portfolio: LLM Usage Metering & Billing Engine`
- **Schedule:** Monthly on the 27th at 10:00 AM (Africa/Lagos, GMT+1)
- **Recurrence:** Monthly recurring event (`RRULE:FREQ=MONTHLY;BYMONTHDAY=27;COUNT=6`)
- **Alarm Trigger:** 30 minutes prior (`TRIGGER:-PT30M`, Display Notification)
- **Location:** `https://jezreal-momoh-portfolio.netlify.app`
- **Embedded Runbook:** Direct link to `HOW_TO_ADD_A_CASE_STUDY.md` and 6-step loop.

---

## 8. Preserved Build Context: Claude Project Knowledge Card

Preserved in Git and in the AI conversation context to ensure future updates require zero onboarding:

- **Voice Card:** Direct, warm, plain, zero buzzwords. Never use "synergizes", "cutting-edge", or "leveraging". Sentences are concise, active, and rooted in engineering facts.
- **Proof Statement:** *"I build backend systems and practical AI tools with Go and Python, backed by production-tested APIs, multi-agent reviewers, resilient scrapers, and live serverless integrations."*
- **Primary Stack:** Go, Python 3.12, FastAPI, SQLite WAL, PostgreSQL, LangGraph, Pydantic v2, Docker, Netlify Edge.
- **Visual System Design Tokens:**
  - Background: `--page: #faf9f6` (Warm off-white)
  - Surface: `--surface: #ffffff`
  - Typography: `--ink: #18181b` (High contrast dark gray)
  - Accent Dark: `--accent-dark: #1d4ed8`
  - Fonts: Inter, -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif
  - Touch Targets: Min 44px on mobile
- **Primary CTA:** Netlify Edge contact form (`#contact`) + 15-minute Calendly intro meeting (`https://calendly.com/laerzej/15-minute-intro-call`).
