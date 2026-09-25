# Tide Loader

An ASCII ocean loader. Blue water washes into a pure white square from the left, pulls back a little, leaves blue `+ = - :` grains on the sand, then reaches further.

**Live:** https://dakotashao.github.io/tide-loader/

## Versions

|  | Smooth | Strips |
| --- | --- | --- |
| **Loading** — four waves fill the square, hold 3 s, restart | [`/smooth/`](https://dakotashao.github.io/tide-loader/smooth/) | [`/strips/`](https://dakotashao.github.io/tide-loader/strips/) |
| **Endless** — the tide keeps coming and going, never fills | [`/smooth-endless/`](https://dakotashao.github.io/tide-loader/smooth-endless/) | [`/strips-endless/`](https://dakotashao.github.io/tide-loader/strips-endless/) |

- **Smooth**: the wave front is one continuous curve.
- **Strips**: the water arrives as thin horizontal strips with ragged ends, and sunlight flashes along the wave crests as they roll toward the shore.

## Structure

```
index.html              overview page linking all four
smooth/                 loading, smooth edge
strips/                 loading, strips
smooth-endless/         endless, smooth edge
strips-endless/         endless, strips
```

Each folder holds a self-contained `index.html` (open it directly in a browser, no build step) and a `preview.png` used for link previews. IBM Plex Mono loads from Google Fonts, with a monospace fallback.

## Tuning

All at the top of the script in each `index.html`:

| Constant | What it does |
| --- | --- |
| `PEAKS` / `TROUGHS` | Loading versions: how far each wave reaches, and where it pulls back to (0–1 of the square) |
| `FILL` / `HOLD` | Loading versions: seconds to fill, seconds to hold before restarting |
| `WAVE` | Endless versions: seconds per wave |
| `DRY` | How fast the leftover grains disappear (0 = they stay until the next wave covers them) |
| `COLS` / `ROWS` | Grid density |
| `BAND` | Strips versions: rows per strip |
