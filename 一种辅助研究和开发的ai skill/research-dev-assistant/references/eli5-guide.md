# ELI5 + first-principles explanation guide

Goal: explain so simply that a curious 10-year-old gets it, while staying technically
honest. Simple is not the same as wrong — it means stripping jargon, not stripping truth.

## The three blocks (always produce all three)
1. **What it is** — name it, then one everyday analogy.
2. **Why it works** — start from the most basic true fact and build up in 3–5 small
   steps. Each step must follow from the last with no hand-waving.
3. **Pros & cons** — honest tradeoffs and the conditions where it stops being the
   right pick.

## Rules of the style
- **Short sentences.** One idea each.
- **No undefined jargon.** If you must use a term, define it in the same breath with
  a plain-words gloss.
- **Use analogies from daily life** — kitchens, queues, maps, sorting laundry, a
  librarian, water flowing downhill.
- **First principles, not authority.** "Because the gradient points downhill, and we
  take small steps downhill, so we end up at the bottom" beats "because SGD converges."
- **Numbers with meaning.** Don't say "0.001"; say "a tiny step so we don't overshoot".
- **Admit uncertainty** in plain words: "we're not 100% sure why, but in tests it..."

## Good vs bad (example: gradient descent)
- ❌ Bad: "We minimize the loss via iterative first-order optimization."
- ✅ Good: "Imagine you're on a foggy hill and want the lowest point. You can't see far,
  so you feel which way is downhill and take a small step. Repeat. That's it. The
  'small step' size matters: too big and you bounce over the valley; too small and it
  takes forever."

## Pros & cons must be balanced
- Always give at least one real downside. If a thing has no downsides, you haven't
  understood it yet.
- State **when to use it** and **when NOT to**.

## Sanity check before sending
- Could a smart kid repeat the "why" back to you?
- Did you sneak in any word you didn't define?
- Is there at least one honest "this is bad when..."?
