# Export and install

*[Español](../es/production.md) · [Guide index](index.md)*

Before a font leaves the editor: check that it is complete, that it has no errors,
that it is named, and that its lines are spaced correctly. Then export and test it
where it will be used.

## 1. Coverage

**Font → Coverage…** lists the characters of the **required set** (chosen in the
wizard, or here from the CLDR sets plus extra characters) with their state: missing,
recipe, decoupled, compound, manual, or with problems. **Create everything missing**
creates each one with its recipe, as a compound (base + mark by anchors) or as an
empty glyph to draw. The set is saved in the font.

## 2. Problems

The **Problems** area lists errors and warnings for the open glyph or the whole font:
contour directions, extremes without nodes, non-integer coordinates, duplicate nodes,
missing anchors… Many have a one-click fix. **Errors block export**; warnings are
accepted and listed in the export report.

## 3. Review all

**Review all** walks through the glyphs one by one between *HH*, *nn* and *00*. Mark
each ✓ reviewed (Enter) or ✗ to fix, with a note. The ✗ go to the *to fix* folder.

## 4. Proof sheet

**Proof sheet**: every glyph in a grid and the test texts (pangrams, control strings,
code, numbers) at 9, 12, 13, 16, 20, 36 and 72 px, with the export line spacing. Print
it, save it as PDF from the print dialog, or as PNG. **Compare with…** puts each line
under the same one set in an installed font. Look at it on paper: problems hide on
screen.

## 5. Font info

**Font → Font info…**: family, style, version, designer, year, license (SIL OFL 1.1,
all rights reserved, or other), URL, copyright and vendor ID, saved in
`fontinfo.plist`. In a monospaced font, saving also sets `isFixedPitch`, a monospaced
PANOSE and an installable `fsType`, so code editors list it as monospaced.

## Vertical metrics

**Font → Export metrics…** shows the three sets of line-spacing metrics a font file
carries:

| Set       | Who reads it                                     | Default                                                 |
| --------- | ------------------------------------------------ | ------------------------------------------------------- |
| OS/2 typo | Windows with USE_TYPO_METRICS, modern apps       | Design ascender and descender, lineGap for ≈ 1.25 em    |
| hhea      | macOS, Linux and browsers                        | Same as typo                                            |
| OS/2 win  | Windows, which clips what goes beyond it         | Highest and lowest point of all glyphs + 10 units       |

Two stacked lines preview the real line spacing. A typed value is saved and wins;
emptying the field returns to the computed value.

## 6. Export

**File → Export…** generates, in the folder you choose, `Family-Style.ttf`,
`.otf` and `.woff2`:

- **TTF** (quadratic outlines), compiled with fontc;
- **OTF** (CFF outlines), with Python and fontTools: `pip install fonttools`;
- **WOFF2**, the compressed web format.

Export works on a **copy**: your UFO is not touched. On the copy it decomposes what
the format requires, merges overlaps, rounds to integers, checks directions and
writes the vertical metrics. Anchors become GPOS `mark`; kerning becomes GPOS `kern`.
The **report** lists glyphs, sizes, metrics, accepted warnings and the validation.

Optional tools, used if they are on the PATH:

- **Hinting** with [ttfautohint](https://freetype.org/ttfautohint/): it fits the TTF
  outlines to the pixel grid at small sizes. On Windows, put `ttfautohint.exe` in a
  folder on the PATH and reopen Export. Without it the TTF relies on the system's
  smoothing, which is barely noticeable on high-resolution screens.
- **Validation** with fontspector (`cargo install fontspector`) or fontbakery
  (`pip install fontbakery`). Without them the app runs its own file check.

## 7. Test it

- **Test installed** installs the TTF **for your user only** (on Windows in
  `%LOCALAPPDATA%\Microsoft\Windows\Fonts`, no administrator needed). Restart the
  application where you want to use it. In a code editor such as Zed, set
  `"buffer_font_family": "<your family name>"` in its settings.
- **Browser test** opens a page next to the files with the WOFF2, the proof sheet
  texts and a box to type in.
