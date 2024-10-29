## **Problema 272: Simulador de l juego de dados "Pig"**

### **Descripción**  
"Pig" es un juego de dados que combina elementos de suerte y estrategia. En esta versión, el jugador humano compite contra la computadora. Ambos jugadores se turnan para lanzar dos dados con el objetivo de ser los primeros en alcanzar o superar una puntuación objetivo predeterminada, generalmente 100 puntos.

Escribe un algoritmo que simule el juego de acuerdo con las reglas descritas.

---

### **Análisis**  
Para simular el juego "Pig" entre el jugador humano y la computadora, se deben considerar las siguientes reglas y secuencias:

1. **Objetivo**:
   - El objetivo del juego es que el jugador humano o la computadora sean los primeros en alcanzar o superar una puntuación total de 100 puntos.

2. **Turnos**:
   - La computadora inicia cada turno lanzando dos dados.
   - Luego, el jugador humano toma su turno lanzando dos dados.
   - En cada turno, ambos jugadores pueden lanzar los dados tantas veces como deseen, acumulando puntos en su puntuación de turno.

3. **Lanzamiento de los Dados**:
   - En su turno, el sistema debe mostrar la indicación: `"Presiona [ENTER] para lanzar el dado..."` para que el jugador humano pueda lanzar sus dados. Cuando el jugador presiona ENTER, se lanzan los dados.
   - Cada lanzamiento puede producir los siguientes resultados:
     - Si alguno de los dados muestra un `1`, el jugador pierde todos los puntos acumulados en el turno y su turno termina.
     - Si ambos dados muestran `1`s, el jugador pierde todos sus puntos acumulados en el juego y su turno también termina.
     - Si los dados muestran valores distintos de `1`, el jugador acumula la suma de los valores obtenidos en el turno.

4. **Mensajes del Sistema Durante el Juego**:
   - Cada vez que el jugador humano lanza los dados, el sistema muestra un mensaje con el resultado obtenido y la acción correspondiente.
     - Ejemplo: `"Humano lanzó 2 dados: 4 y 3"`
     - `"Total acumulado en este turno: 7 puntos"`

5. **Decisión de Continuar o Detenerse**:
   - Después de cada lanzamiento, el jugador debe decidir si sigue lanzando para acumular más puntos o si detiene su turno para conservar los puntos obtenidos hasta ese momento.
   - Para el jugador humano, se muestra un mensaje con la opción de continuar o detenerse.
   - La computadora tomará decisiones basadas en una estrategia predefinida.

6. **Estructura de Control para el Flujo de Turnos**:
   - Para manejar el flujo de turnos, el algoritmo debe utilizar una estructura de control iterativa del tipo **"Hacer... Repetir"** para verificar constantemente si se ha alcanzado la condición de finalización (100 puntos o más).
   - No se pueden usar instrucciones rompedoras (como **romper**, **continuar** u otra similar) para finalizar el ciclo. La condición de finalización debe evaluarse directamente en la estructura "Hacer... Repetir".

7. **Final del Juego**:
   - El juego termina cuando el jugador humano o la computadora alcanzan o superan los 100 puntos. Se debe completar la ronda actual antes de declarar al ganador. En caso de empate, ambos jugadores se consideran ganadores.

**Ejemplo de desarrollo del juego**:  
1. El sistema muestra el turno del jugador humano y la indicación:
   ```
   Presiona [ENTER] para lanzar el dado...
   ```

2. El jugador humano presiona [ENTER], y el sistema muestra:
   - `"Humano lanzó 2 dados: 5 y 2"`
   - `"Total acumulado en este turno: 7 puntos"`

3. El sistema solicita al jugador humano si desea continuar o detenerse. El jugador puede tomar la decisión.
4. El juego continúa en turnos hasta que alguno de los jugadores alcance o supere los 100 puntos.

---

### **Requerimientos**  
- El algoritmo debe solicitar al jugador humano que presione [ENTER] para lanzar los dados en su turno.
- En cada lanzamiento, el sistema debe mostrar el resultado y las acciones resultantes de acuerdo con las reglas.
- El algoritmo debe utilizar una estructura de control iterativa **"Hacer... Repetir"** para el flujo de turnos, sin emplear instrucciones rompedoras (como **romper**, **continuar** u otra similar) para finalizar el ciclo. La condición de finalización debe evaluarse directamente en la estructura.
- Al final de cada turno, el sistema debe preguntar al jugador humano si desea continuar o detenerse.
- El juego termina cuando uno de los jugadores alcanza o supera la puntuación objetivo, y se debe completar la ronda actual para declarar un ganador en caso de empate.
