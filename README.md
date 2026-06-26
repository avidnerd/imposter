# Imposter

A mobile-friendly, one-phone party game. Pass a single phone around — most players see the same secret word, but one player is the imposter who doesn't know it. Discuss, vote, and find the liar.

## How to Run

No install or server required.

1. Open `index.html` in any modern mobile or desktop browser.
2. On a phone, you can tap the file from your files app, or serve it locally:

```bash
# Optional: quick local server (Python 3)
python3 -m http.server 8080
# Then visit http://localhost:8080 in your browser
```

## How to Play

1. Enter the number of players (minimum 3) and a list of custom terms.
2. Tap **Start Game** — a random term and imposter are chosen.
3. Pass the phone player by player. Each player taps **Reveal** to see their role, then **Hide** before passing it on.
4. After everyone has seen their role, discuss and vote in person — put the phone down!
5. Tap **Play Again** or **New Game** when you're ready for another round.

## Replay

- **Play Again with Same Terms** — new random word and imposter, same player count and term list.
- **New Game** — return to the setup screen.

Settings (player count and terms) are saved to `localStorage` for convenience.

## Deploy on Vercel

This is a static site — no build step required.

### Option 1: GitHub (recommended)

1. Push the repo to GitHub (includes `index.html` at the project root).
2. Go to [vercel.com/new](https://vercel.com/new) and import `avidnerd/imposter`.
3. Leave **Framework Preset** as **Other** (no build command).
4. Click **Deploy**.

Vercel will serve `index.html` at your project URL. Every push to `main` redeploys automatically.

### Option 2: Vercel CLI

```bash
npm i -g vercel
vercel
```

Follow the prompts. For production:

```bash
vercel --prod
```

### Notes

- No environment variables or backend needed.
- Works on mobile browsers — share the Vercel URL and play on one phone.
- `vercel.json` tells Vercel to deploy the root folder as static files with no build.
