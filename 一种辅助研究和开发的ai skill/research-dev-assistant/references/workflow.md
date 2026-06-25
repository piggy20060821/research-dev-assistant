# Workflow — the full step-by-step

This expands the 6 mandatory steps in `SKILL.md`. Follow them in order. Do not skip
ahead to code.

## Step 1 — Search papers first
- Restate the task in one plain sentence, then turn it into 2–3 search queries.
- Search academic sources before anything else (see `search-playbook.md`).
- Goal of this step: find out **how the problem is actually solved by people who
  studied it**, not how you guess it might be solved.
- If the task is purely engineering with no research angle (e.g. "rename a
  variable"), say so and skip to industry practice instead of forcing a paper search.

## Step 2 — Study & extract
For the strongest 2–4 sources, write down:
- **Core mechanism:** the one idea that makes it work, in a sentence.
- **Assumptions:** what must be true for it to work (data size, distribution,
  hardware, latency budget...).
- **Reported results:** numbers, on what benchmark, vs what baseline.
- **Failure cases:** where it breaks or is known to be worse.
- **Maturity:** is there reference code? Is it widely reproduced, or one paper?

If two sources disagree, note the disagreement — that is information, not noise.

## Step 3 — Explain like I'm 5 + first principles
Produce three short blocks. See `eli5-guide.md` for the style.
- **What it is** — name it and give one everyday analogy.
- **Why it works** — start from the most basic true fact and build up in 3–5 steps.
  No step may rely on jargon that wasn't just defined.
- **Pros & cons** — honest tradeoffs, plus the conditions under which it stops being
  the right choice.

## Step 4 — Let the user decide
- Offer **2–3 concrete options**, each with: what it is, cost/benefit, when to pick it.
- Give a **clear recommendation** and one sentence on why.
- **STOP and wait.** Do not start implementing until the user picks. This is a hard
  gate, not a suggestion.

## Step 5 — Same rigor for user-supplied inputs
Whenever the plan needs a value or choice from the user (a threshold, a model, a
framework, a folder layout...):
- Do NOT ask a blank question.
- First search **industry-common usage**: what do most real projects use here, and why.
- Present the common options with ELI5 tradeoffs and a default.
- Then let the user confirm or override.

## Step 6 — Justify every line of code
- Before writing code, list the non-trivial decisions and their source.
- While writing, annotate each non-obvious choice with a one-line reason.
- No magic numbers, no copy-pasted parameters whose meaning you can't state.
- After writing, run `code-justification-checklist.md` and fix anything that fails.

## Anti-patterns (never do these)
- Jumping straight to code without searching.
- "Best practice says..." with no named source.
- Choosing a library because it's popular, without saying what it buys you here.
- Picking hyperparameters that "felt right".
- Making a big/irreversible decision for the user instead of asking.
