# Exportar e instalar

*[English](../en/production.md) · [Índice de la guía](index.md)*

Antes de que una fuente salga del editor: comprueba que está completa, que no tiene
errores, que tiene nombre y que sus líneas se espacian bien. Después, expórtala y
pruébala donde se vaya a usar.

## 1. Cobertura

**Fuente → Cobertura…** lista los caracteres del **juego requerido** (elegido en el
asistente o aquí, con los juegos CLDR más caracteres extra) con su estado: falta,
receta, desacoplado, compuesto, manual o con problemas. **Crear todo lo que falta**
crea cada uno con su receta, como compuesto (base + signo por anclas) o como glifo
vacío para dibujarlo. El juego se guarda en la fuente.

## 2. Problemas

El área **Problemas** lista errores y avisos del glifo abierto o de toda la fuente:
sentido de los contornos, extremos sin nodo, coordenadas no enteras, nodos
duplicados, anclas que faltan… Muchos tienen arreglo con un clic. **Los errores
bloquean la exportación**; los avisos se aceptan y quedan listados en el informe.

## 3. Revisar todo

**Revisar todo** recorre los glifos uno a uno entre *HH*, *nn* y *00*. Marca cada uno
✓ revisado (Intro) o ✗ a corregir, con una nota. Los ✗ van a la carpeta *a corregir*.

## 4. Hoja de pruebas

**Hoja de pruebas**: todos los glifos en cuadrícula y los textos de prueba (pangramas,
tiras de control, código, números) a 9, 12, 13, 16, 20, 36 y 72 px, con el
interlineado de exportación. Imprímela, guárdala como PDF desde el diálogo de
impresión o como PNG. **Comparar con…** pone cada línea debajo de la misma en una
fuente instalada. Mírala en papel: en pantalla los problemas se esconden.

## 5. Información de la fuente

**Fuente → Información de la fuente…**: familia, estilo, versión, diseñador, año,
licencia (SIL OFL 1.1, todos los derechos reservados u otra), URL, copyright e ID de
fabricante, guardados en `fontinfo.plist`. En una fuente monoespaciada, al guardar se
ponen además `isFixedPitch`, un PANOSE monoespaciado y un `fsType` instalable, para
que los editores de código la listen como monoespaciada.

## Métricas verticales

**Fuente → Métricas de exportación…** muestra los tres juegos de métricas de
interlineado que lleva un archivo de fuente:

| Juego     | Quién lo lee                                     | Por defecto                                               |
| --------- | ------------------------------------------------ | --------------------------------------------------------- |
| OS/2 typo | Windows con USE_TYPO_METRICS, apps modernas      | Ascendente y descendente del diseño, lineGap para ≈ 1,25 em |
| hhea      | macOS, Linux y navegadores                       | Igual que typo                                            |
| OS/2 win  | Windows, que recorta lo que se sale              | El punto más alto y más bajo de todos los glifos + 10 u   |

Dos líneas apiladas muestran el interlineado real. Un valor escrito se guarda y
manda; vaciar el campo vuelve al calculado.

## 6. Exportar

**Archivo → Exportar…** genera, en la carpeta que elijas, `Familia-Estilo.ttf`,
`.otf` y `.woff2`:

- **TTF** (contornos cuadráticos), compilado con fontc;
- **OTF** (contornos CFF), con Python y fontTools: `pip install fonttools`;
- **WOFF2**, el formato comprimido para web.

La exportación trabaja sobre una **copia**: tu UFO no se toca. En la copia descompone
lo que el formato exige, fusiona solapes, redondea a enteros, comprueba sentidos y
escribe las métricas verticales. Las anclas pasan a `mark` en GPOS; el kerning, a
`kern`. El **informe** da glifos, tamaños, métricas, avisos aceptados y la validación.

Herramientas opcionales, que se usan si están en el PATH:

- **Hinting** con [ttfautohint](https://freetype.org/ttfautohint/): ajusta los
  contornos del TTF a la rejilla de píxeles en tamaños pequeños. En Windows, pon
  `ttfautohint.exe` en una carpeta del PATH y vuelve a abrir Exportar. Sin él, el TTF
  se fía del suavizado del sistema, que en pantallas de alta resolución apenas se
  nota.
- **Validación** con fontspector (`cargo install fontspector`) o fontbakery
  (`pip install fontbakery`). Sin ellos, la app hace su propia comprobación del
  archivo.

## 7. Probarla

- **Probar instalada** instala el TTF **solo para tu usuario** (en Windows, en
  `%LOCALAPPDATA%\Microsoft\Windows\Fonts`, sin administrador). Reinicia la
  aplicación donde quieras usarla. En un editor de código como Zed, pon
  `"buffer_font_family": "<el nombre de tu familia>"` en sus ajustes.
- **Prueba en navegador** abre una página junto a los archivos con el WOFF2, los
  textos de la hoja de pruebas y una caja para escribir.
