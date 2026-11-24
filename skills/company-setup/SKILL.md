---
name: company-setup
description: Sets up a company to run inside Claude, with a general manager, department Projects, a shared Company Brief in Google Drive, tracked hand-offs, a daily dispatcher, a Boardroom and a weekly review. Use when the user says "set up my company in Claude", wants departments as Claude Projects, wants to run a start-up or small business with AI departments, or wants to add, rename or remove a department in an existing setup.
---

# Company setup

Build a working "company in Claude" for the user, who becomes its general manager (GM). Read this whole file before starting; the templates are in `references/`.

## What gets built

1. A Google Drive folder named after the company.
2. **Company Brief** (Google Doc): the single source of truth. Template: `references/brief-template.md`.
3. **Department Project Instructions** (Google Doc): the common block, one block per department, a GM block and a Boardroom block. Template: `references/instructions-template.md`.
4. **Meeting Minutes** (Google Doc). Template: `references/minutes-template.md`.
5. **Dispatcher log** (Google Doc), owned by IT/AI (or the GM if IT/AI is dropped). Template: `references/dispatcher-log-template.md`.
6. Two scheduled tasks: the daily dispatcher (`references/dispatcher-prompt.md`) and the weekly review (`references/weekly-review-prompt.md`).
7. The text the user pastes into each Project, and a short checklist for them.

## Step 1: Check the tools

Check that Google Drive and Google Docs connectors are available; Slides and Sheets are needed for decks and models. If the google-workspace skill is available, load it before the first edit and follow it. If Drive or Docs is missing, say which connector to turn on and stop; everything depends on the shared brief.

## Step 2: Interview the GM

Ask in one or two rounds, with AskUserQuestion where available. Take answers already given in the conversation instead of asking again.

- Company name (a code name is fine), what it makes or sells, who the customer is, where it operates.
- Stage and mission: what has to be proven before the next big commitment.
- Validation phases: for each, a name, timing, budget and one measurable target. If the GM has none yet, propose a short sequence that fits the business (for example prototype, small live test, pilot with partners, verification, scale pitch) and let them edit it.
- Departments: offer the default nine (GM, R&D, Procurement, Operations, Quality, IT/AI, Marketing, Commercial & sales, Finance) and let them rename, merge or drop any. For each kept department, confirm a one-line remit.
- Starting figures they already have (costs, prices, margins, budgets), each marked as planning or verified.
- Schedule: daily dispatcher time and weekly review day and time, in their time zone. Defaults: 06:32 daily, Monday 07:37.

Never fill a gap with an invented figure. Missing numbers go into the brief as open questions with Owner: GM.

## Step 3: Build the documents

1. Create the folder in Drive.
2. Create the documents in this order, because later ones quote the IDs of earlier ones: Company Brief, Meeting Minutes, Dispatcher log, then Department Project Instructions. Upload each as HTML with Google Drive create_file (contentMimeType text/html, parentId the folder), which converts to a native Google Doc with real headings and tables. Write header-row cells as `<td><b>...</b></td>`: plain `<th>` cells lose their bold in conversion.
3. Fill every template placeholder in `{{double braces}}` from the interview; delete sections that do not apply. Remove the department rows and blocks the GM dropped and add any new department in the same shape. Leave `{{instructions_id}}` in the instructions doc as it is, then, once the doc exists, replace it with the doc's own ID using a Google Docs replaceAllText request.
4. Read each document back and check: no `{{` left, tables intact, headings in order.
5. Record the IDs of the folder and the four documents; every later prompt needs them.

## Step 4: Create the scheduled tasks

Fill `references/dispatcher-prompt.md` and `references/weekly-review-prompt.md` with the company name, GM name, departments and document IDs (including the Dispatcher log ID). Create the tasks only after the GM has turned on every connector the departments will use (Google Drive, Docs, Sheets, Slides, plus any design or other tools): a new task picks up the connectors on the account when it is created, and adding one later is harder than recreating the task. If a scheduling tool is available (for example create_trigger), create both tasks in the GM's time zone with push notifications on, and say which approval setting each received. If no scheduling tool is available, give the GM the filled prompts to schedule themselves.

Offer one manual test run of the dispatcher after the GM has created the Projects. After any run, check that the Decisions log and Key assumptions are unchanged; if the dispatcher changed them, restore them and tighten its prompt.

## Step 5: Hand over

Give the GM, in this order:
1. Links to the folder and the four documents.
2. A checklist: create one Project per department plus "<Company> – General manager" and "<Company> – Boardroom"; paste the common block then the department's own block into each; paste the Boardroom block alone into the Boardroom; turn on Google Drive, Docs, Slides and Sheets in each.
3. How to work: ask a department in its Project; hold meetings in the Boardroom ("Start a meeting. Agenda: ..."); make decisions in the GM Project or the Boardroom; read the weekly deck on Mondays.
4. What cannot be automated: departments cannot see each other's chats, and anything needing the real world (quotes, tests, contracts, signatures) needs a person.

## Changing the setup later

To add, rename or remove a department: update the Departments table in the brief (as a GM decision, using the company-gm-boardroom skill), add or edit its block in the instructions doc, update the dispatcher and weekly-review prompts if they list departments, and tell the GM which Projects need re-pasting.

## Worked example

`references/example.md` shows an anonymised food start-up set up this way. Use it to show the GM what good entries look like; never copy its figures into another company.
