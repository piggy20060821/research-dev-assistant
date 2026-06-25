# Code justification checklist — run before declaring code done

The rule: **every non-trivial line has a reason you can state out loud.** If you can't,
it's a guess — fix it or flag it.

## Per-decision
- [ ] **Library / framework:** Why this one over the obvious alternatives? (cite docs,
      maturity, fit). One sentence.
- [ ] **Algorithm / data structure:** Why this complexity is acceptable here. Cite the
      source or state the first-principles reason.
- [ ] **Every numeric constant:** No magic numbers. Each has a named meaning and a
      source ("default from <doc>", "Nyquist => 2x", "batch=32 is the common default").
- [ ] **Every hyperparameter / threshold:** Sourced from a paper, a doc default, or a
      stated reasoning — never "felt right".
- [ ] **Defaults:** Match the common industry default unless you state why you deviate.

## Correctness & robustness
- [ ] Edge cases handled (empty, null, zero, max, negative, unicode...).
- [ ] Error handling is deliberate, not swallowed silently.
- [ ] No security foot-guns (secrets in code, injection, unsafe eval, etc.).
- [ ] Units and types are explicit where they could be confused.

## Clarity
- [ ] Names say what the thing is.
- [ ] A short rationale comment sits on each non-obvious choice (only where it adds
      info — do not over-comment trivial lines).
- [ ] A reader could reconstruct *why*, not just *what*.

## Alternatives & honesty
- [ ] You considered at least one alternative and can say why you rejected it.
- [ ] Known limitations are written down (in a comment or the message to the user).

## Final gate
- [ ] Run the project's lint / typecheck / tests if they exist.
- [ ] If anything here failed and you couldn't justify it, tell the user instead of
      hiding it.
