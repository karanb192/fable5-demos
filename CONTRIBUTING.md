# Contributing a demo

This gallery collects **one-shot demos**: complete interactive pages an AI model built in a single attempt. If you've got one that made someone say "wait, *code* did that?" — send it.

## The rules

1. **One self-contained HTML file.** Inline CSS/JS only. No frameworks, no CDNs, no fonts fetched from anywhere, no network requests at all. If it can't run from a `file://` URL offline, it doesn't qualify.
2. **One shot, honestly stated.** The model built it in a single attempt. Follow-up *bug-fix* passes are fine (a verifier agent or a "fix the console error" nudge) — cosmetic re-prompting until it looks good is not. Say in your PR what the process was.
3. **Real algorithms, no fakery.** If your demo claims physics/math, the implementation must actually be there. A fluid demo needs a solver, not a particle trail with blur. This is the whole point of the gallery.
4. **Any model welcome.** Claude, GPT, Gemini, local models — state which model and version.
5. **It must be understandable in 5 seconds** by someone non-technical, and work on a phone (390px wide, touch).

## How to submit

1. Fork this repo
2. Add `your-demo-name/index.html` (kebab-case folder name)
3. Optionally add `your-demo-name/og.png` (1200×630 screenshot) for link previews
4. Add a card for it in `index.html` (copy an existing `<a class="card">` block) and a row to the README table — including the **"What's real inside"** line
5. Open a PR using the template — it asks for: model + version, the prompt (or a summary), what's real inside, and your one-shot honesty statement

## Review bar

PRs are checked for: self-containment (we grep for external requests), the claimed algorithm actually existing in the source, mobile usability, and honesty of the one-shot claim. Quality bar: would a stranger bookmark it?

## Ideas that would be great here

Path tracers · soft-body physics · working synthesizers · cellular automata · orbital mechanics · neural nets training live · procedural worlds · optical illusions · interactive math explainers — anything where **depth is visible**.
