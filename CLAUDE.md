# Quasar + Pratus Holiday Food Drive 2026: Project Brief

This repo hosts the site for the company-wide holiday food drive at Quasar Consulting Group and Pratus Group. Read this whole file before making changes.

## Who this is for

- Owner: Nathaniel (Nate), Marketing Coordinator at Quasar. He's a designer and marketer, not a developer. Explain steps in plain language, one at a time, and don't assume Git or coding knowledge.
- Audience: 334 employees across six offices. Most will open the site from a button on The Pulse (Quasar's internal SharePoint hub) or a Teams post, often on a phone.

## The goal and why the site exists

Last year's drive missed its goals mainly because it was confusing:
- Scoring used meals, with contradictory conversions ($1 = 2 meals vs $2 = 1 meal) and extra goal adjustments for some offices.
- Updates went out by email and got lost. There was no single place to see standings or find donation links.
- Each office used a different local food bank, and some (North Bay) had no online tracker, so totals were hard to collect.

This year's theme is **one link, one number, one place**. Every design or content decision should make the drive simpler to understand and easier to give to.

## The new format: HQ vs. everyone else

The competition has changed from six offices competing against each other to **two teams**:

| Team | Offices | Headcount |
|---|---|---|
| Team HQ | Woodbridge | 260 |
| The challengers (working name: Team Coast to Coast) | Sterling Road (Pratus) 30, Vancouver 20, Ottawa 15, North Bay 6, Timmins 3 | 74 |
| **Company total** | | **334** |

HQ is about 78% of the company, so total dollars can never be the main score. The scoring has to be per person so the challengers have a real shot. Lean into the **underdog story**: a scrappy cross-country team taking on headquarters.

### Scoring (current direction, some details still being decided)

- Every person counts the same: each team's goal = headcount × $20 per person ($10 fallback still possible). No adjustments.
  - Team HQ goal: $5,200. Challengers goal: $1,480. Company goal: $6,680.
- **Main score: % of goal.** Whichever team gets furthest past its goal wins.
- **Participation:** the share of each team's people who donated any amount. This is the big equalizer and should be shown prominently.
- **Ideas still under discussion** (don't build unless Nate confirms):
  - A weekly "series," where each week is a game with its own winner and the overall winner takes the most weeks.
  - A shared company milestone (for example, a leadership match unlocked when the whole company hits its goal), so everyone has something to win together.
  - A friendly sector or department mini-leaderboard inside Woodbridge.

### Prizes (still being confirmed)

- If the challengers win: pizza or treats sent to every regional office, possibly an HQ leadership dare on a company-wide call.
- If HQ wins: office party plus the travelling Pulse Cup.

## Where donations go

- Moving from local food banks to a **Canada-wide food bank partner**, likely Food Banks Canada (to be confirmed).
- The partner can set up **separate team pages**, one for each team, so totals are tracked on their platform. Nate copies the totals into the site each Friday.
- Messaging: "supporting food banks in every community where we live and work." Don't say donations go to one specific local food bank.
- Real donation links are still to come. Use clear placeholders until then.

## Timeline

- Kickoff: Monday, November 23, 2026
- Weekly Friday updates: Nov 27, Dec 4, Dec 11, Dec 18 (last before holiday closure)
- Donations close: January 1, 2027 (possibly 11:59 pm Dec 31 instead, so all donations fall in the 2026 tax year)
- Winners announced: first week back in January

## How the site is built

- Everything is in **one file: index.html** (HTML, CSS and JavaScript together). Keep it that way. No build tools, frameworks or extra files unless Nate asks.
- Hosted free on **GitHub Pages** from the main branch, root folder. Live at https://nathanielmarketing.github.io/Quasar-2026-Food-Drive-Competition/
- Pushing to main redeploys the site in about a minute.
- The repo is **public**. Never add passwords, logins, personal contact details, surnames of champions, or anything sensitive.

### The numbers block

At the top of index.html is a block marked "FOOD DRIVE NUMBERS: EDIT THIS BLOCK EACH FRIDAY."

- Everything else (team totals, % of goal, participation, progress bars, company total, "last updated" date) must be calculated from this block. Never hardcode those numbers elsewhere.
- Nate sometimes edits this block directly on github.com with the pencil icon. Keep it simple, clearly labelled and easy to edit by hand: plain numbers, no dollar signs or commas, one line per office.
- Recommended structure for the new format: keep one line per office with `raised`, `donors` and `people`, plus a `team` field ("HQ" or "Challengers"). The site adds up each team from its offices. This keeps the office breakdown and the team totals in sync automatically.
- Before editing, pull the latest version from GitHub so web edits aren't overwritten.

## Site changes needed for the new format

The current index.html was built for the old six-office competition. It needs updating to:

1. **Head-to-head scoreboard** as the centrepiece: Team HQ vs. the challengers, side by side, with % of goal, dollars raised vs goal, and participation for each. Make it feel like a sports matchup.
2. **Office breakdown for the challengers** underneath, so each small office (especially Timmins and North Bay) can see its contribution.
3. **Donation links:** two clear buttons, one per team, replacing the six office cards. Keep a short "which team am I on?" line.
4. **Update the rules, FAQ, hero copy and timeline** to the new format and dates.
5. Keep the participation toggle or show participation alongside % of goal.

## Brand and design

The site should feel like part of **The Pulse**, Quasar's internal SharePoint hub, but brighter and more festive.

- Fonts: Segoe UI first, with system fallbacks.
- Colours: brand blue `#1d5bd8`, deep blue `#123f9e`, navy `#10285c`, gold `#ffc21a`, light sky `#eaf2ff`.
- Section pattern from The Pulse: a gold eyebrow line above a large heading.
- The Quasar chevron shapes appear as decoration in the hero.
- Give each of the two teams a strong, distinct colour used consistently everywhere they appear. Individual office colours can stay for the challengers' office breakdown.
- Rounded cards, pill buttons, gold highlight on whichever team is leading.
- One moment of motion: totals count up and bars fill on load. Respect reduced-motion settings.
- Must work well on phones, and in both light and dark mode.

## Writing rules

- **Never use em dashes**, in page text, code comments or messages to Nate. Use commas, colons, parentheses or new sentences instead.
- Use curly apostrophes and quotes (’ “ ”) in visible text; straight quotes in code.
- Tone: friendly, casual, upbeat, clear. Short sentences. Canadian spelling (colour, centre, cheque).
- Keep explanations of the rules short. If something needs a paragraph to explain, simplify the rule.

## Planned additions

- Champion spotlights: headshots and trading-card style or Quick Q's style mini profiles for each office's champion.
- Final team names, prizes, food bank partner and donation links once confirmed.

## Working with Nate

- Show him what changed before pushing, and preview the page when possible.
- After pushing, remind him the site takes about a minute to update and to hard refresh (Ctrl + F5).
- If something might break the weekly update process, flag it before doing it.
- When a decision changes, update this file too.
