## **Problema 271: Simulador del Juego LCR**

### **Descripción**  
"LCR" (Left, Center, Right) es un juego de dados simple y divertido que se juega en grupo. Cada jugador tiene una cantidad de fichas y sigue instrucciones basadas en los resultados de los dados para pasar fichas a otros jugadores o colocarlas en el centro. El objetivo es ser el último jugador con fichas restantes.

Escribe un algoritmo que simule el juego LCR, incluyendo a tres participantes: dos controlados por la computadora llamados Rosie y Bender, y un jugador humano cuyo nombre y cantidad de fichas inicial se solicitan al inicio.

---

### **Análisis**  

1. **Elementos del Juego**:
   - El juego utiliza dados de seis caras para determinar las acciones en cada turno.
   - Las posibles caras del dado indican las siguientes acciones:

| Valor del dado | Símbolo | Significado | Acción a realizar                                      |
|----------------|---------|-------------|-------------------------------------------------------|
| 1              | L       | Left        | Pasa una ficha al jugador a la izquierda.             |
| 2              | C       | Center      | Coloca una ficha en el centro, eliminándola del juego.|
| 3              | R       | Right       | Pasa una ficha al jugador a la derecha.               |
| 4, 5, 6        | *       | Punto       | Acción neutra, no se hace nada.                       |

2. **Jugadores**:
   - El juego se desarrolla con tres jugadores: dos controlados por la computadora (Rosie y Bender) y un jugador humano.
   - Al inicio, se solicita el nombre del jugador humano y la cantidad de fichas iniciales, que debe estar entre 3 y 5. Si el usuario ingresa un valor fuera del rango, se debe mostrar un mensaje de error y solicitar nuevamente hasta que se ingrese un número válido.
   - Todos los jugadores comienzan con la misma cantidad de fichas determinada al inicio.
   - Las posiciones de los jugadores en el juego son las siguientes:

| Jugador de la izquierda | Jugador | Jugador de la derecha |
|-------------------------|---------|------------------------|
| Bender                  | Humano  | Rosie                 |
| Humano                  | Rosie   | Bender                |
| Rosie                   | Bender  | Humano                |

3. **Inicio del Juego**:
   - El jugador humano siempre comienza el primer turno.

4. **Turnos del Juego**:
   - Los jugadores se turnan para lanzar los dados en el siguiente orden: jugador humano, Rosie, y luego Bender.
   - En cada turno:
     - El sistema muestra las posiciones relativas y cantidad de fichas de los jugadores con referencia al jugador que va a lanzar.
     - El jugador lanza entre uno y tres dados, dependiendo de la cantidad de fichas que tiene. Si un jugador tiene menos de tres fichas, lanza solo la cantidad de dados equivalente al número de fichas que posee.
   - Al final de cada turno, el sistema muestra el estado actualizado de las fichas de cada jugador.

5. **Condición de Victoria**:
   - El juego continúa hasta que solo un jugador tenga fichas, convirtiéndose en el ganador.
   - Los jugadores que pierden todas sus fichas no lanzan los dados en su turno, pero pueden recibir fichas de otros jugadores y reintegrarse al juego.

---

### **Ejemplo de Desarrollo del Juego:**
   - Antes de comenzar el turno del jugador humano, el sistema muestra:
     ```
     Turno de Humano:
     [Rosie: 3 fichas] <-- [Humano: 3 fichas] --> [Bender: 3 fichas]
     ```
   - El jugador humano presiona [ENTER] para lanzar los dados.
   - El jugador humano lanza tres dados y obtiene los resultados: L, *, R.
     - El sistema muestra: "Humano lanzó 3 dados: L, *, R"
     - También muestra las acciones: "Humano pasó 1 ficha a Rosie y 1 ficha a Bender"
   - Al final de cada turno, el sistema muestra el estado actualizado de las fichas de cada jugador y se verifica la condición de finalización.
   - El juego continúa en sentido horario hasta que solo un jugador tiene fichas, y ese jugador es el ganador.

---

### **Restricciones de Implementación**

1. El juego debe utilizar una estructura de control iterativa del tipo "Hacer... Repetir" para el flujo de turnos.
2. No se pueden usar instrucciones rompedoras (como `break`, `continue`, u otra similar) para finalizar el ciclo de juego; la condición de finalización debe evaluarse directamente en la estructura iterativa.

