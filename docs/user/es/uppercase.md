# Mayúsculas

*[English](../en/uppercase.md) · [Índice de la guía](index.md)*

**Glifo → Crear mayúsculas con receta (las 26)…** crea las mayúsculas que faltan y
actualiza las acopladas, con un resumen antes.

## La escala de mayúscula

Las mayúsculas no son minúsculas escaladas. Sus astas son algo más gruesas para que no
se vean ligeras junto a las minúsculas, mientras que sus horizontales casi no cambian:

| Valor derivado                  | Cuenta                                                   |
| ------------------------------- | -------------------------------------------------------- |
| asta mayúscula                  | asta × *capStemFactor*                                   |
| lado curvo mayúscula            | lado curvo × *capStemFactor*                             |
| horizontales curvas mayúscula   | horizontales curvas × (1 + (factor − 1) / 2)             |

*capOvershoot* fija cuánto sobresalen O, Q, C, G de la altura de mayúscula y de la
base; *capSerif* y *capISerif*, los vuelos de los remates.

## Orden de construcción

1. **H** y **O**: las mayúsculas de control, recta y redonda.
2. **I, L, E, F, T, D**: astas y brazos (*grosor de brazos*, *picos de brazo*).
3. **Q, C, G**: la familia de la O (cola de la Q, apertura de C y G, mandíbula de la G).
4. **A, V, W, X, Y, K, M, N, Z**: diagonales.
5. **B, P, R, S, U, J**: panzas, la S y los ganchos.

Mira las mayúsculas en palabras junto a las minúsculas (*Hamburgefonstiv*,
*HHOHOO*): el área **Ritmo** compara el blanco entre remates de HH con el de nn.

## Piezas vinculadas

**Glifo → Nuevo contorno…** tiene una pestaña **Piezas** con partes paramétricas:
asta, barra, diagonal, curva, media O, gancho, remate, ménsula, esquina, pico y punto.
Una pieza se coloca enganchándola a nodos y astas, sigue **vinculada** a los
parámetros (contorno discontinuo) y aparece en el Inspector con sus propios valores.
Úsalas para construir una mayúscula que las recetas no cubren; **Convertir en
contorno normal** la libera.
