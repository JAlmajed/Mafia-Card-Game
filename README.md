# 🎭 Mafia Storyteller

A single-page web app that helps the storyteller (narrator) run a game of Mafia with cards. No backend, no build step: just open `index.html`.

## Features
- **Saved player names**: add names once (comma-separated works too), tick the ones playing tonight, untick or delete the rest. Names and your selection are remembered on the device.
- **Roles with counts**: Mafia, Doctor, Detective, Girlfriend, Serial Killer. Villagers fill the remaining seats.
- **Random or Manual dealing**: let the app deal roles randomly, or switch to Manual and choose each player's role from a dropdown.
- **Custom roles**: create your own with a name, emoji, team (Town / Mafia / Solo killer / Neutral) and night ability (none, protect, investigate, block, kill). Saved for next time.
- **Guided night**: read-aloud scripts, tells you exactly whom to wake, and shows the Detective's answer.
- **Discussion and voting timers**: set the minutes in setup; start, pause, reset, ±30s, with a beep and vibration at zero. The timer survives a page refresh.
- **← Back button**: undo the last step (a night choice, the dawn reveal, a vote, or going back to setup) if you tap by mistake.
- Alive tracking, win detection, a game log, a private night report, and a "Hide roles" button.

## Role rules used
| Role | Team | Night action |
|---|---|---|
| Mafia | Mafia | Wake together and pick one player to kill |
| Doctor | Town | Protects one player every night (can't skip). Can protect themselves, but can't protect the same player two nights in a row (they can again on the night after) |
| Detective | Town | Learns whether a player is Mafia: thumbs up = Mafia, thumbs down = not Mafia (Serial Killer shows as *not* Mafia) |
| Girlfriend | Town | Spends the night with a player and blocks their ability. If she blocks a Mafia member, the Mafia kill fails |
| Serial Killer | Solo | Kills one player each night on their own. Can't target themselves |

Night order: Girlfriend → Mafia → Serial Killer → Doctor → Detective.

**Winning:** Town wins when all Mafia and Serial Killers are gone. Mafia wins when they equal or outnumber everyone else and no Serial Killer is alive. The Serial Killer wins when no Mafia are left and only 2 players remain. If everyone dies, it's a draw.

## Run it
Open `index.html` in any browser.

## Publish on GitHub Pages
1. In the repo, go to **Settings → Pages**.
2. Set **Source** to "Deploy from a branch", choose `main` and `/ (root)`, and save.
3. After a minute your app is live at `https://<your-username>.github.io/<repo-name>/`.
