# Punctuation and symbols

*[Español](../es/punctuation.md) · [Guide index](index.md)*

**Glyph → Create punctuation and symbols…** creates the whole ASCII set from recipes,
plus what the character set's languages need: `. , ; : ! ¡ ? ¿ …`, quotes, dashes,
brackets, `+ − × ÷ = < > ~ ^ * # % $ € @ & ° º ª` and the spacing marks. Manual and
decoupled glyphs are respected.

## Shared measurements

Punctuation reuses the letters: the period is the i dot, the comma is the period with
a tail, the math signs sit on the e bar.

| Parameter                     | What it sets                                                  |
| ----------------------------- | ------------------------------------------------------------- |
| punctSize                     | Size of the dot of `. , : ; ! ? …` (× the i dot)              |
| punctTail, punctTailShape     | Tail of comma and quotes: length, straight or teardrop        |
| quoteStyle                    | Straight quotes `' "` as sticks or wedges                     |
| mathAxis                      | Center of `+ − × ÷ = < > ~` and the hyphens (≈ the e bar)     |
| mathWidth, mathWeight         | Width and thickness of the math signs                         |
| hyphenWidth, endashWidth, emdashWidth | The three dashes, clearly different                   |
| delimTop, delimBottom         | Where `( ) [ ] { } / \ \|` end (linked to ascender and descender) |
| parenDepth, bracketArm        | Curvature of `( )`, arms of `[ ]`                             |
| asteriskSpokes, asteriskHeight | 5 or 6 spokes; height (high, as in code)                     |
| dollarStem                    | The stem crosses the S or only sticks out                     |

## Approximations

Some symbols (`{ } @ &` among them) are built as approximations and marked **review
by hand**: they are a starting point. Decouple them and finish them in the point
editor.

## Pieces and test texts

**New contour…** adds **comma**, **angle** (`‹ › < > ^`) and **parenthesis** pieces.
The text strip has code texts (brackets, operators, `0O`, `1lI`) to check
punctuation where it matters most in a monospaced font.
