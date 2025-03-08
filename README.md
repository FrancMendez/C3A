# C3A Francisco Josue Mendez Suriano 091-14-9796
Tarea C3A
Introducción

Los flip-flops son elementos fundamentales en los circuitos digitales secuenciales, utilizados para almacenar y gestionar información en sistemas electrónicos. Su funcionamiento se basa en el uso de compuertas lógicas para mantener un estado estable hasta que una señal de control determine un cambio. En este documento, exploraremos la evolución desde el SR Latch hasta el D Flip-Flop, destacando sus mejoras y ventajas en aplicaciones de sincronización y almacenamiento de datos.

1. SR Latch

El SR Latch es la base de todos los flip-flops y se construye con dos compuertas NOR.

Circuito del SR Latch

Entradas: S (Set) y R (Reset)Salidas: Q y Q’ (inversa de Q)

Reglas de operación

S = 1, R = 0 → Q = 1 (Set)

S = 0, R = 1 → Q = 0 (Reset)

S = 0, R = 0 → Mantiene el estado anterior

S = 1, R = 1 → Estado inválido (no permitido)

Mejora en el siguiente paso: Se puede evitar el estado inválido utilizando una compuerta adicional.

2. D-Latch

El D-Latch mejora al SR Latch al eliminar la condición no válida (S = 1, R = 1).

Circuito del D-Latch

Se agrega una compuerta NOT a la entrada D para generar S y R automáticamente.

Se introduce una señal de Habilitación (Enable o Clock, C) para permitir cambios solo cuando C = 1.

Mejora en el siguiente paso: Un D-Latch puede cambiar su estado en cualquier momento cuando C = 1, lo que no es ideal para la sincronización en circuitos secuenciales.

3. D Flip-Flop

Para mejorar la estabilidad del D-Latch, se utiliza el D Flip-Flop, que cambia su estado solo en los flancos de reloj.

Circuito del D Flip-Flop

Se compone de dos D-Latches en cascada:

Latch Maestro: Controlado por el flanco bajo del reloj.

Latch Esclavo: Controlado por el flanco alto del reloj.

Esto permite que los datos solo cambien en un instante preciso, evitando transiciones intermedias.

Ventajas del D Flip-Flop sobre el D-Latch

Estado estable y sincronización precisa con el reloj.

Ideal para registros y máquinas de estados.

Elimina el problema de cambios indeseados cuando C = 1.

Conclusión

La evolución desde el SR Latch hasta el D Flip-Flop muestra la importancia de mejorar la estabilidad y la sincronización en los circuitos digitales. Mientras que el SR Latch es un punto de partida básico, el D-Latch introduce control mediante una señal de habilitación y el D Flip-Flop logra una sincronización precisa en el flanco del reloj, evitando transiciones indeseadas. Estas mejoras permiten su aplicación en sistemas digitales complejos como registros y máquinas de estados finitos, esenciales en el diseño de hardware digital moderno.

VIDEOS

Video 1 https://youtu.be/imEMMmzGb5g
Video 2 https://youtu.be/q58DtZRR4cY
