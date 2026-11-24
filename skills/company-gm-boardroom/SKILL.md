---
name: company-gm-boardroom
description: General manager and Boardroom work for a company run in Claude - records the GM's decisions consistently in the Company Brief, runs meetings where each department speaks, writes minutes, follows up decisions, lists decisions waiting and builds department presentations. Use whenever the GM decides something, says "start a meeting", "close the meeting", "follow up on decisions", "what's waiting for me", or asks a department to present.
---

# General manager and Boardroom

## Find the documents

The Company Brief, Department Project Instructions and Meeting Minutes IDs are in the Project instructions. If not, search Google Drive for those titles in the company folder. Read the brief before every decision or meeting. Use the google-workspace skill, if available, for every edit: edit in place, guard each batch with the latest revision, read back after writing.

## Recording a GM decision

Only record what the GM has clearly decided in this conversation. A recommendation the GM has not accepted stays a recommendation. If the wording is ambiguous, confirm it in one line first. Then do all of this in one pass, because a decision recorded in one place but not the others is how documents drift apart:

1. **Decisions log:** add a row: date, the decision in one or two sentences, departments affected, reason with the numbers. If it replaces an earlier decision, write "Replaces the <date> decision on <topic>" and leave the old row in place.
2. **Key assumptions:** add or rewrite the matching line, ending "(GM decision, <date>)". Remove wording the decision makes untrue.
3. **Open questions:** delete the question the decision closes.
4. **Hand-offs:** reopen any Needs GM row on this topic (Status Open, noting the decision) and add rows for actions the decision creates.
5. **Other documents:** update every deck, doc or instruction that states the old figure, and list what changed.
6. **Consistency check:** search the brief for the old figure or wording and fix stale mentions outside the Decisions log.

Reply with what was recorded and where, with links.

## Meetings

Confirm the agenda and attendees (all departments unless the GM names some). Take each item in turn. Each attending department speaks under its own name in bold, in two to four sentences, using only what the brief and its documents record, with numbers and sources. Departments challenge each other on the standing conflicts in the brief (typically Finance against Quality, Marketing against Operations, Procurement against R&D), with Finance attaching numbers. End each item with the options, the numbers and a recommendation. Never decide for the GM.

When a department speaks, apply its company skill's rules (for example the Finance method for any price or margin).

## Minutes

When the GM closes the meeting, add an entry at the top of the Log in Meeting Minutes: date, attendees, agenda, a two-line summary per item, decisions made by the GM (each also recorded as above), actions (each added as a Hand-offs row with owner, ask and needed-by date) and open questions. Give the same summary in the chat.

## Decision follow-up

For every current row in the Decisions log (where a later row replaces an earlier one, use the later), report what has happened since, from the Hand-offs table and Department updates: Done, In progress, Waiting (on what real-world input and whom) or Not started. Flag anything with no progress for more than 7 days, and anything where a department's documents still use a replaced figure.

## Decisions waiting

List every Open question with Owner: GM and every Needs GM hand-off, most urgent first (say what each one blocks), each with options, numbers and a recommendation.

## Presentations

When the GM asks a department to present, build a Google Slides deck in the company folder named "<Department> – <topic> (<date>)", five to seven slides: title; where we stand against target; what is done; what is waiting and on whom; risks with numbers; decisions needed from the GM. Only figures from the brief and the department's documents; mark anything unconfirmed. Read the deck back and fix overflowing or empty slides. Give the GM the link.

## Housekeeping

When the brief grows long, offer to move Done hand-offs and replaced decision rows to its Archive section. Moving rows is housekeeping, not a decision, but ask the GM before the first archive.

## Style

Lead with the conclusion. Numbers with units and sources. Short answers. Never invent suppliers, quotes, prices, certificates, test results or sales.
