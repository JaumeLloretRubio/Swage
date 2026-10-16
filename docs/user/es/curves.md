# Curvas

*[English](../en/curves.md) · [Índice de la guía](index.md)*

Los contornos están hechos de **curvas de Bézier cúbicas**: nodos sobre el contorno y
dos tiradores por cada tramo curvo.

| Elemento       | Qué es                                                              |
| -------------- | ------------------------------------------------------------------- |
| Nodo esquina   | Un punto donde la dirección cambia                                  |
| Nodo suave     | Un nodo con los tiradores alineados: la curva sigue sin quiebro     |
| Tirador        | Controla la tensión del tramo                                       |
| Contorno       | Un trazado cerrado; una letra tiene uno o varios                    |

Pon nodos en los **extremos** de cada curva (lo más a la izquierda, a la derecha,
arriba y abajo), con tiradores horizontales o verticales. Así las fuentes se ven y
se ajustan mejor. El área Problemas avisa de un extremo sin nodo o de un tirador
inclinado, y ofrece **añadir extremos** como arreglo.

## Tensión

La **tensión** es el largo de los tiradores respecto a la curva. 0,552 dibuja un
círculo; más es más cuadrada, menos, más redonda.

- *tensión exterior*: tiradores del contorno exterior de la o y de las demás curvas.
- *tensión interior*: tiradores de la contraforma. Suele ser algo mayor que la
  exterior para que el blanco de dentro no se vea en punta.

El Inspector muestra la tensión del tramo seleccionado y deja escribirla.

## El editor de puntos

Desacopla un glifo (o crea uno manual) para editarlo a mano.

| Herramienta  | Tecla | Uso                                                                |
| ------------ | ----- | ------------------------------------------------------------------ |
| Seleccionar  | V     | Pulsa un punto; pulsa dentro de un contorno para seleccionarlo entero (objeto) |
| Pluma        | P     | Clic = nodo esquina · arrastrar = nodo suave · clic en el primero = cerrar · Esc = dejar abierto |
| Espejo       | M     | Clic = colocar el eje · Intro = reflejar · Alt+Intro = copia reflejada |

- **Objetos**: un contorno seleccionado tiene caja con tiradores para mover, escalar y
  girar.
- **Simetría viva**: editas una mitad y la otra la sigue.
- **Booleanas**: unir, restar, intersecar, fusionar solapes.
- **Alinear y distribuir** nodos o contornos; **centrar** el glifo o la selección.
- **Guías**: al arrastrar, engancha a nodos, líneas de métricas, 0, el avance y el
  centro.
- **Coordenadas enteras** (opción del área Métricas): los puntos nuevos y movidos se
  redondean a unidades enteras. **Redondear glifo** redondea uno ya hecho.
- **Relleno / Contorno** alterna entre la letra rellena y su contorno con nodos.
- **R** muestra detrás del glifo las siluetas de las fuentes de referencia.
