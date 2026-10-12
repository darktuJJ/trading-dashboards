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
- Screenshots are **linked from the original repository** rather than copied here, to avoid licensing issues.

## Index

| Name | Link | Tech stack | Highlights / what to learn from | Screenshots | Notes |
| --- | --- | --- | --- | --- | --- |
| [SETS MACHINE](dashboards/SETS.md) | [darktuJJ/SETS](https://github.com/darktuJJ/SETS) (upstream [Shelpid/SETS](https://github.com/Shelpid/SETS)) | Plain HTML / CSS / vanilla JavaScript, drawn on `<canvas>` ([`dist/ui/draw.js`](https://github.com/darktuJJ/SETS/blob/main/dist/ui/draw.js)) | Live animation of a genetic-algorithm evolution (gene pool, lineage, fitness history); equity curve with trade markers; no framework, no build step | [Main view](https://raw.githubusercontent.com/darktuJJ/SETS/main/docs/images/hero.png) · [Gene pool GIF](https://raw.githubusercontent.com/darktuJJ/SETS/main/docs/images/genepool.gif) | A demo, not a trading system: paper trades on historical BTC data only |

## Adding an entry

1. Create `dashboards/<name>.md`, following the structure of [`dashboards/SETS.md`](dashboards/SETS.md).
2. Add a row to the index table above.
3. Link screenshots from the original repository; only copy images when the license clearly allows it.

## License

This repository's own content is licensed under the [MIT License](LICENSE). Referenced projects, screenshots and code belong to their original authors and remain under their own licenses.
