# Company Brief template

Fill every `{{placeholder}}`. Keep the section order: departments and automations look for these headings by name.

---

# Company Brief

Shared reference for every department. Each department reads this before answering and works from the facts below. Update it after every major decision.

*Last updated: {{date}}*

## Company overview
- Company name: {{name}}
- What the company does: {{one or two sentences}}
- Customers and market: {{who buys, through which channels}}
- Base and operating regions: {{where}}
- Stage: {{for example pre-scale validation: N phases over about N months before any major investment}}

## Mission and goals
**Mission**: {{one sentence}}

Objectives for the validation plan, with how each will be measured:
1. Phase 1 ({{timing}}, about {{budget}}): {{measurable target}}
2. Phase 2 ...
{{one line per phase}}

## Departments
Each department is a separate Claude Project with its own instructions.

| Department | Responsible for | Main outputs | Works with |
|---|---|---|---|
| General manager | Direction, phase budgets, go / no-go calls, arbitrating conflicts | Priorities, targets, decisions | All departments |
| {{department}} | {{remit}} | {{outputs}} | {{partners}} |

## How the departments work together
Work moves through stages. Each stage has one lead, one hand-off out and a Finance check.

| Stage | Lead | Hand-off out | Finance role |
|---|---|---|---|
| Set direction | General manager | Priorities, phase budgets, targets | Provides budget, target price and margin |
| Develop product | {{R&D, Quality}} | Tested product, specs, compliance sign-off | Confirms unit cost from quotes |
| Source and cost | {{Procurement}} | Supplier quotes, landed cost per unit | Checks quotes against the cost assumption |
| Make and control | {{Operations, Quality}} | Production run, yield, labour, logistics | Tracks actual cost against plan |
| Position and sell | {{Marketing, Commercial & sales}} | Brand, pitch, pilot listings, sales data | Sets the price floor and customer terms |
| Review and decide | Finance, then GM | Go / no-go / adjust decision | Reports margin and cash against targets |

If a phase misses its target, work returns to the department that owns the problem, not to the start.

Standing conflicts the GM arbitrates: Finance against Quality (cost cuts against compliance), Marketing against Operations (promised features against capability), Procurement against R&D (cheaper inputs against product quality). Finance flags conflicts early, with the numbers attached.

## Key assumptions
Facts and figures every department treats as current. Each line ends with its source and status: (GM decision, date), (planning figure, source) or (verified, source). Remove or correct a line as soon as it changes.
- {{assumption}} ({{source and status}})

## Decisions log

| Date | Decision | Departments affected | Reason |
|---|---|---|---|
| {{date}} | Run the company as a general manager plus {{N}} departments, all reporting directly to the GM. | All | Keeps lines of accountability short while the company is small. |

## Hand-offs
Requests passed from one department to another. Any department can add a row with Status Open. A daily scheduled dispatcher works each Open row as the department in the To column, using the Department Project Instructions doc in this folder, and updates the status. Status is Open, In progress, Waiting (needs a real-world input such as a quote or test result), Needs GM (needs a decision) or Done.

| Date | From | To | Ask | Status |
|---|---|---|---|---|

## Department updates
After each working session, each department replaces its own summary here (120 words or fewer: concluded, needs from other departments, open items, decisions for the GM).

### General manager
[latest summary]

### {{department}}
[latest summary]

## Open questions
- {{question}}. Owner: {{department or GM}}. Raised {{date}}.

## Archive
Done hand-offs and replaced decisions move here when the brief grows long, so the live sections stay quick to read. Moving a row is housekeeping, not a decision.
