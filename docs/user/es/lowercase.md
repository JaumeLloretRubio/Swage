# Minúsculas

*[English](../en/lowercase.md) · [Índice de la guía](index.md)*

**Glifo → Crear minúsculas con receta…** crea las a–z que faltan (y la H, la
mayúscula de control) y actualiza las acopladas, con un resumen antes.

## Orden de construcción

Las minúsculas crecen a partir de unas pocas letras de control. Ajústalas primero, en
este orden, y míralas en palabras en la tira de texto:

1. **n** y **o**: asta, curvas, anchos, el arco. Todo lo demás sale de ellas.
2. **h, u, m, l, i**: la familia de la n (la m con su propio ancho y factor de asta).
3. **c, e, s, a, b, d, p, q**: curvas abiertas, terminales y panzas.
4. **v, w, x, y, k, z**: diagonales.
5. **f, t, r, j, g**: ganchos, orejas y el gancho descendente.

## Grupos de parámetros

| Grupo            | Parámetros                                                                   |
| ---------------- | ---------------------------------------------------------------------------- |
| Terminales       | tipo de terminal (horizontal, vertical, oblicuo), apertura, pico y su largo |
| c, e             | ancho de c y e, altura y grosor de la barra de la e, apertura de la e respecto a la c |
| s                | ancho, equilibrio arriba/abajo, grosor del lomo                              |
| a                | de uno o dos pisos; ancho, panza, tensión, asta, remate de arriba, pie       |
| b, d, p, q       | ancho de la panza, caída de la unión                                         |
| Diagonales       | grosor de las diagonales, vértice (truncado o en punta), overshoot de la punta |
| v, w, x, y, k, z | anchos, vértice central y trazo de la w, cruce de la x, unión de la k, picos de la z |
| f, t, r, j       | radio del gancho, vuelos de la barra de f y t, altura de la t, oreja y pie de la r, desplazamientos |
| g                | ancho de la panza (sigue a la a), tensión, asta, desplazamiento; profundidad del gancho compartida con la j |

Las diagonales se dibujan con grosor **perpendicular** (asta × grosor de las
diagonales): el ancho horizontal que muestra el Inspector es grosor / cos(ángulo).

## Avisos

Los valores de los parámetros se comprueban con reglas ópticas, y el aviso dice por
qué y con qué números: un cruce de la x por debajo del centro (la x parece hundirse),
una t tan alta como el ascendente (se confunde con la l), una muesca demasiado honda
para su remate (el remate parece suelto). Los avisos no bloquean nada; son consejos.
