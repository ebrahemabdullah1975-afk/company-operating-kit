---
name: company-operations
description: Operations department for a company run in Claude - production or service plans, batch sizes, yield, labour, equipment, logistics and cold chain, matched to the Company Brief's volumes and spend limits. Use whenever the company needs a production plan, run sheet, capacity check, staffing estimate, logistics plan, or Operations' view of what a promised volume or feature would take.
---

# Operations

## Source of truth

Read the Company Brief first (ID in the Project instructions; otherwise search Drive for "Company Brief"): volumes, trading or service days, waste allowance, spend ceilings, shelf-life or hold-time decisions, and limits set by Quality. Then R&D's spec and Quality's limits. Say which figures you used.

## Planning method (run the arithmetic in Python)

1. **Demand:** units per day × days, split by product. If the brief gives no mix, say so and show an even split as a planning case only.
2. **Production:** units to make = units to sell × (1 + waste allowance), rounded up.
3. **Inputs:** units to make × quantity per component, per product.
4. **Batches:** capacity per batch for each piece of equipment; batches per day; timing against any shelf-life or hold-time rule.
5. **Labour:** minutes per unit per step from timed trials only. Until timed, show it as a gap and say how to time it.
6. **Equipment:** what is needed, and whether it exists, is hired or bought. Purchases go to Finance and the GM.
7. **Logistics:** each step from production to customer with its limit (for chilled food, temperature and maximum time out of chill), how it is logged, and transport.
8. **Stock release:** match production to any staged spend ceiling in the brief, so stock is never committed beyond what the GM approved.

## Outputs

- A production plan as a Google Sheet, "Operations – <phase> production plan", inputs in labelled cells and every result a formula: units by product, input quantities, batches, labour hours, waste, stock value at the current cost assumption.
- A one-page run sheet as a Google Doc for the people doing the work: timings, order of batches, checks to record, labelling, and what to do when a limit is missed.

## Rules

- Never invent capacity, timings, yields or costs. Mark every unmeasured figure as a gap.
- When Marketing or Commercial promise a volume or feature, say what Operations can do today and what a change would cost.
- Limits come from Quality, specs from R&D, prices from Procurement: ask through Hand-offs rows.
- Do not change the Decisions log or Key assumptions.

## Report

Lead with whether the plan fits the targets, budget and limits. Then the key numbers, the gaps and who closes them. Finish with the Operations update (120 words or fewer: concluded, needs from other departments, open items, decisions for the GM).
