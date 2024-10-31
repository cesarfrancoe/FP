## **Problema 271: Simulador del Juego LCR**

### **Descripción**  
"LCR" (Left, Center, Right) es un juego de dados simple y divertido que se juega en grupo. Cada jugador tiene una cantidad de fichas y sigue instrucciones basadas en los resultados de los dados para pasar fichas a otros jugadores o colocarlas en el centro. El objetivo es ser el último jugador con fichas restantes.

Escribe un algoritmo que simule el juego LCR, incluyendo a tres participantes: dos controlados por la computadora llamados Rosie y Bender, y un jugador humano cuyo nombre y cantidad de fichas inicial se solicitan al inicio.

---

### **Análisis**  
Para simular el juego "LCR" con tres participantes, se deben tener en cuenta las siguientes reglas y secuencias:

1. **Jugadores y Fichas Iniciales:**
   - El juego se desarrolla con tres jugadores: dos controlados por la computadora (Rosie y Bender) y un jugador humano.
   - Al inicio, se solicita el nombre del jugador humano y la cantidad de fichas iniciales, que debe estar entre 3 y 5. Si el usuario ingresa un valor fuera del rango, se debe mostrar un mensaje de error y solicitar nuevamente hasta que se ingrese un número válido.
   - Todos los jugadores comienzan con la misma cantidad de fichas determinada al inicio.
   - El juego se desarrolla en turnos, donde cada jugador lanza los dados y sigue las instrucciones hasta que solo uno quede con fichas.

2. **Visualización del Estado del Juego Antes de Cada Turno:**
   - Antes de cada turno, el sistema muestra las posiciones relativas y cantidad de fichas de los jugadores con referencia únicamente al jugador que va a lanzar, junto con un mensaje claro sobre el jugador que está por lanzar.
   
     Ejemplos de visualización:
     - Si el jugador humano va a lanzar:
       ```
       Turno de Humano:
       [Rosie: ? fichas] <-- [Humano: ? fichas] --> [Bender: ? fichas]
       Presiona [ENTER] para lanzar el dado...
       ```
     - Si Rosie va a lanzar:
       ```
       Turno de Rosie:
       [Bender: ? fichas] <-- [Rosie: ? fichas] --> [Humano: ? fichas]
       Rosie lanzará ? dados.
       ```
     - Si Bender va a lanzar:
       ```
       Turno de Bender:
       [Humano: ? fichas] <-- [Bender: ? fichas] --> [Rosie: ? fichas]
       Bender lanzará ? dados.
       ```

3. **Lanzamiento de los Dados y Comportamiento de los Resultados:**
   - En cada turno, el jugador lanza entre uno y tres dados, dependiendo de la cantidad de fichas que tiene, y el sistema muestra un mensaje indicando el número de dados lanzados.
   - Los dados pueden mostrar las siguientes caras:
     - **1: L (Left)** - Pasa una ficha al jugador a la izquierda.
     - **2: C (Center)** - Coloca una ficha en el centro, eliminándola del juego.
     - **3: R (Right)** - Pasa una ficha al jugador a la derecha.
     - **4, 5, 6: * (Punto)** - Acción neutra, no se hace nada.
   - Si un jugador tiene menos de tres fichas, solo lanza la cantidad de dados equivalente al número de fichas que posee.
   - Para el jugador humano, el sistema debe mostrar el mensaje "Presiona [ENTER] para lanzar el dado...". Cuando el jugador presiona ENTER, se lanzan los dados.

4. **Mensajes del Sistema Durante el Juego:**
   - Cada vez que un jugador lanza los dados, el sistema muestra un mensaje detallado de los resultados de los dados y las acciones realizadas.
     - Ejemplo: "Humano lanzó 3 dados: L, *, R"
     - También muestra las acciones realizadas: "Humano pasó 1 ficha a Rosie y 1 ficha a Bender"
   - Al final de cada turno, el sistema muestra el estado actualizado de las fichas de cada jugador.

5. **Orden de los Jugadores y Sentido del Juego:**
   - El juego se desarrolla en sentido horario, comenzando siempre con el jugador humano, seguido de Rosie y, por último, Bender.
   - Este orden se repite cíclicamente hasta que solo uno de los tres conserve fichas.

6. **Estructura de Control para el Flujo de Turnos:**
   - Para manejar el flujo de turnos, el algoritmo debe utilizar una estructura de control iterativa del tipo "Hacer... Repetir" para verificar constantemente si se ha alcanzado la condición de finalización (solo un jugador conserva fichas).
   - No se pueden usar instrucciones rompedoras (como romper, continuar u otra similar) para finalizar el ciclo. La condición de finalización debe evaluarse directamente en la estructura "Hacer... Repetir".

7. **Objetivo del Juego:**
   - El juego continúa en rondas hasta que solo un jugador tenga fichas, convirtiéndose en el ganador.
   - Los jugadores que pierden todas sus fichas no lanzan los dados en su turno, pero pueden recibir fichas de otros jugadores y reintegrarse al juego.

**Ejemplo de Desarrollo del Juego:**
   - Antes de comenzar el turno del jugador humano, el sistema muestra:
     ```
     Turno de Humano:
     [Rosie: 3 fichas] <-- [Humano: 3 fichas] --> [Bender: 3 fichas]
     Presiona [ENTER] para lanzar el dado...
     ```
   - El jugador humano presiona [ENTER] para lanzar los dados.
   - El jugador humano lanza tres dados y obtiene los resultados: L, *, R.
     - El sistema muestra: "Humano lanzó 3 dados: L, *, R"
     - También muestra las acciones: "Humano pasó 1 ficha a Rosie y 1 ficha a Bender"
   - Al final de cada turno, el sistema muestra el estado actualizado de las fichas de cada jugador y se verifica la condición de finalización.
   - El juego continúa en sentido horario hasta que solo un jugador tiene fichas, y ese jugador es el ganador.

---

### **Requerimientos**  

1. El algoritmo debe solicitar el nombre del jugador humano al inicio del juego.
2. El algoritmo debe solicitar la cantidad inicial de fichas, validando que esté entre 3 y 5. Si el usuario ingresa un valor fuera de este rango, se debe mostrar un mensaje de error y solicitar nuevamente hasta que sea correcto.
3. Antes de cada turno, el sistema debe mostrar las posiciones relativas y la cantidad de fichas de los jugadores, con referencia únicamente al jugador que va a lanzar, junto con un mensaje claro sobre quién lanzará los dados y cuántos.
4. Para el jugador humano, el sistema debe mostrar el mensaje "Presiona [ENTER] para lanzar el dado...", y cuando el jugador presione ENTER, se lanzarán los dados.
5. Cada vez que un jugador lanza los dados, el sistema debe mostrar un mensaje detallado de los resultados y las acciones realizadas en ese turno.
6. El juego debe utilizar una estructura de control iterativa "Hacer... Repetir" para el flujo de turnos, sin emplear instrucciones rompedoras (como romper, continuar u otra similar) para finalizar el ciclo. La condición de finalización debe evaluarse directamente en la estructura.
7. El juego se desarrolla en sentido horario, comenzando siempre con el jugador humano, seguido de Rosie y, por último, Bender.
8. Cada jugador debe seguir las instrucciones de los dados en cada turno para pasar fichas o eliminarlas.
9. Si un jugador tiene menos de tres fichas, solo debe lanzar el número de dados equivalente a la cantidad de fichas que posee.
10. Los jugadores sin fichas no lanzan dados, pero pueden recibir fichas de otros jugadores y reintegrarse al juego.
11. El juego debe finalizar cuando solo un jugador conserva fichas, declarando a ese jugador como el ganador.
