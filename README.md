# Fantasy Football Draft & Season Tracker

A simple two-page website built to make fantasy football easier to follow — whether you're drafting for the first time or just trying to keep track of a league with a lot of moving parts. No login, no app download, just open it in a browser.

## What's here

**`index.html` — Draft Tracker**
A live draft board for a 10-team league. Shows every available player with their draft rank (ADP) and projected points, so you can see at a glance who's a good value pick and who's already gone. Syncs directly with Sleeper to pull real picks and team names as your draft happens, and lets you build out each team's starting lineup (QB, RB, WR, TE, FLEX, K, DST) to see how a roster is shaping up.

**`season.html` — Season Tracker**
Once the draft's done, this page picks up where the draft tracker leaves off — standings, weekly scores, and a look at each team's starting lineup, exactly as it was set up on draft day. It automatically shares data with the draft tracker, so nothing needs to be re-entered.

## Who this is for

You don't need to already know fantasy football to use this. The idea is to make the moving pieces — draft value, roster construction, starting lineups vs. bench depth — visible and easy to follow, rather than something you have to already understand going in.

## How to use it

1. Open `index.html` in any browser to see the draft board.
2. Click **Sync from Sleeper** to pull in real picks from a live draft (or paste in a different league's link under "League" to load a different one).
3. Pick your own team from the **Viewing as** dropdown — everyone in the league can do this independently.
4. Once the draft wraps up, click through to the **Season Tracker** to follow standings and weekly scores.

## Hosting

This is a static site — no server or backend needed. It's built to run on **GitHub Pages**: upload both files to a repository (with `index.html` as the entry point) and turn on Pages in the repo settings. Everyone's picks, team names, and preferences are saved locally in their own browser, so no two people will ever overwrite each other's view.
