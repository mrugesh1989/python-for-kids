# 🐍 Python for Kids

An interactive, single-file web app that teaches kids aged 5–15 real Python — from
"what is a program?" to writing their first chatbot. Kids write and run **actual
Python** in the browser (via [Skulpt](https://skulpt.org)), guided by Sage the Snake.

## Features
- **Snake Trail map** — 12 lessons rendered as a winding python; first 3 free, rest Pro
- **Lesson 1** — tap-to-program maze game (sequencing, no typing needed for young kids)
- **Lessons 2–12** — real Python editor with Run, auto-checking tasks, hints, and bug hunts
- **Playground** — free-form Python sandbox with starter snippets
- **Ask Sage** — AI tutor (Anthropic API inside Claude artifacts; rule-based hint engine
  everywhere else, so the app never breaks on static hosting)
- **XP, confetti, quizzes, age tracks** (Explorer 5–8 / Builder 9–12 / Hacker 13–15)
- Zero build step, zero dependencies to install — one `index.html`

## Deploy to GitHub Pages (5 commands)
```bash
# 1. Create a new repo named python-for-kids on github.com, then:
git init
git add index.html README.md
git commit -m "Python for Kids v1"
git branch -M main
git remote add origin https://github.com/<YOUR_USERNAME>/python-for-kids.git
git push -u origin main
```
Then on GitHub: **Settings → Pages → Source: Deploy from a branch → main / (root) → Save.**
Your app goes live at `https://<YOUR_USERNAME>.github.io/python-for-kids/` in ~1 minute.

## Honest limitations (read before monetizing)
1. **The paywall is a demo.** GitHub Pages is static hosting — any client-side gate can be
   bypassed via dev tools. Real subscriptions require Stripe + a backend (or serverless
   functions on Vercel/Cloudflare) to verify entitlements server-side.
2. **The AI tutor** uses the Anthropic API only when run inside a Claude artifact. On
   GitHub Pages it automatically falls back to the built-in hint engine. To make live AI
   work publicly, proxy requests through a small backend that holds your API key —
   **never** ship an API key in client-side code.
3. **COPPA / privacy:** the app currently stores nothing and collects nothing, which is
   the safest posture for a kids' product. If you ever add accounts or analytics for
   under-13 users, COPPA compliance becomes your problem. Talk to a lawyer first.
4. **Employer compliance:** monetizing this while employed at a bank requires
   outside-business-activity pre-clearance. Get it in writing before charging a dollar.

## License
MIT — do whatever you like, attribution appreciated.
