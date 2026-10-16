# Parámetros y recetas

*[English](../en/parameters.md) · [Índice de la guía](index.md)*

El área **Parámetros** lista todas las medidas de la fuente, por grupos. Selecciona
un parámetro para ver en el lienzo y en la tira a qué glifos afecta; pasa el puntero
por encima para saber qué hace y para qué sirve.

## Las medidas base

Casi todo sale de unas pocas. Fíjalas primero, mirando la *n*, la *o* y la *H* en la
tira de texto:

| Parámetro                  | Qué fija                                                            |
| -------------------------- | ------------------------------------------------------------------- |
| asta                       | Grosor de las astas verticales de las minúsculas; casi todo lo demás la sigue |
| barra                      | Grosor de las horizontales rectas (H, f, t, brazos)                 |
| lado curvo                 | Grosor de los lados de la o y de todas las curvas (algo más que el asta) |
| horizontales curvas        | Grosor arriba y abajo de la o: el contraste                         |
| ancho de la n / de la o    | El ritmo de las minúsculas (la o algo más ancha que la n)           |
| profundidad del arco, grosor arriba, caída del hombro | La forma del arco de la n                |
| ancho de la H              | El ritmo de las mayúsculas                                          |
| remate, vuelos del pie, bandera | Remates de losa: grosor y cuánto sobresalen                    |
| esquinas, unión            | Forma de las esquinas de los remates (recta, bisel, superelipse) y cómo se unen al asta (sin unión, ménsula, muesca) |
| forma, tamaño, giro y separación del punto | El punto de la i y la j, que reutilizan la puntuación y los signos |

Los valores derivados (asta mayúscula, asta de cifras…) se muestran sin poder
editarlos, con su cuenta.

## Valores, cuentas y vínculos

Escribe un número o una **cuenta**: `stem * 1.05`, `round(nWidth * 0.62)`. Se
admiten `,` y `.` como separador decimal; dentro de una función, separa los
argumentos con «, » (coma y espacio) o con `;`. **Cuenta y vínculos** vincula un
parámetro a otro para que lo siga; el Inspector muestra la cadena.

Aparece una **sugerencia** cuando una regla óptica no está de acuerdo con el valor
(por ejemplo, curvas más finas que las astas); **Aplicar sugerencia** la pone.

## Ajustes locales

**Solo en este glifo** da al glifo abierto su propio valor de un parámetro. Manda
sobre el de la fuente solo ahí y sobrevive al reacoplar. **Restablecer a la fuente**
quita todos los ajustes locales de un glifo.

## Deshacer en toda la fuente

Los cambios de parámetros tienen su propio historial: **Deshacer parámetros** /
**Rehacer parámetros** revierten un cambio en todos los glifos a la vez, aparte del
deshacer por glifo del lienzo.

## Conjuntos A/B y pegar valores

- **Conjuntos A/B** guardan dos versiones de los parámetros; cambia de una a otra en
  la tira de texto para compararlas en palabras.
- **Pegar valores…** lee una lista `nombre = valor` (o `id = valor`) copiada de unas
  notas, de otra fuente o de una tabla, y enseña qué va a cambiar antes de aplicarlo.

## Crear glifos con receta

**Nuevo glifo** crea un glifo vacío o uno con receta. Las órdenes masivas (*Crear
minúsculas*, *Crear mayúsculas*, *Crear cifras*, *Crear puntuación y símbolos*,
*Crear letras acentuadas*) enseñan primero un resumen: qué se crea, qué se actualiza
y qué se deja como está. Los glifos manuales y desacoplados no se machacan nunca.
