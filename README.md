# Company Operating Kit

Run a small company inside Claude. You are the general manager (GM). Each department is its own Claude Project, they share one Company Brief in Google Drive, they pass work to each other through a tracked Hand-offs table, and only you make decisions.

Built from a real pre-scale food start-up run this way; that company appears only as an anonymised worked example.

## What you get

| Part | What it does |
|---|---|
| **company-setup** | Interviews you about your company, then builds everything: the Drive folder, Company Brief, Department Project Instructions, Meeting Minutes, Dispatcher log, and the two scheduled tasks. Gives you the text to paste into each Project. |
| **company-gm-boardroom** | Records your decisions consistently, runs Boardroom meetings where each department speaks in turn, writes minutes, follows up decisions, lists what is waiting for you, and builds department presentations. |
| **Eight department skills** | Finance, R&D, Procurement, Operations, Quality, IT/AI, Marketing, Commercial & sales. Each one reads its numbers from your brief, works in a fixed way, never invents figures, and ends with a short department update. |
| **Daily dispatcher** (scheduled task) | Every morning, works each Open hand-off as the receiving department, sets its status (Done, Waiting, Needs GM), flags anything waiting more than 7 days, checks its own work, writes an entry in the Dispatcher log and sends you a summary. |
| **Weekly review** (scheduled task) | Every Monday, builds a Google Slides deck: phase status, one slide per department, decision follow-up, decisions waiting for you, new skills worth adding. |

## Install

In Claude Code (2.1.275 or later):

```
/plugin marketplace add ebrahemabdullah1975-afk/company-operating-kit
/plugin install company-operating-kit@company-operating-kit
```

In the Claude app, download the latest `.plugin` file from this repository's releases (or zip this folder and rename it to `company-operating-kit.plugin`), open it in Claude and accept the plugin.

## Requirements

- A Claude plan with Projects, skills and scheduled tasks.
- Google Workspace connectors turned on: Google Drive and Google Docs (required), Google Slides (for decks), Google Sheets (for models and logs).

## Getting started

1. Install the plugin.
2. In a new chat, say **"Set up my company in Claude"**.
3. Turn on every connector your departments will use first (Google Drive, Docs, Sheets, Slides, and any design tool), because the scheduled tasks pick up connectors when they are created.
4. Answer the interview (company, product, stage, phases, departments).
5. Create one Project per department, plus a General manager Project and a Boardroom Project, and paste in the instructions the setup gives you. Turn on the Google connectors in each.
6. Start working: talk to departments, hold a Boardroom meeting, make decisions.

## Ground rules built in

- The Company Brief is the single source of truth; skills read figures from it every time, so your decisions flow through without editing any skill.
- Only the GM decides. Departments and automations raise options; they never record a decision.
- Nothing is invented: no suppliers, prices, quotes, certificates, test results or sales. Gaps stay visible.
- Departments cannot see each other's chats; anything that matters goes in the brief.

## Licence

Apache 2.0.
