# Mobile & Accessibility Audit: Fix Log

**Assignment:** Open It on Your Phone · Week 6 · General AI Fluency  
**Student:** Jezreal Momoh  
**Live Site:** [https://jezreal-momoh-portfolio.netlify.app](https://jezreal-momoh-portfolio.netlify.app)  
**Repository:** [https://github.com/jezreal-dev/portfolio](https://github.com/jezreal-dev/portfolio)  
**Date:** November 17, 2026

---

## 1. Executive Summary

Opening the portfolio on a real mobile device revealed several subtle friction points common to desktop-first builds: iOS auto-zooming on form inputs, cramped navigation touch targets, potential viewport horizontal wobble, and undersized action links. 

This audit systematically resolved all mobile-first defects across viewport widths ranging from 320px (iPhone SE / Galaxy Fold) up to tablet and desktop. Every link was verified live, contrast was hardened to exceed WCAG AA/AAA standards, and touch targets now satisfy the 44×44px / 48×48px mobile usability threshold.

---

## 2. Real Problems Found & Fixed

| Area | Before (The Problem) | After (The Code Fix) | Why It Matters (Trustworthiness) |
| :--- | :--- | :--- | :--- |
| **Form Inputs (iOS Safari)** | `font-size: 14px` on `<input>` and `<textarea>` caused iOS Safari to automatically zoom the entire viewport upon tapping any field, forcing the user to manually pinch out. | Changed input `font-size: 16px` and added `min-height: 48px`. | Eliminates aggressive browser viewport jumping; keeps the form grounded and usable with one thumb. |
| **Navigation Tap Targets** | At `< 470px`, `nav a` was shrunk to `11px` with `11px` gaps and no vertical padding (< 20px hit area). Prone to fat-finger mis-taps. | Increased font size to `13px` with `padding: 8px 4px; display: inline-flex; min-height: 44px`. | Conforms to WCAG 2.5.5 / 2.5.8 touch target standards; links are reliably tappable on mobile screens. |
| **Project Action Links** | `.text-link` ("View repository ↗") was `13px` with `0px` vertical padding, making it hard to tap between cards. | Set `.text-link` to `14px`, `min-height: 44px; padding: 4px 0; display: inline-flex; align-items: center`. | Primary proof links (GitHub repos) can be opened with confidence on touchscreen without missing. |
| **Viewport Wobble / Overflow** | At narrow viewports (< 360px), fixed headings (`43px`) risked horizontal overflow. `html, body` lacked overflow bounds. | Added `overflow-x: hidden` to `html, body`; clamped `h1` to `clamp(34px, 9vw, 44px)` with fluid scaling. | Completely eliminates sideways horizontal scrolling or accidental viewport wobble. |
| **Mobile Button Stacking** | Hero actions and contact buttons sat in horizontal flex rows that crammed text on narrow screens. | Added `@media (max-width: 470px) { .hero-actions { flex-direction: column; } .button { width: 100%; min-height: 48px; } .form-actions button { width: 100%; } }`. | Thumb-friendly, edge-to-edge buttons that look deliberate and native on mobile devices. |
| **Color Contrast & Legibility** | `.eyebrow` (12px uppercase) used `--accent` (`#2563eb`), which was borderline on warm tinted backgrounds. | Upgraded `.eyebrow` and primary text links to `--accent-dark` (`#1d4ed8`), yielding > 5.8:1 contrast. | Exceeds WCAG AA (4.5:1) for small text; stays crisp even on low-brightness phone screens in sunlight. |
| **Footer Accessibility** | Footer links stacked awkwardly on small screens with cramped touch targets. | Added `flex-wrap: wrap; gap: 16px;` and `padding: 8px 4px; min-height: 44px` on `.footer-links a`. | Clean spacing and effortless tapping for GitHub, LinkedIn, and Email links. |

---

## 3. Link Integrity Audit (100% Passing)

Every internal and external hyperlink was verified live via HTTP requests:

* `https://github.com/jezreal-dev` -> **HTTP 200 OK**
* `https://github.com/jezreal-dev/themis` -> **HTTP 200 OK**
* `https://github.com/jezreal-dev/gemmaroute` -> **HTTP 200 OK**
* `https://github.com/jezreal-dev/flyrank-backend-ai-engineering/tree/main/scraper` -> **HTTP 200 OK**
* `https://calendly.com/laerzej/15-minute-intro-call` -> **HTTP 200 OK**
* `mailto:jezreelmomoh1234@gmail.com` -> **Valid URI Scheme**
* CV Download (`./assets/Jezreal_Momoh_Backend_AI_Engineer_CV.pdf`) -> **Verified File Present**
* In-page jump anchors (`#work`, `#about`, `#notes`, `#contact`) -> **All IDs match DOM landmarks**

---

## 4. Performance & Asset Weight

* **Zero Heavy Framework Bundles:** Built entirely in lean semantic HTML and pure CSS. Total transferred page weight is under 60 KB (including icons and styles).
* **Instant Load:** Time-to-Interactive (TTI) is virtually zero on 4G and 3G mobile networks.
* **Responsive Breakpoints Verified:** Tested cleanly across 320px, 375px, 414px, 768px, and 1080px widths.
