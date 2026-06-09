<div align="center">

<img src="assets/banner.png" alt="banner" width="100%" />

# 🤖 isaiah-kim-bot

**An AI assistant that answers recruiter questions about Isaiah Kim — live, confident, and straight to the point.**

![HTML](https://img.shields.io/badge/HTML-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Claude API](https://img.shields.io/badge/Claude%20API-Anthropic-6B4FBB?style=for-the-badge)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)

**[Live Demo →](https://isaiah-kim-bot.vercel.app)**

</div>

<br/>

`isaiah-kim-bot` is a recruiter-facing AI chat interface that answers questions about Isaiah Kim — a Staff Frontend Engineer with 8 years of experience. Ask about his background, technical projects, comp expectations, or why he's targeting Staff roles. It's powered by Claude Sonnet via the Anthropic Messages API and deployed as a serverless function on Vercel. No database, no auth — just a polished single-page app backed by a system prompt loaded with real resume context.

## ✨ Features

- **AI-powered Q&A** — Claude Sonnet answers recruiter questions in character using a detailed system prompt covering resume, projects, and talking points
- **Suggested prompts** — Sidebar shortcuts for the most common recruiter questions (staff scope, comp expectations, cross-functional work, why he's moving)
- **Multi-turn conversation** — Full conversation history is maintained client-side and passed to the API on each request
- **Minimal serverless backend** — Single Vercel function at `/api/chat.js` proxies requests to the Anthropic API; no backend infrastructure to manage
- **Polished dark UI** — Syne + DM Mono typography, lime-green accent (`#c8f542`), animated typing indicator, and responsive mobile layout
- **Zero-config deployment** — Static HTML + one API route; deploys to Vercel in seconds with a single env var

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla HTML, CSS, JavaScript (single file) |
| AI Model | Claude Sonnet (`claude-sonnet-4-20250514`) via Anthropic Messages API |
| Backend | Vercel Serverless Function (`api/chat.js`) |
| Fonts | Google Fonts — Syne + DM Mono |
| Deployment | Vercel |

## 🚀 Getting Started

1. **Clone the repo**
   ```bash
   git clone https://github.com/kyisaiah47/isaiah-kim-bot.git
   cd isaiah-kim-bot
   ```

2. **Set your Anthropic API key**

   Create a `.env` file (or set it in Vercel):
   ```
   ANTHROPIC_API_KEY=sk-ant-...
   ```

3. **Deploy to Vercel**
   ```bash
   npm i -g vercel
   vercel --prod
   ```

   Or link an existing project:
   ```bash
   vercel link
   vercel env add ANTHROPIC_API_KEY
   vercel --prod
   ```

The app is a single `index.html` with no build step. The only server-side piece is `api/chat.js`.

## 📄 License

MIT
