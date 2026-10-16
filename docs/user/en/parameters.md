# Parameters and recipes

*[Español](../es/parameters.md) · [Guide index](index.md)*

The **Parameters** area lists every measurement of the font, in groups. Select a
parameter to see in the canvas and the strip which glyphs it affects; hover it for
what it does and why.

## The core measurements

Almost everything derives from a few of them. Set these first, looking at *n*, *o*
and *H* in the text strip:

| Parameter                | What it sets                                                         |
| ------------------------ | -------------------------------------------------------------------- |
| stem                     | Thickness of the lowercase vertical stems; most other values follow it |
| bar                      | Thickness of straight horizontals (H, f, t, arms)                    |
| curved side              | Thickness of the sides of o and every curve (a bit more than stem)   |
| curved horizontals       | Thickness at the top and bottom of o: the contrast                   |
| n width / o width        | The rhythm of the lowercase (the o a little wider than the n)        |
| arch depth, top thickness, shoulder drop | The shape of the n arch                              |
| H width                  | The rhythm of the capitals                                           |
| serif, foot overhangs, flag | Slab serifs: thickness and how far they stick out                 |
| corners, junction        | Corner shape of serifs (straight, chamfer, superellipse) and how they join the stem (none, bracket, notch) |
| dot shape, size, rotation, gap | The dot of i and j, reused by punctuation and marks            |

Derived values (cap stem, figure stem…) are shown read-only with their formula.

## Values, expressions and links

Type a number or an **expression**: `stem * 1.05`, `round(nWidth * 0.62)`. Both `,`
and `.` are accepted as decimal separators; inside a function, separate arguments
with “, ” (comma and space) or `;`. Available functions: `min`, `max`, `round`.
**Formula and links** links a parameter
to another so it follows it; the Inspector shows the chain.

A **suggestion** appears when an optical rule disagrees with the value (for example,
curves thinner than stems); **Apply suggestion** sets it.

## Local adjustments

**Only in this glyph** gives the open glyph its own value of a parameter. It wins
over the font's value only there and survives recoupling. **Reset to the font**
removes all of a glyph's local adjustments.

## Undo for the whole font

Parameter changes have their own history: **Undo parameters** / **Redo parameters**
revert a change in every glyph at once, apart from the per-glyph undo of the canvas.

## A/B sets and pasting values

- **A/B sets** keep two versions of the parameters; switch in the text strip to
  compare them in words.
- **Paste values…** reads a list `name = value` (or `id = value`) copied from notes,
  another font or a table, and shows what will change before applying it.

## Creating glyphs from recipes

**New glyph** creates an empty glyph or one from a recipe. The bulk commands
(*Create lowercase*, *Create uppercase*, *Create figures*, *Create punctuation and
symbols*, *Create accented letters*) show a summary first: what is created, what is
updated and what is left alone. Manual and decoupled glyphs are never overwritten.
