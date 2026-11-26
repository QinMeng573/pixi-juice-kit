# pixi-juice-kit

**Game-feel effects for PixiJS, extracted from a real shipped game — not invented for a demo.**

v0.1 is a single-file playground (`index.html`, PixiJS 7 via CDN). Open it, click the grid, steal what you like.

**Guided demo:** [DEMO.md](DEMO.md) — feel all 6 damage tiers in 60 seconds of clicking.

## Effects in v0.1

| Effect | Rule it ships with |
|---|---|
| Shockwave grid pulse | Travels cell-to-cell at **0.088s per cell**, flat solid fill + border — no gradients, no noise |
| Damage tier flash | 6 tiers by damage — thresholds **2 / 5 / 11 / 20 / 35**: green → blue → purple → rose → crimson → gold-orange |
| Screen shake | Amplitude scales with tier, decays ×0.88 per frame |
| Hit-stop | 90ms freeze, crit tiers (5–6) only |

These numbers are production tuning from *Chess of King*, a PvZ-style tower-defense chess game — playtested values, not placeholders.

## Why

Most "juice" demos show effects with arbitrary numbers. This kit publishes the
exact thresholds and timings a real game settled on, so you start from tuned values.

## Roadmap (in order, no perfectionism)

- [ ] Extract each effect into importable modules (`src/shockwave.ts`, `src/hitstop.ts`, ...)
- [ ] Landing squash for jumping units (0.16 / 0.18 squash values from the same game)
- [ ] Cathedral volumetric light + emblem break-out effects

## License

MIT
