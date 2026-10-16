# Lowercase

*[Español](../es/lowercase.md) · [Guide index](index.md)*

**Glyph → Create lowercase from recipes…** creates the missing a–z (and H, the
control capital) and updates the coupled ones, with a summary first.

## Build order

The lowercase grows from a few control letters. Tune them first, in this order, and
look at them in words in the text strip:

1. **n** and **o**: stem, curves, widths, the arch. Everything else derives from
   them.
2. **h, u, m, l, i**: the n's family (the m with its own width and stem factor).
3. **c, e, s, a, b, d, p, q**: open curves, terminals and bowls.
4. **v, w, x, y, k, z**: diagonals.
5. **f, t, r, j, g**: hooks, ears and the descending hook.

## Parameter groups

| Group             | Parameters                                                                  |
| ----------------- | --------------------------------------------------------------------------- |
| Terminals         | terminal type (horizontal, vertical, oblique), aperture, beak and its length |
| c, e              | c/e width, e bar height and thickness, e aperture relative to the c         |
| s                 | width, top/bottom balance, spine weight                                     |
| a                 | single- or double-story; width, bowl, tension, stem, top serif, foot         |
| b, d, p, q        | bowl width, join drop                                                       |
| Diagonals         | diagonal weight, vertex (truncated or pointed), vertex overshoot            |
| v, w, x, y, k, z  | widths, w middle vertex and stroke, x crossing, k join, z spurs             |
| f, t, r, j        | hook radius, f/t bar overhangs, t height, r ear and foot, offsets           |
| g                 | bowl width (follows the a), tension, stem, offset; hook depth shared with j  |

Diagonals are drawn with a **perpendicular** thickness (stem × diagonal weight): the
horizontal width shown in the Inspector is thickness / cos(angle).

## Warnings

Parameter values are checked against optical rules, and the warning says why and
with which numbers: an x crossing below the center (the x seems to sink), a t as tall
as the ascender (confused with the l), a notch too deep for its serif (the serif looks
detached). Warnings never block anything; they are advice.
