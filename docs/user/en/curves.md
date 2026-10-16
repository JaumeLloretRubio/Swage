# Curves

*[Español](../es/curves.md) · [Guide index](index.md)*

Outlines are made of **cubic Bézier curves**: nodes on the contour and two handles
per curve segment.

| Element      | What it is                                                         |
| ------------ | ------------------------------------------------------------------ |
| Corner node  | A point where the direction changes                                |
| Smooth node  | A node with aligned handles: the curve continues without a kink    |
| Handle       | Controls the segment's tension                                     |
| Contour      | A closed path; a letter has one or more                            |

Put nodes at the **extremes** of each curve (leftmost, rightmost, top, bottom), with
horizontal or vertical handles. Fonts render and hint better that way. The Problems
area warns about an extreme without a node or a tilted handle, and offers **add
extremes** as a fix.

## Tension

**Tension** is the length of the handles relative to the curve. 0.552 draws a
circle; more is squarer, less is rounder.

- *outerTension*: handles of the outer contour of o and the other curves.
- *innerTension*: handles of the counter. It is usually a little higher than the
  outer one so the white inside does not look pointed.

The Inspector shows the tension of a selected segment and lets you type it.

## The point editor

Decouple a glyph (or create a manual one) to edit it by hand.

| Tool        | Key | Use                                                                 |
| ----------- | --- | ------------------------------------------------------------------- |
| Select      | V   | Click a point; click inside a contour to select it whole (object)   |
| Pen         | P   | Click = corner node · drag = smooth node · click the first = close · Esc = leave open |
| Mirror      | M   | Click = place the axis · Enter = reflect · Alt+Enter = reflected copy |

- **Objects**: a selected contour has a box with handles to move, scale and rotate.
- **Live symmetry**: edit one half and the other follows.
- **Booleans**: union, subtract, intersect, merge overlaps.
- **Align and distribute** nodes or contours; **center** the glyph or the selection.
- **Guides**: while dragging, snaps to nodes, metric lines, 0, the advance and the
  center.
- **Integer coordinates** (option in the Metrics area): new and moved points round to
  whole units. **Round glyph** rounds an existing one.
- **Fill / Outline** switches between the filled letter and its outline with nodes.
- **R** shows the silhouettes of the reference fonts behind the glyph.
