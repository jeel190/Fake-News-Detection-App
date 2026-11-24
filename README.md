<div align="center">

# 📰 **News Detect**
### *Real-Time AI & Live Fact-Checking Web Application*

[![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-3.0.3-000000?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![Gemini AI](https://img.shields.io/badge/Gemini_AI-Fact_Check-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev/)
[![Vercel Ready](https://img.shields.io/badge/Vercel-Ready-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://vercel.com/)

*Verify any news headline, viral forward, or factual claim in seconds — powered by **Gemini AI**, **live news feeds**, **Wikidata**, and **linguistic misinformation analysis**.*

</div>

---

## ✨ Why News Detect?

Misinformation spreads fast — especially on WhatsApp forwards and social media. **News Detect** goes beyond simple keyword matching or static ML models by combining **live real-world news corroboration**, **entity-level fact verification**, **negation & typo understanding**, and **Gemini AI reasoning** to give a clear, instant verdict: **Real News** or **Fake News**.

### 🎯 Key Highlights
- **⚡ Instant Binary Verdicts** — Clear `REAL NEWS` or `FAKE NEWS` classification with a confidence meter and human-readable explanation.
- **🧠 Negation & Typo Aware** — Understands statements like *"Narendra modi is not current pm"* or misspelled queries like *"Nrendra modii is nt curent pm"* without getting tricked by keyword overlap.
- **🔢 Numerical Fact Verification** — Validates comparative claims (e.g., *"over 1000 crore"* vs *"under 10 crore"*) against live reported figures.
- **🌐 Zero-Key Public APIs + Gemini AI** — Combines free, no-auth APIs from [`public-apis`](https://github.com/public-apis/public-apis) with Google's Gemini AI.
- **📜 Search History & Quick Test Headlines** — Includes 20 curated test headlines (2024–2026) and a built-in check history log.
- **🎨 Clean Editorial UI** — Responsive newspaper-inspired interface with Devanagari display typography (`न्यूज़ डिटेक्ट में आपका स्वागत है!`).

---

## 🏗️ How Verification Works

```text
User Claim
   │
   ├──► 1. Linguistic & Hoax Heuristics (scams, clickbait, miracle cures, impossibilities)
   ├──► 2. Wikidata & Wikipedia REST Entity-Role Check (officeholders, capitals, negation)
   ├──► 3. Live News Feeds (Google News RSS, Spaceflight News API, HackerNews Algolia)
   └──► 4. Gemini AI Fact-Checker (grounded with live headlines & context)
            │
            ▼
     [ REAL NEWS / FAKE NEWS ] + Confidence % + Sources
```

---

## 🔌 APIs Integrated

| Source | Purpose | Auth Required |
| :--- | :--- | :--- |
| **Google Gemini AI** | Semantic reasoning, typo & nuance understanding | `GEMINI_API_KEY` (Free Tier) |
| **Wikidata API** (`public-apis`) | Entity resolution & current officeholder verification | No |
| **Wikipedia REST & Search** (`public-apis`) | Biographical & geographic fact-checking | No |
| **Spaceflight News API v4** (`public-apis`) | Space & science news (ISRO, NASA, SpaceX) | No |
| **HackerNews Algolia API** (`public-apis`) | Tech, AI & startup news verification | No |
| **Google News RSS** | Real-time news publisher corroboration | No |

---

## 🚀 Run Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/jeel190/Fake-News-Detection-App.git
   cd Fake-News-Detection-App
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set your Gemini API key** *(optional — works with free public APIs even without it, recommended for best accuracy)*
   ```bash
   # Create a .env file
   echo GEMINI_API_KEY=your_gemini_api_key_here > .env
   ```

4. **Start the app**
   ```bash
   python app.py
   ```
   Open **http://127.0.0.1:5000** in your browser.

---

## ☁️ Deploy to Vercel

This repository includes `vercel.json` and serverless-compatible SQLite (`/tmp/database.db`) configuration out of the box:

1. Import **`jeel190/Fake-News-Detection-App`** on [Vercel](https://vercel.com/new).
2. Add Environment Variable:
   - `GEMINI_API_KEY` = `your_gemini_api_key`
3. Click **Deploy**!

---

<div align="center">
  <sub>Built with ❤️ using Python, Flask, Gemini AI & Open Public APIs</sub>
</div>
