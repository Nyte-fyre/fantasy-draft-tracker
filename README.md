# Fantasy Football Helper

A simple, multi-page website built to make fantasy football easier to follow — whether you're drafting for the first time or just trying to keep track of a league with a lot of moving parts. No login, no app download, just open it in a browser.

## What's here

**`index.html` — Home**
The main menu. A clean landing page with buttons into every other page.

**`draft.html` — Draft Tracker**
A live draft board for a 10-team league. Shows every available player with their draft rank (ADP) and projected points, so you can see at a glance who's a good value pick and who's already gone. Syncs directly with Sleeper to pull real picks and team names as your draft happens, and lets you build out each team's starting lineup (QB, 2 RB, 2 WR, TE, FLEX, K, DST) — every slot is a dropdown, so you can freely experiment with different lineup combinations and see how the numbers change.

**`season.html` — Season Tracker**
Once the draft's done, this page picks up where the draft tracker leaves off:
- **Standings** — computed automatically from real weekly matchup scores
- **Trade & Waiver History** — every trade, waiver claim, and free agent move in the league, newest first
- **Waiver Wire** — every player not currently on a roster, so you can see who's actually available
- **Starting Lineups** — a read-only view of each team's lineup, exactly as configured in the Draft Tracker

Smart about syncing — once a week's games are finished, that week's data is cached and never re-fetched, so repeat syncs later in the season are fast. Has a "Preview with Sample Data" button for trying the page out before the season actually starts, and a "Reset Sync Data" button if anything ever needs a clean slate.

**`week.html` — This Week**
Live head-to-head matchup cards for the current week, pulled straight from Sleeper. Shows each team's real-time score with the leader highlighted, so you can check in mid-week without digging through the season page. If the regular season hasn't started yet, it says so plainly instead of showing empty or misleading data.

**`news.html` — News Room**
- **Injury Report** — every injured player on *your league's* rosters specifically, with status (Questionable/Doubtful/Out/IR), affected body part, and which fantasy team owns them
- **Trending Adds/Drops** — the hottest waiver pickups and cuts across all of Sleeper in the last 24 hours, with a note on whether each player is already rostered in your league or still available

## Who this is for

You don't need to already know fantasy football to use this. The idea is to make the moving pieces — draft value, roster construction, starting lineups vs. bench depth, season standings, injury news — visible and easy to follow, rather than something you have to already understand going in.

## How to use it

1. Open `index.html` to get to the home menu.
2. Click into the **Draft Tracker** to follow (or plan for) your draft. Hit **Sync from Sleeper** to pull in real picks, or paste a different league's link under "League" to load a different draft entirely.
3. Pick your own team from the **Viewing as** dropdown — everyone in the league can do this independently, and it only affects what you personally see.
4. Once the draft wraps up, use **Season Tracker** for standings/trades, **This Week** for live scores, and **News Room** for injuries and waiver activity — all synced from Sleeper with a click.

Every content page has a row of nav pills at the top (Home / Draft / Season / This Week / News) so you can jump anywhere without backtracking through other pages.

## How the pages share data

All five pages live on the same site, so they share data automatically through the browser's local storage — no extra setup required. Draft picks and lineup choices made in the Draft Tracker show up automatically on the Season Tracker. Everyone's picks, team names, and preferences are saved locally in their own browser, so no two people will ever overwrite each other's view.

## Hosting

This is a static site — no server or backend needed. It's built to run on **GitHub Pages**: upload all five HTML files to a repository, with `index.html` as the entry point (this is the home page, not the draft tracker), and turn on Pages in the repo settings.

## What's next

- Real news headlines (beyond injury status and trending players) would need a separate feed and haven't been added yet.
- Everything here relies on Sleeper's public API for live data, so features are limited to what Sleeper exposes (no play-by-play or official real-time stats).
