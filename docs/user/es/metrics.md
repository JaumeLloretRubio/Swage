# Métricas

*[English](../en/metrics.md) · [Índice de la guía](index.md)*

Las métricas son las líneas horizontales contra las que se dibuja cada letra. Viven
en el área **Métricas** y se pintan en el lienzo.

| Métrica             | Qué es                                                           |
| ------------------- | ---------------------------------------------------------------- |
| UPM                 | Unidades por em: el tamaño de la rejilla (normalmente 1000)      |
| Línea base          | Donde se apoyan las letras, y = 0                                |
| Altura x            | Altura de las minúsculas sin ascendente (x, n, o)                |
| Altura de mayúscula | Altura de las mayúsculas planas (H)                              |
| Ascendente          | Altura de b, d, h, k, l                                          |
| Descendente         | Profundidad de p, q, g, j, y (negativa)                          |
| Avance mono         | En una fuente monoespaciada, el ancho de la celda que comparten todos los glifos |

## Overshoot

Una letra redonda que solo toca la altura x parece más pequeña que una plana. Por
eso las curvas **sobresalen** un poco de las líneas: por encima de la altura x y por
debajo de la base. *overshoot* fija cuánto en las minúsculas, y *capOvershoot* en O,
Q, C, G y las cifras. El lienzo muestra las zonas de overshoot.

## Cambiar una métrica

Cambia un valor en el área Métricas y todos los glifos acoplados se reconstruyen con
las líneas nuevas. Como cualquier cambio de parámetros, se puede deshacer en toda la
fuente (**Deshacer parámetros**). Los glifos desacoplados y manuales no se mueven:
revísalos en la tira de texto.

## Métricas verticales para exportar

Las métricas de arriba describen el diseño. El archivo exportado necesita además
métricas de interlineado (hhea, OS/2 typo y win), que se calculan a partir de ellas.
Ver [Exportar e instalar](production.md#métricas-verticales).
