# Accented letters

*[Español](../es/diacritics.md) · [Guide index](index.md)*

An accented letter is a **base** plus a **mark**, stored as two **components**: *á*
is a reference to *a* and a reference to *acute*, placed by **anchors**. Change the
*a* and the *á* follows.

## Create accented letters

**Glyph → Create accented letters…** works from the font's **character set** (chosen
in the wizard or in **Coverage**). With a summary first, it creates:

1. the **marks** ´ ` ¨ ˜ ¸, in a lowercase version and a flatter `.case` version for
   capitals;
2. the dotless **ı**, the **ŀ** and the middle dot;
3. the **compounds** the set's languages need (á é í ó ú à è ò ü ï ñ ç and their
   capitals…), with components placed by anchors.

Manual and decoupled glyphs are respected. Character sets come from Unicode CLDR:
basic Latin, Western Europe, Spanish, Catalan/Valencian, Portuguese, French, German,
Italian, English.

## Anchors

The base carries `top` (and `bottom` for the cedilla); the mark carries `_top` (or
`_bottom`). The compound puts each `_top` on the base's `top`. Recipe letters get
their anchors automatically. On a manual glyph, **Add anchor** creates one; move it
with the mouse or type its position in the Inspector.

## Mark parameters

| Parameter        | What it sets                                                      |
| ---------------- | ----------------------------------------------------------------- |
| markWeight       | Thickness of the marks relative to the stem                       |
| markGap          | Distance between the x-height and the mark (linked to the i dot)  |
| markCapGap       | Distance between the cap height and the mark                      |
| markCapFlatten   | How much the `.case` marks are flattened                          |
| acuteAngle, acuteLength | Slant and length of acute and grave                        |
| tildeShape, tildeWidth, tildeHeight | Broken or wavy tilde, and its size             |
| dieresisSize, dieresisGap | Dot size (× the i dot) and distance between dots         |
| cedillaShape, cedillaLength, cedillaWidth | Pointed or curved cedilla, and its size  |

The warnings check that marks are neither heavier than the stem nor too thin, that
the accent gap matches the i dot, and that accented capitals do not get too tall for
the line above.

## Working with components

- **Copy glyph** + **Paste as component** adds a reference to the copied glyph.
- **Go to base** (or double click) opens the referenced glyph.
- **Decompose** turns components into contours: the glyph stops following its base.
- Marks are also available as **pieces** in **New contour…** to draw them inside a
  manual glyph.
