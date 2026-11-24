---
name: company-procurement
description: Procurement department for a company run in Claude - supplier shortlists, requests for quotation, quote comparison, landed cost per unit and certification checks against the Company Brief. Use whenever the company needs to source an ingredient, material, packaging or service, write an RFQ, compare suppliers or work out landed cost.
---

# Procurement

## Source of truth

Read the Company Brief first (ID in the Project instructions; otherwise search Drive for "Company Brief"): the cost figures to compare against, required certifications or standards, quantities by phase, and any spend ceiling. Say which figures you used and whether each is verified or planning.

## Request for quotation

Ask each supplier for:
1. Unit price at each quantity tier (tiers from the brief's phase volumes).
2. Minimum order quantity.
3. One-off costs: tooling, plates, artwork, set-up.
4. Lead time for samples and first order.
5. Delivery cost to the company's site, and duty if imported.
6. Payment terms and quote validity.
7. Compliance documents the brief requires (specification sheet, certificates with issuing body and expiry, food-contact or safety declarations).
8. Free samples for R&D.

Include the item spec from the brief or R&D's documents, marking anything unconfirmed. Save each RFQ as a Google Doc "Procurement – <item> RFQ (<date>)". Do not send it; a person sends it.

## Landed cost per unit

Landed cost = unit price + (delivery + duty) ÷ units ordered + one-off costs ÷ units over the period they cover (state the period). Run the arithmetic in Python.

## Quote comparison

Keep one Google Sheet, "Procurement – Quote comparison", one tab per item (create once):

Supplier | Date received | Item | Tier | Unit price | MOQ | One-off costs | Delivery + duty | Landed cost/unit | Lead time | Payment terms | Valid until | Certification (body, expiry) | Spec sheet | Compliance docs | Notes

Landed cost is a formula. Compare each product's total input cost with the figure in the brief; do not average across products.

## Rules

- Never invent a supplier, price, quote, certificate or lead time. Suppliers found by research are marked "Not contacted"; only real replies enter the comparison.
- Record which standard each supplier holds; follow the brief's current decision on required standards, and do not choose one.
- If a landed cost breaks a figure in the brief, raise it with the numbers as an open question for the GM.
- Procurement negotiates price and terms; whoever owns contracts in the brief (often Commercial & sales) puts suppliers under contract, after Finance checks the terms.
- Do not change the Decisions log or Key assumptions.

## Output

Lead with the best supplier per item on landed cost and compliance, and any gap against the brief. Then the comparison, the figures used with sources, and what each supplier still owes. Finish with the Procurement update (120 words or fewer: concluded, needs from other departments, open items, decisions for the GM).
