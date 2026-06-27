# Modern Glass

A flat, glassmorphic, **mobile-first design system** aligned with Apple HIG and Material 3.
Depth comes from **tonal elevation** (no shadows or glows); **dark themes can be generated
from a single seed color**, with accents normalized to a WCAG-AA readable tone.

> **License:** CC BY-NC 4.0 — free to use and adapt for **non-commercial** purposes with
> attribution. **Commercial use is not permitted.** See [`LICENSE`](LICENSE).

## Spec

The machine-readable spec is in **[`design-system.yaml`](design-system.yaml)**: design tokens,
themes (dark / light + seed derivation), the typography scale, elevation, touch targets,
motion, accessibility, icons, haptics, and component conventions.

## Highlights

- **Tonal elevation** — `bg(0) < card(1) < nested chip(2) < nav(3)`, each a lighter tone.
  No shadows, no glows. Light mode steps page → white card → faint recessed nested.
- **Seed-derived dark themes** — surfaces come from one color (hue only, low chroma, very
  dark); the accent is lightened to ≥ 4.5:1 contrast. *Identity from the surface tint,
  legibility from the accent tone* — never fight one color to do both.
- **Typography** — Hanken Grotesk (UI/display/numeric), JetBrains Mono (uppercase
  micro-labels). Body 17px, secondary floor 15px, tabular numbers.
- **HIG interaction** — 44px minimum touch targets, press feedback (`scale .97`),
  `:focus-visible` rings, `prefers-reduced-motion` respected, ARIA, and haptics mapping.
- **No emoji** — icons are a webfont (e.g. Material Symbols) or text.

## Themes

Switched via a `data-theme` attribute that swaps CSS custom properties (`--bg`, `--bg2`,
`--chip`, `--glass`, `--nav`, `--text*`, `--accent*`, …). Three modes ship: **dark**,
**light**, and **seed** (derived from a single brand/team color).

## Using it

Map the tokens in `design-system.yaml` to your own CSS custom properties (or design-token
pipeline), then build components against the *roles* (surface ladder, text levels, accent,
semantic win/lose) rather than raw hex values.

## License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0
International License (CC BY-NC 4.0)**. Commercial use is not permitted.
See [`LICENSE`](LICENSE) · `SPDX-License-Identifier: CC-BY-NC-4.0`
