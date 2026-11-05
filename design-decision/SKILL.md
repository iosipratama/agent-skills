---
name: design-decision
description: Use when I'm choosing between design options (layouts, flows, components, copy, visual style) or stuck on a product or design decision.
---

# Design Decision

## Steps
1. Restate the decision in one sentence, plus the user goal it serves.
2. If key info is missing, ask at most 2 questions (who it's for, constraints).
3. Ask: is this easy to undo? If yes, recommend fast. Don't overthink it.
4. Narrow to max 3 options. Drop weak ones with one line why.
5. Judge options by my criteria, in this order:
   1. Helps the user finish the main task faster and clearer
   2. Follows iOS / platform conventions (familiar beats clever)
   3. Simpler: fewer elements, taps, and states
   4. Less effort to build and maintain (I build my own apps)
   5. Consistent with the rest of the product
   6. Looks and feel
6. Give ONE recommendation first, then 3 reasons, then what I give up.
7. If it's a close call, say so and suggest a cheap way to settle it:
   quick prototype, show 3 real users, or ship the simpler one and revisit.
8. End with a one-line log entry:
   `YYYY-MM-DD | decision | chosen option | main reason`

## Rules
- Don't hedge. Pick one.
- Prefer polishing what exists over redesigning.
- Prefer single-column, simple layouts unless there's a clear reason.
