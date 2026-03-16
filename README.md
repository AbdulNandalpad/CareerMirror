# CareerMirror 🪞

> See yourself the way the market does.

Brutally honest AI-powered LinkedIn profile analyser. No flattery. Just where you stand — and how to stay relevant.

---

## Deploy to Vercel (5 minutes)

### 1. Install Vercel CLI
```bash
npm install -g vercel
```

### 2. Deploy
```bash
cd careermirror
vercel
```
Follow the prompts. Choose "No" for existing project, accept defaults.

### 3. Add your API key
In the Vercel dashboard → your project → Settings → Environment Variables:
```
ANTHROPIC_API_KEY = sk-ant-your-key-here
```
Get your key at: https://console.anthropic.com

### 4. Redeploy
```bash
vercel --prod
```

Your app is live at `https://careermirror.vercel.app` (or similar).

---

## Deploy to Netlify (2 minutes — even easier)

1. Rename `api/analyze.js` → `netlify/functions/analyze.js`
2. Add at the top of the file: `exports.handler = async (event) => {`
3. Drag the folder to https://app.netlify.com/drop
4. Add `ANTHROPIC_API_KEY` in Site Settings → Environment Variables

---

## Local Development

```bash
npm install -g vercel
vercel dev
```
Then open http://localhost:3000

Set your API key:
```bash
export ANTHROPIC_API_KEY=sk-ant-your-key-here
```

---

## Project Structure

```
careermirror/
├── index.html        # Full frontend app
├── api/
│   └── analyze.js    # Serverless API proxy (keeps key secure)
├── vercel.json       # Routing config
└── README.md
```

---

## Features

- LinkedIn profile paste or simulated OAuth flow
- AI replacement risk score per skill
- Brutally honest career critique
- Market trend alignment score
- 3-step career roadmap
- Fully responsive, dark/light mode ready

---

Built with Claude Sonnet + Vercel Serverless Functions.
