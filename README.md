# 🎭 Mafia Storyteller

A single-page web app that helps the storyteller (narrator) run a game of Mafia with cards. No backend, no build step.

## What it does
- Enter player names and choose how many Mafia / Doctor / Detective (the rest become Villagers)
- Randomly assigns roles (the storyteller sees them; hand out physical cards or tell players privately)
- Guides each night with a read-aloud script: Mafia → Doctor → Detective
- Resolves dawn (kill, save, or no attack), then runs the day vote
- Tracks who is alive and detects the winner automatically
- Keeps a game log, and saves progress in the browser so a refresh won't lose the game

## Run it
Open `index.html` in any browser.

## Publish on GitHub Pages
1. Create a new repository on GitHub (e.g. `mafia-storyteller`).
2. Upload `index.html` and `README.md` (Add file → Upload files), then commit.
3. Go to **Settings → Pages**, set **Source** to "Deploy from a branch", choose `main` and `/ (root)`, and save.
4. After a minute your app is live at `https://<your-username>.github.io/mafia-storyteller/`.

## Ideas for next steps
- More roles (Godfather, Bodyguard, Jester)
- Timer for discussion and voting
- Multiple languages (e.g. Arabic with RTL support)
- Install as a phone app (PWA)
