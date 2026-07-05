# One-Shot Simulations · by Claude Fable 5

**Live gallery → https://karanb192.github.io/fable5-demos/**

A collection of **real interactive simulations, each written in a single attempt by [Claude Fable 5](https://www.anthropic.com)** — chaos theory, fluid dynamics, emergent flocking, Fourier analysis, algorithm visualization. One prompt in, one working simulation out.

Every piece follows the same three constraints:

1. **One shot.** The model wrote it in a single attempt — no iterating until it looks right. (An adversarial verifier agent was allowed to fix genuine bugs; that's it.)
2. **One file.** Self-contained HTML — inline CSS/JS, zero external requests, no frameworks, no build step. It runs from a `file://` URL, offline.
3. **Real algorithms.** If it says Navier-Stokes, there is a pressure solver in the source. Nothing is faked with noise and blur — open view-source and check.

## The collection

| Simulation | What you see | What's actually running |
|---|---|---|
| [🦋 The Butterfly Effect](https://karanb192.github.io/fable5-demos/butterfly-effect/) | 100 double pendulums released 0.0001° apart agree, then explode into chaos | The exact double-pendulum equations of motion, RK4-integrated at 240Hz in float64 — the divergence you watch is a measured Lyapunov blow-up, not a script |
| [🕊️ Murmuration](https://karanb192.github.io/fable5-demos/murmuration/) | A starling flock that reacts to your cursor — the hawk | Reynolds boids: separation / alignment / cohesion computed from actual neighbors over a spatial hash grid — the flock's shapes emerge |
| [🖌️ Ink & Water](https://karanb192.github.io/fable5-demos/ink-water/) | Ink you pour into water, swirling like the real thing | Navier-Stokes solved on the GPU in WebGL shaders: advection, vorticity confinement, Jacobi pressure projection |
| [✏️ Circle Scribe](https://karanb192.github.io/fable5-demos/circle-scribe/) | A chain of spinning circles that redraws whatever you sketch | A discrete Fourier transform of your drawing — the circles are its Fourier series, reconstructed live |
| [🎼 Sorting Orchestra](https://karanb192.github.io/fable5-demos/sorting-orchestra/) | Four sorting algorithms racing on the same bars, audibly | Genuine algorithm implementations as generators — every note and flash is an actual compare/swap event |

## Why "one shot" matters

Anyone can iterate an AI toward a pretty result. These are different: a single prompt produced the complete working system — the physics, the rendering, the interaction design, the visual identity, the mobile layout. The gap between "looks like a simulation" and "is a simulation" is exactly where model depth shows, and it's verifiable: the source is right here.

## How the collection was made

An autonomous multi-agent pipeline, every agent running Fable 5: research (what makes people say *wow*) → ideation (specs with distinct visual identities) → **one-shot build** (one agent, one attempt per simulation) → adversarial verification (a second agent hunts for bugs, fake physics, and external dependencies, then fixes what it finds). These five are the curated best of that run.

## Contributing

Want to add a one-shot Fable 5 simulation to the collection? PRs welcome — see [CONTRIBUTING.md](CONTRIBUTING.md). The bar: single attempt (honestly stated), single self-contained file, and the algorithm genuinely implemented in the source.

## License

MIT — do whatever you like, attribution appreciated.
