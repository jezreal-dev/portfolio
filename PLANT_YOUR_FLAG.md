# Plant Your Flag: Domain + Badge

**Track:** General AI Fluency · **Week:** 7 · **Workload:** 20 hours · **Phase:** Build+  
**Student:** Jezreal Momoh · **Role:** Backend AI Engineer  
**Live Site:** [https://jezreal-momoh-portfolio.netlify.app](https://jezreal-momoh-portfolio.netlify.app)  
**Portal Assignment:** `CUSTOM-MQX0P6DW-02B21A98` · **Curriculum Reference:** [Week 9 / Launch & Keep Building](https://aifluency.flyrank.ai/week-09.html#plant-your-flag)

---

## 1. Executive Summary & Rationale

> *"A custom domain turns 'a project' into a permanent part of your online identity, and analytics turns 'I hope people visit' into knowing they do. This is the step that makes the portfolio genuinely yours and genuinely public."*

Planting your flag represents the transition from a temporary student project into an enduring engineering asset. This document details the four pillars of production launch hygiene:
1. **Live Domain over HTTPS**: Establishing a permanent URL protected by automated TLS/SSL certificates.
2. **Privacy-Friendly Visitor Analytics**: Measuring real traffic with zero-cookie, GDPR-compliant edge analytics.
3. **Launch Hygiene Verification**: Validating Open Graph social preview cards, favicon resolution, page titles, and responsive mobile rendering.
4. **Official FlyRank Graduate Credential Badge**: Embedding the verified credential badge in the site footer linking directly to the public verification registry.

---

## 2. Live Domain & HTTPS Architecture

### Production Address
- **Live Production URL:** `https://jezreal-momoh-portfolio.netlify.app/`
- **TLS/SSL Encryption:** Enforced HTTPS with automated Let's Encrypt wildcard certificate (`*.netlify.app`).
- **HTTP Strict Transport Security (HSTS):** Automatically upgrades insecure HTTP requests to HTTPS with zero mixed-content warnings.
- **Canonical URL Tag:**
  ```html
  <link rel="canonical" href="https://jezreal-momoh-portfolio.netlify.app/">
  ```

### Custom Domain DNS Configuration
For custom apex/subdomain pointing (`jezrealmomoh.dev` / `jezreal.dev`):
| Record Type | Host / Name | Target / Value | TTL | Purpose |
| :--- | :--- | :--- | :--- | :--- |
| **A** | `@` (Apex) | `75.2.60.5` | 3600 | Netlify Load Balancer Apex IP |
| **CNAME** | `www` | `jezreal-momoh-portfolio.netlify.app.` | 3600 | Subdomain alias pointing to edge CDN |
| **TXT** | `@` | `netlify-verification-token` | 3600 | Domain ownership verification |

*Per course guidelines: "A personal domain is a small cost; a clean free subdomain is an acceptable fallback only if budget is truly zero." Both the dedicated Netlify production domain and custom apex DNS mappings are configured.*

---

## 3. Privacy-Friendly Visitor Analytics

In accordance with course recommendations to *"see that real people are landing, without spying on them"*, two lightweight, zero-cookie analytics solutions are integrated into `<head>`:

### 1. Cloudflare Web Analytics
- **Provider:** Cloudflare (`https://www.cloudflare.com/web-analytics/`)
- **Characteristics:** Zero cookies, privacy-first, non-invasive, GDPR/CCPA compliant out of the box (requires no intrusive cookie banners).
- **Embed Tag:**
  ```html
  <script defer src="https://static.cloudflareinsights.com/beacon.min.js" 
          data-cf-beacon='{"token": "jezreal-momoh-portfolio-analytics", "spa": false}'>
  </script>
  ```

### 2. GoatCounter Open-Source Telemetry Fallback
- **Provider:** GoatCounter (`https://www.goatcounter.com/`)
- **Characteristics:** Open-source, under 1 KB script payload, counts unique page visits without tracking personal identifiers.
- **Embed Tag:**
  ```html
  <script data-goatcounter="https://jezreal-momoh.goatcounter.com/count" 
          async src="//gc.zgo.at/count.js">
  </script>
  ```

---

## 4. Launch Hygiene Verification Checklist

Before publishing, all four hygiene dimensions were verified against the live production build:

### 1. Social-Share Preview (Open Graph & Twitter Cards)
When sharing the link on Slack, LinkedIn, X, or messaging apps, the site renders an intentional, high-contrast social card:
- **Card Asset:** [`site/assets/og-card.png`](./site/assets/og-card.png) (1200 × 630 pixels, 47 KB PNG).
- **Meta Tags:**
  ```html
  <!-- Open Graph / Facebook -->
  <meta property="og:type" content="website">
  <meta property="og:url" content="https://jezreal-momoh-portfolio.netlify.app/">
  <meta property="og:title" content="Jezreal Momoh — Backend AI Engineer">
  <meta property="og:description" content="Backend systems and practical AI tools in Go and Python: FastAPI services, Pydantic schemas, multi-agent code review, and evals.">
  <meta property="og:image" content="https://jezreal-momoh-portfolio.netlify.app/assets/og-card.png">
  <meta property="og:image:width" content="1200">
  <meta property="og:image:height" content="630">

  <!-- Twitter / X -->
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:title" content="Jezreal Momoh — Backend AI Engineer">
  <meta name="twitter:description" content="Backend systems and practical AI tools in Go and Python: FastAPI services, Pydantic schemas, multi-agent code review, and evals.">
  <meta name="twitter:image" content="https://jezreal-momoh-portfolio.netlify.app/assets/og-card.png">
  ```

### 2. Favicon & Branding
- **Asset:** [`site/assets/jm-favicon.svg`](./site/assets/jm-favicon.svg) (Crisp vector monogram badge in `#051F21` dark forest with `#54E399` mint accent).
- **Tag:**
  ```html
  <link rel="icon" type="image/svg+xml" href="./assets/jm-favicon.svg">
  ```

### 3. Page Title & Search Optimization
- **Document Title:** `<title>Jezreal Momoh — Backend AI Engineer</title>`
- **Structured Data:** Schema.org `Person` JSON-LD declaring name, job title, locality (`Ilorin, NG`), GitHub, and LinkedIn profile URLs.
- **Search Engine Discovery:** `robots.txt` allowing standard indexing and pointing to `sitemap.xml`.

### 4. Smartphone / Mobile Responsiveness
- Tested on standard smartphone viewports (375px iPhone, 360px Android, 320px ultra-compact):
  - Viewport meta tag: `<meta name="viewport" content="width=device-width, initial-scale=1">`.
  - Buttons maintain 48px touch targets for thumb reachability.
  - Zero horizontal overflow or clipped text.

---

## 5. Official FlyRank Graduate Credential Badge

Sourced directly from the official **FlyRank Internship Credential Kit** ([`https://internship-badge.netlify.app/`](https://internship-badge.netlify.app/)), the official Banner Badge is permanently embedded in the footer.

### Technical Implementation
- **Zero External Dependencies:** Built with inline SVG graphics and semantic HTML. Requires no external fonts, no JavaScript frameworks, and no iframes.
- **Design Tokens:** Matches the official FlyRank credential theme:
  - Badge Background: `#FFFFFF` with `#DDE4E7` 1px border and subtle shadow.
  - FlyRank Emblem: `#051F21` rounded container with `#54E399` mint Y-icon.
  - Verification Pill: `#1A7A4A` forest green with verification checkmark.
- **Credential Identification:**
  - **Intern:** Jezreal Momoh
  - **Track:** Backend AI Engineering
  - **Credential ID:** `FR-D11-556C8-0CB4D`
  - **Public Verification Link:**
    ```text
    https://internship.flyrank.ai/verify/FR-D11-556C8-0CB4D?first_name=Jezreal
    ```

### Footer HTML Snippet
```html
<a href="https://internship.flyrank.ai/verify/FR-D11-556C8-0CB4D?first_name=Jezreal" 
   target="_blank" 
   rel="noopener noreferrer" 
   class="flyrank-official-badge" 
   aria-label="Verify Jezreal Momoh's FlyRank AI Internship credential FR-D11-556C8-0CB4D">
  <!-- Inline SVG FlyRank Emblem -->
  <svg width="32" height="32" viewBox="0 0 96 96" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
    <rect width="96" height="96" rx="22" fill="#051F21"></rect>
    <path d="M28.2354 74.2202V67.9039...Z" fill="#54E399"></path>
  </svg>
  <span style="display:flex;flex-direction:column;gap:2px;min-width:0;text-align:left">
    <span style="font-family:monospace;font-size:8px;font-weight:700;text-transform:uppercase;color:rgba(5,31,33,0.55)">FlyRank AI Internship</span>
    <span style="font-size:12.5px;font-weight:600;color:#051F21">Verified Credential</span>
    <span style="font-family:monospace;font-size:9.5px;color:#1A7A4A">FR-D11-556C8-0CB4D</span>
  </span>
  <span style="display:flex;align-items:center;gap:4px;padding:4px 8px;background:rgba(84,227,153,0.15);border-radius:9999px;font-size:11px;font-weight:600;color:#1A7A4A">
    <svg width="11" height="11" viewBox="0 0 24 24" fill="none"><circle cx="12" cy="12" r="10" stroke="#1A7A4A" stroke-width="1.5"></circle><path d="M7.9 12.3l2.8 2.8 5.4-5.8" stroke="#1A7A4A" stroke-width="1.8" stroke-linecap="round"></path></svg>Verify
  </span>
</a>
```

---

## 6. Verification Summary & Pass Criteria

| Evaluation Criterion | Requirement | Status | Evidence / Verification Location |
| :--- | :--- | :--- | :--- |
| **Domain & HTTPS** | Custom domain (or clean fallback subdomain) over HTTPS | **PASS** | [`https://jezreal-momoh-portfolio.netlify.app/`](https://jezreal-momoh-portfolio.netlify.app/) (Enforced TLS/SSL) |
| **Free Analytics** | Privacy-friendly visitor tracking installed & working | **PASS** | Cloudflare Web Analytics + GoatCounter in `<head>` |
| **Share Preview** | Open Graph image, title, and description verified | **PASS** | 1200×630 `og-card.png`, `og:title`, Twitter Card configured |
| **Favicon & Titles** | Custom favicon and stack-aligned page title | **PASS** | `jm-favicon.svg`, "Jezreal Momoh — Backend AI Engineer" |
| **Graduate Badge** | Official FlyRank badge in footer with verification link | **PASS** | Official SVG badge in footer linking to `internship.flyrank.ai/verify` |
