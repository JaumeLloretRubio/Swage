# Concepts

*[Español](../es/concepts.md) · [Guide index](index.md)*

## Font units

Every measurement is in **font units**, with y going up from the baseline. The
**UPM** (units per em, usually 1000) is the size of the grid. Nothing in the font
is stored in pixels. See [Metrics](metrics.md).

## Parameters

A **parameter** is a named measurement shared by many letters: *stem*, *curved
side*, *n width*, *overshoot*, *serif thickness*… Some are numbers, some are
choices (a single- or double-story a, the shape of the dot). A value can be:

- a number;
- an **expression** that uses other parameters (`stem * 1.05`);
- a **link** to another parameter (it follows it).

A glyph can have a **local adjustment**: its own value of a parameter, which wins
over the font's value only in that glyph. See [Parameters and recipes](parameters.md).

## Recipes, coupled and decoupled glyphs

A **recipe** is the program that builds one glyph from the parameters. A glyph with
its recipe is **coupled**: change a parameter and it is rebuilt.

When a recipe is not enough, **decouple** the glyph. Its outline becomes ordinary
contours you edit by hand, and parameters no longer touch it. The recipe is kept:
**Recouple** rebuilds the glyph and discards the manual edits (it can be undone).

Bulk actions such as *Create lowercase from recipes* always show a **summary**
first and never overwrite manual or decoupled glyphs.

A glyph without a recipe (drawn from scratch or imported) is **manual**.

## Pieces

**Pieces** are parametric parts you add with **Glyph → New contour…**: stem, bar,
diagonal, curve, half O, hook, serif, bracket, corner, spur, dot, marks, bowls,
comma, angle, parenthesis. A piece stays **linked**: it is drawn with a dashed
outline and follows the parameters, like a small recipe inside a manual glyph.
**Convert to a regular contour** breaks the link.

## Components and anchors

A **component** is a reference to another glyph: *á* is the *a* plus the acute
mark. If the base changes, every glyph that uses it changes. **Anchors** (`top`,
`bottom`, and `_top`, `_bottom` on the marks) say where the mark goes. **Decompose**
turns components into contours. See [Accented letters](diacritics.md).

## Areas and layouts

The window is a set of **areas**:

| Area        | What it is for                                                  |
| ----------- | --------------------------------------------------------------- |
| Font band   | All glyphs, by folder; click to open                            |
| Canvas      | Draw and edit one glyph                                         |
| Parameters  | The font's measurements, grouped                                |
| Inspector   | The selected glyph, node, contour, component or the font        |
| Text strip  | Words at several sizes, test texts, kerning in place            |
| Metrics     | The vertical metrics of the font                                |
| Rhythm      | The white between letters, measured                             |
| Kerning     | Pairs and classes                                               |
| Compare     | Your glyph against reference fonts                              |
| Problems    | Errors and warnings, with a fix when there is one               |
| Guide       | Reserved for guided content                                     |

Every area can be split, tabbed, maximized or made floating from its menu (the ▾
next to its title). A **layout** is a saved arrangement of areas; save your own with
**+ save**.

## Folders

The font band groups glyphs in **folders**: smart ones (lowercase, uppercase,
accented, figures, punctuation, symbols, marks, to fix…) and your own. Folders are
saved in the UFO.

## The UFO

A font is a **UFO 3** folder: an open format that other editors (Glyphs, FontLab,
RoboFont, Fontra…) read. Parameters, recipes and settings are stored in the UFO's
`lib`, so nothing is lost if you open the font elsewhere. Opening a font never
modifies it; only saving does.
