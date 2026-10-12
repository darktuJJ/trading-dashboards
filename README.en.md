[简体中文](README.md) · **English**

# trading-dashboards

A collection of trading / strategy dashboard UIs I come across, kept as references for design and implementation.

## Purpose

- Record trading dashboards worth learning from (backtesting, live monitoring, strategy evolution, risk panels, etc.).
- Focus on the **UI and visualization** itself: layout, charts, animation, interaction and implementation technique.
- Reference only. Inclusion is not an endorsement of any strategy or its trading performance.

## How entries are organized

- Each entry has its own Markdown file under [`dashboards/`](dashboards/), e.g. [`dashboards/SETS.md`](dashboards/SETS.md), covering source, tech stack, highlights, key files and caveats.
- The index table below has one row per entry, linking to its detail file.
- Screenshots live under [`dashboards/assets/`](dashboards/assets/), one folder per entry, with source and copyright noted in the detail file.

## Index

| Name | Link | Tech stack | Highlights / what to learn from | Screenshots | Notes |
| --- | --- | --- | --- | --- | --- |
| [SETS MACHINE](dashboards/SETS.md) | [Shelpid/SETS](https://github.com/Shelpid/SETS) | Plain HTML / CSS / vanilla JavaScript, drawn on `<canvas>` ([`dist/ui/draw.js`](https://github.com/Shelpid/SETS/blob/main/dist/ui/draw.js)) | Live animation of a genetic-algorithm evolution (gene pool, lineage, fitness history); equity curve with trade markers; no framework, no build step | [Main view](dashboards/assets/SETS/hero.png) · [Gene pool GIF](dashboards/assets/SETS/genepool.gif) · [Demo video](dashboards/assets/SETS/sets-machine-promo.mp4) | A demo, not a trading system: paper trades on historical BTC data only |

## Adding an entry

1. Create `dashboards/<name>.md`, following the structure of [`dashboards/SETS.md`](dashboards/SETS.md).
2. Add a row to the index table above.
3. Put screenshots in `dashboards/assets/<name>/` with attribution; remove them promptly if the original author asks.

## License

This repository's own content is licensed under the [MIT License](LICENSE). Referenced projects, screenshots, videos and code belong to their original authors and are not covered by the MIT License.
