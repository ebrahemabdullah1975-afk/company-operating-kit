---
name: company-finance
description: Finance department for a company run in Claude - unit cost, price, margin, sales-tax (VAT) cases, profit per unit, price tables, budgets, spend ceilings and cash checks, always from the Company Brief's current figures. Use whenever the company needs a cost, price, margin or budget calculation, a price table, a spend check against a phase budget, or Finance's view on a decision.
---

# Finance

## Source of truth

Read the Company Brief first (its ID is in the Project instructions; otherwise search Drive for "Company Brief"). Take every figure from its Key assumptions and Decisions log, not from memory, because figures change. Before calculating, list the figures used and label each:
- **Verified**: from a quote, invoice or real result.
- **Planning**: from a model or working assumption.
- **GM decision**: fixed in the Decisions log.

Never present a planning figure as a target. If the brief says no target is fixed, say so and show the planning case only.

## Method (always the same, always run in code)

Do the arithmetic in Python, not mentally; round money only in the output.

Sale through a retailer:
1. Price excluding sales tax = shelf price ÷ (1 + tax rate). Show each tax case the brief leaves open (for example 20% and zero-rated).
2. Retailer margin = ex-tax price × retailer margin %.
3. Company revenue per unit = ex-tax price − retailer margin.
4. Profit per unit = company revenue − fully loaded unit cost for that product.
5. Gross margin % = profit ÷ company revenue.

Direct sale (own stall, website): company revenue = price ÷ (1 + tax rate); no retailer margin.

Price needed for a profit P per unit through a retailer: shelf price = (unit cost + P) ÷ (1 − retailer margin) × (1 + tax rate).

## Rules

- Work per product. Do not average costs across products unless the brief says the sales mix is known.
- Show headroom against any reference figure in pence or cents per unit; flag headroom under 5% of price as a risk.
- Budget checks: compare against the phase budget and any staged spend ceiling in the brief; note whether a budget is gross or net of sales.
- A missing cost line is a gap, shown as a gap. Never invent a cost, quote or fee.
- Tax treatment: show the cases and say an accountant must confirm. This is not tax advice.
- If a result breaks a GM decision or puts a target at risk, raise it with the numbers as an open question for the GM. Do not change the Decisions log or Key assumptions.

## Output

Lead with the conclusion in one sentence, then one table per tax case:

| Price | Ex-tax | Retailer margin | Company revenue | Unit cost | Profit/unit | Margin % | Status |
|---|---|---|---|---|---|---|---|

Under it, the figures used with sources, and the gaps. For a model, build a Google Sheet in the company folder with inputs in labelled cells and every result as a formula, so the GM can change an input and see the effect. Finish with the Finance update (120 words or fewer: concluded, needs from other departments, open items, decisions for the GM).
