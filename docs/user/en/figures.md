# Figures

*[Español](../es/figures.md) · [Guide index](index.md)*

**Glyph → Create figures…** creates 0–9 and **zero.alt** (the zero without a mark)
from recipes, with a summary first. The figures are **tabular**: all ten share one
advance, so columns of numbers align.

## The figure scale

Figures sit between lowercase and capitals: as tall as the capitals or a little less,
and usually a little lighter.

| Parameter      | What it sets                                                          |
| -------------- | --------------------------------------------------------------------- |
| figHeight      | Height of the figures (linked to the cap height)                      |
| figStemFactor  | Stem thickness relative to the stem (curves follow with half of it)   |
| figWidth       | Common drawing width                                                  |
| figAdvance     | Common advance in a proportional font                                 |
| figAperture    | Terminal aperture of 2 3 5 6 9 (linked to the c)                      |
| figTerminal    | Cut of the terminals: like the letters, or its own                    |
| figSerifs      | With serifs (feet on 1 and 4, spurs on terminals) or sans figures     |

## Each figure

| Figure | Parameters                                                       |
| ------ | ---------------------------------------------------------------- |
| 0      | zeroWidth, zeroTension, zeroMark (dot, diagonal bar or none)     |
| 1      | oneFoot, oneFlag, oneOffset                                      |
| 3, 8   | figJoin (height of the join), figUpper (upper bowl × lower)      |
| 4      | fourBar                                                          |
| 5      | fiveBowl                                                         |
| 6, 9   | sixBowl (the 9 is the 6 rotated)                                 |
| 7      | sevenFoot                                                        |

The marked zero tells 0 from O, which matters in code. **zero.alt** keeps the plain
zero; the warnings check that it is still narrower and squarer than the O.

## Pieces for figures

**New contour…** adds three pieces: **open bowl** (a ring with the font's terminal),
**double bowl** (two stacked rings, as in 3 and 8) and **zero mark**. The **Rhythm**
area measures the white with *00* as control.
