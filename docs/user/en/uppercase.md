# Uppercase

*[Español](../es/uppercase.md) · [Guide index](index.md)*

**Glyph → Create uppercase from recipes (all 26)…** creates the missing capitals and
updates the coupled ones, with a summary first.

## The cap scale

Capitals are not scaled lowercase. Their stems are a little thicker so they do not
look light next to the lowercase, while their horizontals barely change:

| Derived value          | Formula                                                     |
| ---------------------- | ----------------------------------------------------------- |
| cap stem               | stem × *capStemFactor*                                      |
| cap curved side        | curved side × *capStemFactor*                               |
| cap curved horizontals | curved horizontals × (1 + (factor − 1) / 2)                 |

*capOvershoot* sets how far O, Q, C, G go beyond the cap height and the baseline;
*capSerif* and *capISerif* the serif overhangs.

## Build order

1. **H** and **O**: the straight and the round control capitals.
2. **I, L, E, F, T, D**: stems and arms (*armThickness*, *armSpur*).
3. **Q, C, G**: the O family (Q tail, C/G aperture, G jaw).
4. **A, V, W, X, Y, K, M, N, Z**: diagonals.
5. **B, P, R, S, U, J**: bowls, the S and the hooks.

Check the capitals in words with the lowercase (*Hamburgefonstiv*, *HHOHOO*): the
**Rhythm** area compares the white between serifs of HH with that of nn.

## Linked pieces

**Glyph → New contour…** has a **Pieces** tab with parametric parts: stem, bar,
diagonal, curve, half O, hook, serif, bracket, corner, spur and dot. A piece is
placed by snapping to nodes and stems, stays **linked** to the parameters (dashed
outline) and appears in the Inspector with its own values. Use them to build a
capital the recipes do not cover; **Convert to a regular contour** frees it.
