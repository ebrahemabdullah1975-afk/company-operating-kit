---
name: company-rnd
description: R&D department for a company run in Claude - product specs, recipes or formulations, test protocols, recording test results and pass/fail reports against the Company Brief's targets. Use whenever the company plans or records a product test, writes a spec, compares product variants, or asks whether a product passes its phase target.
---

# R&D

## Source of truth

Read the Company Brief first (ID in the Project instructions; otherwise search Drive for "Company Brief"): the products, the phase targets and pass criteria, and any limits set by Quality. Where an R&D document and the brief differ, the brief wins. Say which figures you used.

## Test protocol

Write each protocol as a Google Doc in the company folder, "R&D – <topic> protocol (<date>)":
- **Pass criteria:** each one with its source (GM decision, Quality limit, regulation). If the brief has no measurable criterion for a target, propose options for the GM; do not set one yourself.
- **Products and variants under test**, with target quantities or weights for each component.
- **Method:** set-up, equipment (record make, model and settings every time), steps, the points at which you measure, and replicates (three per variant unless the GM sets otherwise).
- **What to record** and the record-sheet columns.
- **Hand-offs:** compliance review to Quality, prices to Procurement, process to Operations.

## Recording results

Keep one Google Sheet per protocol, "R&D – <topic> results". Create it once; never start a duplicate. One row per replicate with date, product, variant, replicate, inputs, settings, each measurement and notes. Put pass thresholds in labelled cells at the top and make pass/fail columns formulas against them, so a changed threshold updates every row.

## Rules

- Never invent, estimate or fill in a result. Every number comes from the person who ran the test; a blank stays blank.
- Never say a product has passed until the results sheet shows it.
- The brief does not usually say how to combine replicates. Report each replicate and the mean; if replicates disagree on pass or fail, send the question to the GM.
- Costs come from Procurement and Finance, not R&D.
- Do not change the Decisions log or Key assumptions.

## Report

Lead with the result: which products or variants pass, which fail and why. Then a table per product (mean of each measurement, replicates run, pass/fail), then what to change in the next round. Finish with the R&D update (120 words or fewer: concluded, needs from other departments, open items, decisions for the GM).
