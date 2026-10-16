# Metrics

*[Español](../es/metrics.md) · [Guide index](index.md)*

Metrics are the horizontal lines every letter is drawn against. They live in the
**Metrics** area and are drawn in the canvas.

| Metric         | What it is                                                         |
| -------------- | ------------------------------------------------------------------ |
| UPM            | Units per em: the size of the font's grid (usually 1000)           |
| Baseline       | Where letters sit, y = 0                                           |
| x-height       | Height of lowercase letters without ascenders (x, n, o)            |
| Cap height     | Height of flat capitals (H)                                        |
| Ascender       | Height of b, d, h, k, l                                            |
| Descender      | Depth of p, q, g, j, y (negative)                                  |
| Mono advance   | In a monospaced font, the width of the cell all glyphs share       |

## Overshoot

A round letter that only touches the x-height looks smaller than a flat one. Curves
therefore go a little **beyond** the lines: above the x-height and below the
baseline. *overshoot* sets how much for lowercase, *capOvershoot* for O, Q, C, G and
the figures. The canvas shows the overshoot zones.

## Changing a metric

Change a value in the Metrics area and every coupled glyph is rebuilt to the new
lines. Like any parameter change it can be undone across the whole font
(**Undo parameters**). Decoupled and manual glyphs are not moved: check them in the
text strip.

## Vertical metrics for export

The metrics above describe the design. The exported file also needs line-spacing
metrics (hhea, OS/2 typo and win), computed from them. See
[Export and install](production.md#vertical-metrics).
