# Conceptos

*[English](../en/concepts.md) · [Índice de la guía](index.md)*

## Unidades de fuente

Todas las medidas están en **unidades de fuente**, con la y hacia arriba desde la
línea base. Las **UPM** (unidades por em, normalmente 1000) son el tamaño de la
rejilla. Nada de la fuente se guarda en píxeles. Ver [Métricas](metrics.md).

## Parámetros

Un **parámetro** es una medida con nombre que comparten muchas letras: *asta*, *lado
curvo*, *ancho de la n*, *overshoot*, *grosor del remate*… Unos son números y otros
opciones (la a de uno o dos pisos, la forma del punto). Un valor puede ser:

- un número;
- una **cuenta** que usa otros parámetros (`stem * 1.05`);
- un **vínculo** a otro parámetro (lo sigue).

Un glifo puede tener un **ajuste local**: su propio valor de un parámetro, que manda
sobre el de la fuente solo en ese glifo. Ver [Parámetros y recetas](parameters.md).

## Recetas, glifos acoplados y desacoplados

Una **receta** es el programa que construye un glifo a partir de los parámetros. Un
glifo con su receta está **acoplado**: cambias un parámetro y se reconstruye.

Cuando una receta no basta, **desacopla** el glifo. Su contorno pasa a ser contornos
normales que editas a mano, y los parámetros dejan de tocarlo. La receta se guarda:
**Reacoplar** reconstruye el glifo y descarta lo editado a mano (se puede deshacer).

Las acciones masivas, como *Crear minúsculas con receta*, muestran siempre un
**resumen** antes y nunca machacan los glifos manuales ni los desacoplados.

Un glifo sin receta (dibujado desde cero o importado) es **manual**.

## Piezas

Las **piezas** son partes paramétricas que añades con **Glifo → Nuevo contorno…**:
asta, barra, diagonal, curva, media O, gancho, remate, ménsula, esquina, pico, punto,
signos, panzas, coma, ángulo, paréntesis. Una pieza sigue **vinculada**: se dibuja
con contorno discontinuo y sigue a los parámetros, como una receta pequeña dentro de
un glifo manual. **Convertir en contorno normal** rompe el vínculo.

## Componentes y anclas

Un **componente** es una referencia a otro glifo: la *á* es la *a* más el signo
agudo. Si la base cambia, cambian todos los glifos que la usan. Las **anclas** (`top`,
`bottom`, y `_top`, `_bottom` en los signos) dicen dónde va el signo.
**Descomponer** convierte los componentes en contornos. Ver
[Letras acentuadas](diacritics.md).

## Áreas y disposiciones

La ventana es un conjunto de **áreas**:

| Área            | Para qué sirve                                                   |
| --------------- | ---------------------------------------------------------------- |
| Banda de fuente | Todos los glifos, por carpetas; pulsa uno para abrirlo           |
| Lienzo          | Dibujar y editar un glifo                                        |
| Parámetros      | Las medidas de la fuente, por grupos                             |
| Inspector       | El glifo, nodo, contorno o componente seleccionado, o la fuente  |
| Tira de texto   | Palabras a varios tamaños, textos de prueba, kerning en el sitio |
| Métricas        | Las métricas verticales de la fuente                             |
| Ritmo           | El blanco entre letras, medido                                   |
| Kerning         | Pares y clases                                                   |
| Comparar        | Tu glifo frente a fuentes de referencia                          |
| Problemas       | Errores y avisos, con arreglo cuando lo hay                      |
| Guía            | Reservada para contenido guiado                                  |

Cada área se puede dividir, poner en pestañas, maximizar o hacer flotante desde su
menú (el ▾ junto al título). Una **disposición** es una colocación de áreas
guardada; guarda las tuyas con **+ guardar**.

## Carpetas

La banda de fuente agrupa los glifos en **carpetas**: inteligentes (minúsculas,
mayúsculas, acentuadas, cifras, puntuación, símbolos, signos, a corregir…) y las
tuyas. Las carpetas se guardan en el UFO.

## El UFO

Una fuente es una carpeta **UFO 3**: un formato abierto que leen otros editores
(Glyphs, FontLab, RoboFont, Fontra…). Los parámetros, las recetas y los ajustes se
guardan en el `lib` del UFO, así que no se pierde nada si abres la fuente en otro
sitio. Abrir una fuente nunca la modifica; solo guardar.
