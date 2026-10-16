# Swage

**A type forge from [The Font Armory](https://the-font-armory.pages.dev).**

A parametric type design editor for the desktop. You describe a typeface with a few
dozen measurements (stem thickness, x-height, overshoot, serif length…) and recipes
build the letters from them. Change a value and every letter that uses it follows.
Then take any glyph out of the system and draw it by hand.

> **Experimental.** Swage is in early development. This repository only holds the
> installers and the user guide; the source code is not public yet.

![Spacing layout: font band, text strip, canvas, rhythm table and kerning](docs/user/img/en-kerning.png)

## Download

Get the latest build from [Releases](https://github.com/JaumeLloretRubio/Swage/releases/latest).

| Platform            | File                                                            |
| ------------------- | --------------------------------------------------------------- |
| Windows 10/11 (x64) | `Swage_<version>_windows-x64-setup.exe` (recommended) or `.msi` |

Optional, for OTF export: Python 3 with `pip install fonttools`.

## What it does

- **Parameters and recipes** for a–z, A–Z, figures, punctuation and accented letters.
- **Point editor** with pen, booleans, mirror and live symmetry, and parametric pieces.
- **Accented letters** from components and anchors, for the character set you choose.
- **Spacing and kerning**: monospaced or proportional, rhythm table, kerning classes.
- **Checks**: problems, coverage, review of every glyph, printable proof sheet.
- **Export** TTF, OTF and WOFF2, and install the font for your user to test it.
- Fonts are **UFO 3** folders; import OTF/TTF. English and Spanish interface.

## Documentation

User guide: [English](docs/user/en/index.md) · [Español](docs/user/es/index.md). It is
also what **Help → Documentation** and **F1** open from the app.

## Notes

- Builds are experimental: keep copies of your fonts.
- The installers are not code signed, so Windows SmartScreen may show a warning. Click
  "More info" and then "Run anyway".
- Found a problem? **Help → Report a problem…** in the app opens an
  [issue](https://github.com/JaumeLloretRubio/Swage/issues) with the version and system
  filled in.
- **The fonts you make with Swage are yours**: sell them, license them, use them for
  anything.

---

## Español

**Una forja tipográfica de [The Font Armory](https://the-font-armory.pages.dev/es/).**

Un editor de tipografías paramétrico para escritorio. Describes una tipografía con unas
decenas de medidas (grosor del asta, altura de x, overshoot, largo del remate…) y las
recetas construyen las letras a partir de ellas. Cambias un valor y todas las letras
que lo usan lo siguen. Después puedes sacar cualquier glifo del sistema y dibujarlo a
mano.

> **Experimental.** Swage está en una fase temprana. Este repositorio solo contiene los
> instaladores y la guía de usuario; el código todavía no es público.

**Descarga:** última versión en [Releases](https://github.com/JaumeLloretRubio/Swage/releases/latest).
En Windows, el `setup.exe` (o el `.msi`). Para exportar OTF hace falta Python 3 con
`pip install fonttools`.

**Guía de usuario:** [docs/user/es](docs/user/es/index.md).

Son versiones experimentales (guarda copias de tus fuentes) y no están firmadas: Windows
puede mostrar el aviso de SmartScreen ("Más información" y luego "Ejecutar de todas
formas"). Para avisar de un fallo, **Ayuda → Informar de un problema…** abre un
[issue](https://github.com/JaumeLloretRubio/Swage/issues).

**Las fuentes que hagas con Swage son tuyas**: puedes venderlas, licenciarlas y usarlas
para lo que quieras.
