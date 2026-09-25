# Tide Loader

An ASCII ocean loader. Blue water washes into a pure white square from the left in four gentle waves. Each wave pulls back a little and leaves blue `+ = - :` grains on the sand, then the next one reaches further. The fourth wave fills the square, it holds for three seconds, and the loop restarts.

Two versions:

- **Smooth** (`index.html`, live at https://dakotashao.github.io/tide-loader/): the wave front is one smooth curve.
- **Strips** (`strips/index.html`, live at https://dakotashao.github.io/tide-loader/strips/): the water arrives as thin horizontal strips with ragged ends, and sunlight flashes along the wave crests as they roll toward the shore.

Open either file in a browser. No build step, no dependencies (IBM Plex Mono loads from Google Fonts, with a monospace fallback).

## Tuning

All at the top of the script in `index.html`:

| Constant | What it does |
| --- | --- |
| `PEAKS` / `TROUGHS` | How far each wave reaches, and where it pulls back to (0–1 of the square) |
| `FILL` / `HOLD` | Seconds to fill, seconds to hold before restarting |
| `DRY` | How fast the leftover grains disappear |
| `COLS` / `ROWS` | Grid density |
| `RAMP` | Characters used inside the water, sparse → dense |
