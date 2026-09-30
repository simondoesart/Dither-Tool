# Shape Dither

A browser-based dithering tool for Avalanche / Ava Labs creative work.

## Modes

- **Shapes** — sample image/video on a grid and replace each cell with one of 7 user-uploadable SVGs (shadow → highlight), with per-shape color + alpha and midtone-driven scaling.
- **Bars** — fixed-axis bar dither with adjustable thickness, gap, floor/ceiling clamps, and audio reactivity (amplitude or per-column FFT spectrum) for music-reactive output.

## Inputs

- Image (PNG, JPG, etc.) or video (MP4, MOV, WebM)
- Audio (MP3, WAV) for Bars mode
- Custom SVGs for shape slots
- Paste from clipboard (e.g. Figma `⌘⇧C` Copy as PNG)

## Outputs

- Single PNG (current frame, with alpha)
- PNG sequence as a `.zip` — drops directly into After Effects as a footage sequence with alpha

## Running

It's a single self-contained HTML file. Either:

1. **Hosted** — open the deployed URL.
2. **Local** — open `index.html` in a modern browser (Chrome, Safari, Arc, Edge).

No build step, no dependencies, no server.

## Tech

Vanilla JS + Canvas 2D + Web Audio API + MediaRecorder. ~1300 lines, all in one file.
