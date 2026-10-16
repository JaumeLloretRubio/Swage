# Cifras

*[English](../en/figures.md) · [Índice de la guía](index.md)*

**Glifo → Crear cifras…** crea 0–9 y **zero.alt** (el cero sin marca) con receta, con
un resumen antes. Las cifras son **tabulares**: las diez comparten avance, así que las
columnas de números quedan alineadas.

## La escala de cifras

Las cifras quedan entre minúsculas y mayúsculas: tan altas como las mayúsculas o un
poco menos, y normalmente algo más ligeras.

| Parámetro             | Qué fija                                                          |
| --------------------- | ----------------------------------------------------------------- |
| altura de cifras      | Altura de las cifras (vinculada a la altura de mayúscula)         |
| asta de cifras        | Grosor del asta respecto al asta (las curvas la siguen a medias)  |
| ancho de cifras       | Ancho común del dibujo                                            |
| avance de las cifras  | Avance común en una fuente proporcional                           |
| apertura (2 3 5 6 9)  | Apertura de los terminales (vinculada a la de la c)               |
| corte de las cifras   | Corte de los terminales: como las letras, o uno propio            |
| remates de las cifras | Con remates (pies en 1 y 4, picos en los terminales) o cifras sin remates |

## Cada cifra

| Cifra | Parámetros                                                         |
| ----- | ------------------------------------------------------------------ |
| 0     | ancho, tensión y marca del 0 (punto, barra diagonal o nada)        |
| 1     | vuelo del pie, bandera, desplazamiento                             |
| 3, 8  | unión (altura), panza superior (× la inferior)                     |
| 4     | barra del 4                                                        |
| 5     | panza del 5                                                        |
| 6, 9  | panza del 6 (el 9 es el 6 girado)                                  |
| 7     | pie del 7                                                          |

El cero con marca distingue 0 de O, algo que importa en código. **zero.alt** conserva
el cero liso; los avisos comprueban que siga siendo más estrecho y más cuadrado que la
O.

## Piezas para cifras

**Nuevo contorno…** añade tres piezas: **panza abierta** (un anillo con el terminal de
la fuente), **doble panza** (dos anillos apilados, como en 3 y 8) y **marca del
cero**. El área **Ritmo** mide el blanco con *00* como control.
