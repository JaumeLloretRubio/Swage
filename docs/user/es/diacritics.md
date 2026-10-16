# Letras acentuadas

*[English](../en/diacritics.md) · [Índice de la guía](index.md)*

Una letra acentuada es una **base** más un **signo**, guardados como dos
**componentes**: la *á* es una referencia a la *a* y otra al *agudo*, colocadas por
**anclas**. Cambias la *a* y la *á* la sigue.

## Crear letras acentuadas

**Glifo → Crear letras acentuadas…** trabaja con el **juego de caracteres** de la
fuente (elegido en el asistente o en **Cobertura**). Con un resumen antes, crea:

1. los **signos** ´ ` ¨ ˜ ¸, en versión de minúscula y en una versión `.case` más
   aplanada para las mayúsculas;
2. la **ı** sin punto, la **ŀ** y el punto volado;
3. los **compuestos** que necesitan los idiomas del juego (á é í ó ú à è ò ü ï ñ ç y
   sus mayúsculas…), con los componentes colocados por anclas.

Respeta los glifos manuales y desacoplados. Los juegos de caracteres salen de Unicode
CLDR: latín básico, Europa occidental, español, catalán/valenciano, portugués,
francés, alemán, italiano, inglés.

## Anclas

La base lleva `top` (y `bottom` para la cedilla); el signo lleva `_top` (o
`_bottom`). El compuesto pone cada `_top` sobre el `top` de la base. Las letras con
receta reciben sus anclas solas. En un glifo manual, **Añadir ancla** crea una;
muévela con el ratón o escribe su posición en el Inspector.

## Parámetros de los signos

| Parámetro          | Qué fija                                                         |
| ------------------ | ---------------------------------------------------------------- |
| peso de los signos | Grosor de los signos respecto al asta                            |
| hueco minúscula    | Distancia entre la altura x y el signo (vinculada al punto de la i) |
| hueco mayúscula    | Distancia entre la altura de mayúscula y el signo                |
| aplanado en mayúscula | Cuánto se aplanan los signos `.case`                          |
| ángulo y largo del agudo | Inclinación y largo del agudo y el grave                   |
| virgulilla (forma, ancho, alto) | Virgulilla quebrada u ondulada, y su tamaño         |
| tamaño y separación de la diéresis | Tamaño del punto (× el de la i) y distancia entre puntos |
| cedilla (forma, largo, ancho) | Cedilla en punta o curva, y su tamaño                   |

Los avisos comprueban que los signos no pesen más que el asta ni sean demasiado
finos, que el hueco del acento case con el punto de la i y que las mayúsculas
acentuadas no suban tanto que choquen con la línea de arriba.

## Trabajar con componentes

- **Copiar glifo** + **Pegar como componente** añade una referencia al glifo copiado.
- **Ir a la base** (o doble clic) abre el glifo referenciado.
- **Descomponer** convierte los componentes en contornos: el glifo deja de seguir a
  su base.
- Los signos están también como **piezas** en **Nuevo contorno…** para dibujarlos
  dentro de un glifo manual.
