# Make It Do Something — Portfolio Dynamic Feature & Explainer

**Assignment:** Make It Do Something · Week 6 · General AI Fluency  
**Student:** Jezreal Momoh  
**Live Site:** [https://jezreal-momoh-portfolio.netlify.app](https://jezreal-momoh-portfolio.netlify.app)  
**Feature:** Fully integrated Netlify Contact Form (`#contact`)  
**Repository:** [https://github.com/jezreal-dev/portfolio](https://github.com/jezreal-dev/portfolio)

---

## Part 1: The Plain-Words Explainer

### 1. What a Backend Is
Think of a static webpage like a printed poster hanging on a shop window. You can read the text, admire the design, and see a phone number or address, but touching the poster doesn't change anything in the shop. That is the **frontend**: everything that runs directly in the user's browser (HTML structure, CSS styling, and layout).

A **backend** is the kitchen behind the shop counter. It is the server-side computer program and database that does the real work out of sight. When you hand an order across the counter, the kitchen checks if the order is valid, stores it in a ledger, talks to third-party suppliers, and delivers the result. In web architecture, a backend receives requests sent across the internet, processes the data according to business rules, protects secrets, and triggers actions in the real world (like sending an email or writing to a database). Without a backend, clicking a button on a website is just tapping glass.

---

### 2. What This Feature Does
This feature turns the static contact section of my personal portfolio into a **live, interactive communication tool**. 

Instead of forcing visitors to manually open their external email app or copy a mailto link, any recruiter, engineering peer, or client can type their name, email address, and inquiry directly into the form and click **Send message**. 

The feature includes:
* **Client-side validation:** Enforces valid email formats and non-empty messages before anything is sent.
* **Anti-spam honeypot:** A hidden field (`bot-field`) invisible to human visitors that catches automated web scrapers and bots.
* **Progressive enhancement:** Uses asynchronous JavaScript (`fetch`) to provide instant inline visual feedback without reloading the page, while gracefully falling back to standard HTTP POST if JavaScript is disabled.
* **Email notification dispatch:** Netlify immediately captures the submission and sends an alert directly to my inbox (`jezreelmomoh1234@gmail.com`).

---

### 3. How the Data Flows (Step-by-Step)

```
[ Visitor Browser ] 
        │
   (1) User types Name, Email, Message
        │
   (2) Clicks "Send message" -> JavaScript intercepts and serializes form
        │
   (3) Asynchronous HTTP POST (URL-encoded) to Netlify Edge Server (/)
        ▼
[ Netlify Serverless Backend ]
        │
   (4) Inspects form payload & verifies honeypot (bot-field) is blank
   (5) Stores submission in Netlify Forms database
   (6) Dispatches notification email via transactional mail server
        │
        ├──────────────────────────────┐
        ▼                              ▼
[ Jezreal's Inbox ]          [ Visitor Browser ]
(7) Email received:          (8) Receives HTTP 200 OK
    "New submission from          Inline UI updates:
     Alex Smith via contact"      "Thank you! Your message was sent."
```

1. **Input & Validation (Browser):** The user enters their Name, Email, and Message into the form at `#contact`. The browser validates the input types.
2. **Serialization (Client):** When the user clicks "Send message", JavaScript prevents the default page reload, disables the submit button to prevent double-clicks, and serializes the inputs into a URL-encoded payload along with the hidden Netlify form identifiers (`form-name=contact`).
3. **Transport (HTTP POST):** The browser sends an HTTP `POST` request over TLS directly to Netlify's hosting edge network at `/`.
4. **Backend Processing & Spam Defense (Netlify):** Netlify’s serverless form handler detects the incoming post, checks the `bot-field` honeypot to ensure no automated spambot filled it out, and logs the verified submission into the backend dashboard.
5. **Real-World Action (Notification):** Netlify's backend triggers an automated email dispatch that delivers the message directly to `jezreelmomoh1234@gmail.com`.
6. **Confirmation (Client Feedback):** Netlify returns an HTTP `200 OK` response. The client script catches this response, clears the form inputs, and renders a green confirmation notification: *"Thank you! Your message was sent successfully."*

---

## Part 2: Evidence & Verification Guide

1. **Live Site Verification:**
   * Visit [https://jezreal-momoh-portfolio.netlify.app#contact](https://jezreal-momoh-portfolio.netlify.app#contact).
   * Submit a message with your name, email, and test message.
   * Observe the instant confirmation state.
2. **Dashboard / Inbox Proof:**
   * Check the incoming notification in `jezreelmomoh1234@gmail.com` or the Netlify dashboard under **Site configuration > Forms**.
