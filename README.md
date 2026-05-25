# Total Flight Management Inc. — Website

VATSIM Virtual Airline · Part 135 · KTEB · Certificate JDJZ2030

## Stack
- Single-file HTML/CSS/JS frontend (`index.html`)
- Netlify serverless function proxying the Anthropic API (`netlify/functions/claude-proxy.js`)
- Auto-deploy via GitHub → Netlify

## Deploy

1. Push this repo to GitHub
2. Connect to Netlify (Import project → GitHub)
3. Build settings are handled by `netlify.toml` — no changes needed
4. Add environment variable in Netlify dashboard:
   - **Key:** `ANTHROPIC_API_KEY`
   - **Value:** your Anthropic API key
5. Deploy — done

## Environment Variables

| Variable | Description |
|---|---|
| `ANTHROPIC_API_KEY` | Anthropic API key for the charter quote engine |

## Features
- Public site: Home, Fleet, Charter Quote (AI-powered), Dispatch Board, About
- Crew Portal: VATSIM login, logbook, roster, notifications
- Demo login: any VATSIM CID + password `tfm2026`

## Local Dev
```bash
npm install -g netlify-cli
netlify dev
```
Then open `http://localhost:8888`
