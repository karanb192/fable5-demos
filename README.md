# Fable 5 Demos

**Live gallery → https://karanb192.github.io/fable5-demos/**

Five self-contained interactive demos, each designed, coded and debugged **in a single shot by [Claude Fable 5](https://www.anthropic.com)** — no frameworks, no CDNs, no build step, no human edits. Every demo is one HTML file.

| Demo | What it is | What's real inside |
|---|---|---|
| [🦋 The Butterfly Effect](https://karanb192.github.io/fable5-demos/butterfly-effect/) | 100 double pendulums released 0.0001° apart | Exact equations of motion, RK4 integration at 240Hz in float64 — the divergence is a measured Lyapunov blow-up, not a script |
| [🕊️ Murmuration](https://karanb192.github.io/fable5-demos/murmuration/) | A starling flock; your cursor is the hawk | Reynolds boids (separation / alignment / cohesion) over a spatial hash grid — the shapes emerge |
| [🖌️ Ink & Water](https://karanb192.github.io/fable5-demos/ink-water/) | Paint with living ink in water | Navier-Stokes solved in WebGL shaders: advection, vorticity confinement, Jacobi pressure projection |
| [✏️ Circle Scribe](https://karanb192.github.io/fable5-demos/circle-scribe/) | Spinning circles redraw your sketch | A real discrete Fourier transform — the circles are the Fourier series of your drawing |
| [🎼 Sorting Orchestra](https://karanb192.github.io/fable5-demos/sorting-orchestra/) | Four sorting algorithms race, audibly | Genuine algorithm implementations as generators; audio/visuals driven by the actual compare/swap events |

## How these were made

Each demo was produced by an autonomous multi-agent workflow: a research phase (what makes people say "wow"), an ideation phase (20 specs, each with its own visual identity), a build phase (one agent per demo, single attempt), and an adversarial verification phase (another agent hunts for bugs, fake physics, and external dependencies, then fixes what it finds). The five here are the curator's favorites out of 20.

**Rules every demo follows:**
- One self-contained HTML file — inline CSS/JS only, zero external requests
- Real algorithms, no fakery — if it says Navier-Stokes, there's a pressure solver in the source
- Works on a phone, respects `prefers-reduced-motion`, light/dark aware (or a deliberate committed theme)

## Contributing

Got a one-shot demo of your own (any model)? PRs welcome:

1. Add `your-demo/index.html` — fully self-contained, no external requests
2. State the model and that it was one attempt (light cleanup passes are fine — say so)
3. Add a card to `index.html` and a row to this table, including what's *real* inside

## License

MIT — do whatever you like, attribution appreciated.
