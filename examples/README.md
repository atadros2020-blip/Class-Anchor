# Example — Calc 1A (Calculus I)

[`calc-1a.html`](calc-1a.html) is a finished concept map for a first-semester
calculus course (modeled on Foothill College's Math 1A). Open it in any
browser — no setup, no internet needed.

## What it demonstrates

It shows every design standard in one file:

- **One root.** The whole course hangs off a single question — *how do things change?* — drawn as the "Rate of change" node near the top.
- **A spine, then branches.** Function review → rate of change → limits → derivatives runs straight down the middle. Derivatives then fan out into "rules for computing" on the left and "what you do with them" on the right, and the spine ends pointing at Calc 1B.
- **Typed nodes.** Each topic is tagged (Prerequisite, Core idea, Foundation, Rule, Application) so the structure is visible at a glance.
- **Detail on demand.** The map surface is almost text-free. Click any node and a panel opens with the formula, what it builds on, what it leads to (with the *why*), and a practice problem with a worked solution.
- **The thread, said out loud.** The "Why are we learning this?" button narrates the through-line from algebra to integrals.

## How it was made

It was generated from the course's materials using [`../prompt.txt`](../prompt.txt), then hand-checked and edited for mathematical accuracy. That is the intended workflow: the prompt produces a strong first draft, and the instructor — the subject-matter expert — corrects and finalizes it.

To use it as a starting point for your own course, copy the file and edit the title, the Canvas link in the top bar, and the `TOPICS` object near the bottom of the file.
