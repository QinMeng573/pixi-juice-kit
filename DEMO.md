# Demo: feel the tiers in 60 seconds

Open `index.html` (PixiJS loads from CDN, so be online). A 9×5 grid appears.

## The click tour

1. **Set Damage to 3, click any cell.** A blue pulse travels outward, one cell every 0.088s. Small hit, small color, no shake. Tier 2.
2. **Set Damage to 18, click again.** Rose pulse (tier 4), noticeably louder color — still no shake. The kit reserves shake for real danger.
3. **Set Damage to 40, click.** Gold-orange (tier 6): the pulse is joined by screen shake *and* a 90ms freeze before it — that freeze is hit-stop, and it is what makes a crit feel heavy.
4. **Press "Crit (tier 6 + hit-stop + shake)"** a few times, then **"Hit (random tier)"** a few times. Notice you can *read* the damage from the color alone, without any numbers. That readability is the point of the tier table.

## The tier table (production values)

| Damage | Tier | Color | Shake | Hit-stop |
|---|---|---|---|---|
| ≤ 2 | 1 | green | — | — |
| ≤ 5 | 2 | blue | — | — |
| ≤ 11 | 3 | purple | — | — |
| ≤ 20 | 4 | rose | — | — |
| ≤ 35 | 5 | crimson | yes | — |
| > 35 | 6 | gold-orange | yes, ×1.6 | 90ms |

Thresholds 2 / 5 / 11 / 20 / 35 and the 0.088s-per-cell wave speed are tuned values from a shipped game (see README), not demo placeholders.

## What to steal first

If you take one thing: **the wave rule**. Flat solid fill + white border, one cell per 0.088s, no gradient, no particles. It reads instantly at any grid size and costs almost nothing to render.
