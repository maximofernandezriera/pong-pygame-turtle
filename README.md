# Práctica: Desarrollo del juego Pong con Python

En esta práctica vamos a desarrollar desde cero el clásico juego Pong utilizando Python. El objetivo es aplicar lo que ya conocéis del lenguaje (variables, condicionales, bucles, funciones y clases) en un proyecto completo y visible: un videojuego funcional para dos jugadores en el mismo teclado.

## Carácter de la práctica

- La práctica es **voluntaria**: no tiene un peso porcentual directo en la nota.
- Cada alumno elige **una** de las dos opciones: **Pygame** o **turtle**.
- La valoración se realiza mediante una **entrevista personal**, en la que deberéis explicar vuestro código y las decisiones que habéis tomado. Me servirá para valorar vuestro progreso.

## Elección de librería

| | Opción A: Pygame | Opción B: turtle |
| --- | --- | --- |
| Instalación | `pip install pygame` | Ninguna: viene con Python |
| Guía de vídeos | Clear Code (español/inglés) | TokyoEdtech (en inglés) |
| Requisitos | Ver [Opción A](#opción-a-pong-con-pygame) | Ver [Opción B](#opción-b-pong-con-turtle) |

Los requisitos de cada opción son independientes y se valoran solo con los criterios de la opción elegida. En ambos casos el juego necesita una ventana gráfica, por lo que la práctica se trabaja en local: no se puede ejecutar en Google Colab.

---

## Opción A: Pong con Pygame

### Contexto

Desarrollaréis el juego con la librería Pygame. Como guía de trabajo seguiremos la lista de reproducción *Creating Pong in Pygame* del canal Clear Code, que construye el juego paso a paso. La lista sirve de referencia y apoyo: la práctica no consiste en copiar el código de los vídeos, sino en entender cada paso y escribir vuestra propia versión.

### Material de referencia

- Lista de reproducción: [Creating Pong in Pygame (Clear Code)](https://youtube.com/playlist?list=PL8ui5HK3oSiEk9HaKoVPxSZA03rmr9Z0k)
- Código del autor de los vídeos (referencia, no para entregar): [github.com/clear-code-projects/Pong_in_Pygame](https://github.com/clear-code-projects/Pong_in_Pygame)

| Vídeo | Contenido | Duración aprox. |
| --- | --- | --- |
| [1. Learning Pygame by making Pong](https://youtu.be/Qf3-aDXG8q4) | Ventana del juego, bucle principal, paletas, pelota, movimiento y colisiones básicas | 29 min |
| [2. Añadiendo marcador y cuenta atrás](https://youtu.be/E4Ih9mpn5tk) | Sistema de puntuación y temporizador de inicio de punto | 24 min |
| [3. Mejorando colisiones y añadiendo sonido](https://youtu.be/n1mKIK7lCx0) | Mecánicas de colisión más realistas y efectos de sonido | 11 min |
| [4. Reescribiendo el código con sprites](https://youtu.be/oOqdHBkA4rc) | Refactorización con sprites de Pygame y mejora del aspecto visual | 17 min |

### Requisitos técnicos

- Python 3 instalado en el equipo y la librería Pygame (`pip install pygame`).
- Un editor o entorno de desarrollo a vuestra elección (por ejemplo, VS Code).
- Importante: Pygame necesita una ventana gráfica, por lo que esta práctica se trabaja en local; no se puede ejecutar en Google Colab.

### Requisitos funcionales

El juego entregado debe cumplir, como mínimo, los siguientes requisitos, organizados en las mismas fases que los vídeos:

1. **Juego base.** Ventana de juego, dos paletas controladas por teclado (una por jugador), una pelota que se mueve y rebota en los bordes superior e inferior, y detección de gol cuando la pelota supera una paleta.
2. **Marcador y ritmo de juego.** Marcador visible con los puntos de cada jugador y una cuenta atrás (o pausa equivalente) al comenzar cada punto.
3. **Colisiones y sonido.** El rebote de la pelota en las paletas debe tener un comportamiento razonable (por ejemplo, el ángulo puede depender de la zona de la paleta donde impacta) y el juego debe incluir efectos de sonido en los rebotes y los goles.
4. **Código organizado.** El código debe estar estructurado en clases y funciones con nombres claros, siguiendo la organización con sprites que propone el cuarto vídeo.

### Ampliaciones opcionales

- Pantalla de menú inicial (el cuarto vídeo deja el código preparado para ello).
- Varios niveles de dificultad (velocidad de la pelota, tamaño de las paletas, etc.).
- Modo de un jugador contra el ordenador.
- Mejoras visuales propias: colores, fondo, animaciones.
- Cualquier otra mejora que se os ocurra y podáis explicar.

---

## Opción B: Pong con turtle

### Contexto

Desarrollaréis el juego con el módulo turtle, que viene incluido con Python. Como guía de trabajo podéis seguir la lista de reproducción *Pong in Python 3 for Beginners*, del canal TokyoEdtech, que construye el juego paso a paso con turtle. Está en inglés. La lista sirve de referencia y apoyo: la práctica no consiste en copiar el código de los vídeos, sino en entender cada paso y escribir vuestra propia versión.

### Material de referencia

- Lista de reproducción (en inglés): [Pong in Python 3 for Beginners (TokyoEdtech)](https://www.youtube.com/playlist?list=PLlEgNdBJEO-kXk2PyBxhSmo84hsO3HAz2)
- GitHub del autor (TokyoEdtech): [github.com/wynand1004](https://github.com/wynand1004)
- Código completo oficial del Pong con turtle: [christianthompson.com/.../pong.py](https://christianthompson.com/sites/default/files/Pong/pong.py)
- Documentación oficial del módulo: [docs.python.org/3/library/turtle.html](https://docs.python.org/3/library/turtle.html)

### Requisitos técnicos

- Python 3 instalado en el equipo. No hace falta instalar ninguna librería: turtle forma parte de la biblioteca estándar.
- Un editor o entorno de desarrollo a vuestra elección (por ejemplo, VS Code o IDLE).
- Importante: turtle necesita una ventana gráfica, por lo que esta práctica se trabaja en local; no se puede ejecutar en Google Colab.

### Requisitos funcionales

El juego entregado debe cumplir, como mínimo, los siguientes requisitos:

1. **Juego base.** Ventana de juego con fondo propio, dos paletas controladas por teclado (una por jugador) y una pelota que se mueve dentro de la ventana.
2. **Rebotes y colisiones.** La pelota rebota en los bordes superior e inferior y en las paletas. Las paletas no pueden salir de la ventana.
3. **Marcador y goles.** Cuando la pelota supera una paleta se anota un punto al otro jugador, se actualiza un marcador visible en pantalla y la pelota vuelve al centro.
4. **Código organizado.** El código debe estar estructurado en funciones con nombres claros (por ejemplo, una función para mover cada paleta) y comentado donde sea necesario.

### Ampliaciones opcionales

- Efectos de sonido en los rebotes y los goles (comprobad que funcionan en vuestro sistema operativo).
- Una puntuación máxima que termine la partida y muestre al ganador.
- Aumento progresivo de la velocidad de la pelota.
- Modo de un jugador contra el ordenador.
- Mejoras visuales propias: colores, formas, línea central.
- Cualquier otra mejora que se os ocurra y podáis explicar.

---

## Entrega

- Un archivo `.zip` con el código fuente completo (archivos `.py` y los recursos necesarios: imágenes y sonidos, si los hay).
- Un breve documento README (media página) indicando: cómo ejecutar el juego, qué requisitos se han completado, qué ampliaciones se han hecho y las dificultades encontradas.
- El juego debe ejecutarse sin errores con `python main.py` (o el nombre de archivo que indiquéis en el README).

## Valoración

La práctica es voluntaria y no tiene un porcentaje directo en la calificación. La valoración se hará mediante una **entrevista personal**: deberéis saber explicar vuestro código, los requisitos cumplidos y las ampliaciones realizadas.

## Indicaciones

- Los vídeos son un apoyo, no la solución: se valorará que el código sea vuestro y que sepáis explicarlo. Entregar el código de los ejemplos del autor sin cambios cuenta como práctica no superada.
- Podéis trabajar individualmente o en parejas (indicad los nombres en la entrega).
- Dudas y seguimiento: en clase o por el canal habitual del grupo.
