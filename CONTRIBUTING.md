# Contributing a simulation

This collection is **one-shot simulations by Claude Fable 5**: complete interactive simulations the model built in a single attempt. If you prompted Fable 5 and it produced something that made someone say "wait, *one prompt* did that?" — send it.

## The rules

1. **One self-contained HTML file.** Inline CSS/JS only. No frameworks, no CDNs, no fonts fetched from anywhere, no network requests at all. If it can't run from a `file://` URL offline, it doesn't qualify.
2. **One shot, honestly stated.** The model built it in a single attempt. Follow-up *bug-fix* passes are fine (a verifier agent or a "fix the console error" nudge) — cosmetic re-prompting until it looks good is not. Say in your PR what the process was.
3. **Real algorithms, no fakery.** If your simulation claims physics/math, the implementation must actually be there. A fluid demo needs a solver, not a particle trail with blur. This is the whole point of the collection.
4. **Built with Claude Fable 5.** This collection documents what Fable 5 can do in one attempt — state the exact model string (e.g. `claude-fable-5`) in your PR. (Impressive one-shots from other models are worth publishing too — just in their own repos; happy to link truly great ones from the README.)
5. **It must be understandable in 5 seconds** by someone non-technical, and work on a phone (390px wide, touch).

## How to submit

1. Fork this repo
2. Add `your-demo-name/index.html` (kebab-case folder name)
3. Optionally add `your-demo-name/og.png` (1200×630 screenshot) for link previews
4. Add a card for it in `index.html` (copy an existing `<a class="card">` block) and a row to the README table — including the **"What's real inside"** line
5. Open a PR using the template — it asks for: the model string, the prompt (or a summary), what's real inside, and your one-shot honesty statement

## Review bar

PRs are checked for: self-containment (we grep for external requests), the claimed algorithm actually existing in the source, mobile usability, and honesty of the one-shot claim. Quality bar: would a stranger bookmark it?

## Ideas that would be great here

Path tracers · soft-body physics · working synthesizers · cellular automata · orbital mechanics · neural nets training live · procedural worlds · optical illusions · interactive math explainers — anything where **depth is visible**.
