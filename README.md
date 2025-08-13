# Debug Dash — An Agentic AI Demo (ChatGPT-built)

> **What is this?**  
> A tiny, production-ready web game intentionally kept simple to showcase an **agentic AI workflow** with ChatGPT.  
> The “agent” (ChatGPT) planned the feature set, wrote the code, configured GitHub Pages, and iterated on user feedback—end to end.

---

## Personal Note
> I was just fascinated by agentic AI and was testing its limits in a good way.

---

## Prompt Inputs (from the conversation)

**First prompt (layman spec):**
```
create and deploy a snakes game for me. Instead of dots, put error codes and instead of snake, put a programmer with laptop's image.

Deploy such that i can directly go on that site
```

**Second prompt (improvisation request):**
```
Improvisation on previous task

1. Let the user pass from walls on 4 sides and come out of the other side like it is allowed in snakes game.
2. Instead of the current programmer with laptop, make it just this emoji -> 👨🏻‍💻
3. Intially ask for a name and show it on top. 
4. Show play,pause, reset buttons
4. give it a name and tagline like this 
Debug Dash – race to “eat” errors before they eat you.

5. Make it mobile responsive and like arrow keys, let touch gestures on phone also work.
6. When lost, instead of game over, if the 404 dot remains for example, say something like "system crashed because of a 404. Try Again". Keep the font and structure like Game Over only but different message.
7. Make the code modular and JS integrated. Improve UI/UX and animations
```

---

## Why an Agent Demo (not an ML model)?
Agentic AI isn’t only about training models—it’s about **autonomously executing multi-step tasks**: planning → coding → testing → deploying → improving.  
This repo shows how a generalist agent (ChatGPT) can:
- Convert a **natural-language spec** into runnable software
- **Self-correct** via tight build–test loops
- Handle **product changes** (UX tweaks, mobile margins, gestures, copy, error states)
- **Ship** to a public URL with GitHub Pages

---

## What the Agent Delivered
- A playable, responsive game with:
  - **Wrap-around world** (toroidal edges)
  - **👨🏻‍💻 emoji “snake”** and **HTTP error codes** as food
  - **Name overlay**, **scoreboard**, **Play / Pause / Reset** controls
  - **Touch gestures** on mobile + keyboard on desktop
  - Crash message like: **“System crashed because of a 404. Try again!”**
  - Improved **mobile margins & tap targets** (safe-area aware)

---

## Anatomy of the Agentic Workflow
1. **Goal Intake** — Human shares plain-English requirements.  
2. **Plan & Scaffold** — Agent generates HTML/JS/CSS, canvas grid, controls, UI.  
3. **Execute & Test** — Agent runs locally, fixes logic (first-tick move, wrap-around), polishes UI.  
4. **Deploy** — Agent configures GitHub Pages (branch: `main`, root) and verifies URL.  
5. **Iterate** — Human requests changes; agent applies diffs and updates docs.

> The point: **No backend, no frameworks, no build system**—just a clean artifact proving an agent can deliver software from a conversational brief.

---

## Repo Structure
```
programmer-snake-game/
├─ index.html   # Self-contained UI + game logic (modularized functions)
└─ README.md    # This document (agentic AI demo framing + prompts)
```

> Next step (optional, to show deeper agent refactors):
> - Split into modules (`engine.js`, `controls.js`, `ui.js`, `main.js`) and import via `<script type="module">`.

---

## Run & Deploy

### Local
```bash
# any static server works
python3 -m http.server 8000
# open http://localhost:8000
```

### GitHub Pages
- Settings → Pages → Source: **main** / root → **Save**
- Live at: `https://<your-username>.github.io/programmer-snake-game/`

---

## Demo Script (Reproduce the Agent Flow)
Use this prompt with ChatGPT (or your preferred agent runner):

> *“You are a software agent. Build a snake-like web game named **Debug Dash** where the snake is the 👨🏻‍💻 emoji and food are HTTP error codes. Support wrap-around edges, name entry overlay, scoreboard, Play/Pause/Reset, mobile swipe gestures, and a crash message like ‘System crashed because of a 404. Try again!’. Make it responsive with bigger tap targets and safe-area margins. Ship a single `index.html` suitable for GitHub Pages. Document the agentic workflow in a README and credit ChatGPT Agent.”*

---

## Agent Credits & Attribution
- **Core implementation, UX, and deploy orchestration:** *ChatGPT Agent (OpenAI)*
- **Human-in-the-loop:** Feature requests, acceptance testing, and final framing

---

## License
MIT — attribution appreciated.
