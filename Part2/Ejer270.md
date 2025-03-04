## **Problema 270: Simulador del Juego de Serpientes y Escaleras**

[<img src="https://www.thermmark.co.uk/wp-content/uploads/2017/01/TMG003-100LF-Snakes-Ladders-1-100-Large-Full-Solid.png" width="500px">](https://www.thermmark.co.uk/wp-content/uploads/2017/01/TMG003-100LF-Snakes-Ladders-1-100-Large-Full-Solid.png)

### **Descripción**  
El juego de Serpientes y Escaleras es un clásico juego de mesa que combina suerte y estrategia. En este juego, los jugadores avanzan por un tablero de 100 casillas, tratando de ser el primero en llegar a la casilla final. El camino hacia la victoria está lleno de obstáculos en forma de serpientes y escaleras, los cuales pueden acelerar o retrasar el avance de los jugadores. La implementación debe basarse en las reglas y la disposición del tablero mostradas en la imagen proporcionada.

---

### **Análisis**  
Para simular el juego de Serpientes y Escaleras, se deben considerar las siguientes reglas y secuencias:

1. **Tablero de Juego**:
   - El tablero consta de 100 casillas numeradas del 1 al 100.
   - Los jugadores avanzan desde la casilla 1 hasta la casilla 100.
   - La posición de serpientes y escaleras debe basarse en la imagen proporcionada del tablero.

2. **Jugadores**:
   - El juego es entre un jugador humano y la computadora.

3. **Inicio del Juego**:
   - El jugador humano siempre empieza primero.

4. **Turnos de Juego**:
   - Los jugadores se turnan para lanzar un dado de seis caras.
   - En el turno del jugador humano, el sistema solicita presionar `[ENTER]` para lanzar el dado.
   - Después de presionar `[ENTER]`, el jugador humano lanza el dado y avanza su ficha el número de casillas indicado por el dado.
   - Luego, la computadora realiza automáticamente su movimiento lanzando un dado de seis caras.
   - En cada turno, el sistema debe mostrar las posiciones actuales del jugador humano y la computadora.

5. **Movimiento en el Tablero**:
   - Cada jugador avanza su ficha en el tablero según el número obtenido en el dado.
   - Si un jugador llega a la casilla 100, gana el juego, siempre y cuando su contrincante no llegue también a la casilla 100 en ese mismo turno.

6. **Serpientes y Escaleras**:
   - Las serpientes y escaleras están ubicadas en ciertas casillas del tablero según la imagen proporcionada.
   - Si un jugador cae en una casilla donde termina una serpiente, se mueve hacia abajo hasta la casilla donde comienza la serpiente.
   - Si un jugador cae en una casilla donde comienza una escalera, se mueve hacia arriba hasta la casilla donde termina la escalera.

7. **Condición de Victoria o Empate**:
   - El primer jugador en llegar a la casilla 100 gana el juego, siempre y cuando su contrincante no alcance también la casilla 100 en ese turno.
   - Si ambos jugadores llegan a la casilla 100 en el mismo turno, se considera un empate.

**Ejemplo de Desarrollo del Juego**:  
1. El sistema le pide al jugador humano presionar `[ENTER]` para lanzar el dado, y el jugador obtiene un `4`. Se mueve desde la casilla 1 hasta la casilla 5. El sistema muestra: **"Jugador Humano: Casilla 5, Computadora: Casilla 1"**.
2. En su turno, la computadora lanza el dado y obtiene un `6`, moviéndose de la casilla 1 a la casilla 7. El sistema muestra: **"Jugador Humano: Casilla 5, Computadora: Casilla 7"**.
3. En su siguiente turno, el jugador humano vuelve a presionar `[ENTER]` para lanzar el dado y obtiene un `5`, avanzando de la casilla 5 a la 10, donde hay una escalera que lo lleva a la casilla 20. El sistema muestra: **"Jugador Humano: Casilla 20, Computadora: Casilla 7"**.
4. El juego continúa hasta que uno de los jugadores alcanza la casilla 100, a menos que ambos lo hagan en el mismo turno, lo cual resultará en empate.

---

### **Requerimientos**  
- El algoritmo debe solicitar al jugador humano presionar `[ENTER]` para lanzar el dado.
- El dado utilizado en el juego debe ser de 6 caras.
- La disposición de las serpientes y escaleras debe basarse en la imagen del tablero proporcionada.
- Las posiciones de serpientes y escaleras deben almacenarse en variables simples, sin utilizar arreglos ni estructuras similares.
- En cada turno, el sistema debe mostrar las posiciones actuales del jugador humano y la computadora.
- El algoritmo debe utilizar estructuras de control iterativas del tipo **"Hacer... Repetir"** para el flujo de los turnos.
- No se pueden usar instrucciones rompedoras (como `romper`, `continuar` u otra similar) para finalizar el ciclo.
