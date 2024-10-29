## **Problema 272: Juego de Dados "Pig"**

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
   - En cada turno, tanto la computadora como el jugador humano pueden lanzar los dados tantas veces como deseen, acumulando puntos en su puntuación de turno.

3. **Puntuación**:
   - Si alguno de los jugadores lanza un `1` en cualquiera de los dados, pierde todos los puntos acumulados en ese turno y su turno termina inmediatamente.
   - Si un jugador lanza dos `1`s, pierde todos los puntos acumulados en el juego hasta ese momento, y su turno termina.

4. **Decisión de Continuar o Detenerse**:
   - Al inicio de su turno, el jugador humano debe escribir la letra **"L"** para lanzar los dados.
      - Si ingresa cualquier otro valor, el sistema debe mostrar un mensaje de error y solicitar nuevamente la entrada hasta que sea correcta.
   - Después del primer lanzamiento, el jugador humano debe decidir si continúa lanzando o detiene su turno.
      - Para cada lanzamiento adicional en el mismo turno, el jugador humano debe responder con "S" para continuar o "N" para detenerse y acumular los puntos del turno a su puntuación total.
      - Si el usuario ingresa cualquier valor distinto de "S" o "N", el sistema debe mostrar un mensaje de error y solicitar nuevamente la respuesta hasta que sea correcta.
   - La computadora tomará decisiones basadas en una estrategia predefinida para decidir si continúa lanzando o se detiene.

5. **Final del Juego**:
   - El juego termina cuando el jugador humano o la computadora alcanzan o superan los 100 puntos.
   - Se debe completar la ronda actual antes de declarar al ganador. En caso de empate, ambos jugadores se consideran ganadores.

**Ejemplo de desarrollo del juego**:  
1. La computadora lanza los dados y obtiene un `3` y un `4`, acumulando 7 puntos en su turno.
2. La computadora decide lanzar de nuevo y obtiene un `2` y un `5`, acumulando 7 puntos adicionales para un total de 14 puntos en su turno.
3. La computadora decide detenerse y acumula sus puntos a su puntuación total.
4. Es el turno del jugador humano. El sistema le pide escribir "L" para lanzar los dados. El jugador escribe "L" y obtiene un `6` y un `1`. Debido a que obtuvo un `1`, pierde todos los puntos de su turno y su turno termina.
5. El juego continúa hasta que alguno de los jugadores alcance o supere los 100 puntos.

---

### **Requerimientos**  
- El algoritmo debe alternar turnos entre la computadora y el jugador humano, permitiendo la acumulación de puntos en cada turno.
- Si un jugador obtiene al menos un `1` en los dados, debe perder los puntos de su turno, y si obtiene dos `1`s, pierde todos sus puntos acumulados en el juego.
- La decisión de continuar o detenerse debe ser opcional para el jugador humano después de cada lanzamiento.
   - Al inicio de su turno, el jugador humano debe escribir la letra **"L"** para lanzar los dados. Si se ingresa cualquier otro valor, se debe mostrar un mensaje de error y solicitar nuevamente la entrada hasta que sea correcta.
   - Para cada lanzamiento adicional en el mismo turno, el jugador humano debe responder con "S" para continuar lanzando o "N" para detenerse. Si el usuario ingresa cualquier otro valor, debe mostrarse un mensaje de error y solicitar nuevamente la respuesta hasta que sea correcta.
- La computadora debe seguir una estrategia predefinida para decidir si continúa lanzando o se detiene.
- El juego debe terminar al completar la ronda en que un jugador alcanza o supera la puntuación objetivo.

---

### **Notas sobre Estrategias para la Computadora**

Existen varias estrategias que la computadora puede seguir para decidir si continúa lanzando o se detiene:

1. **Estrategia aleatoria básica**: La computadora genera un número aleatorio entre 0 y 1 donde `0` indica "N" (detenerse) y `1` indica "S" (continuar). Esto permite una probabilidad simple de 50% para cada opción, agregando un elemento de imprevisibilidad.

2. **Estrategia basada en puntaje acumulado del turno**: La computadora podría decidir detenerse si ha acumulado una cantidad de puntos específica en su turno (por ejemplo, 15 puntos), reduciendo así el riesgo de perder puntos acumulados en caso de obtener un `1`.

3. **Estrategia según la puntuación total**: Si la computadora está cerca de alcanzar el objetivo de 100 puntos, podría optar por arriesgarse menos y detenerse rápidamente para asegurar los puntos necesarios sin correr riesgos innecesarios. Por ejemplo, si la computadora tiene 95 puntos, le bastará con obtener al menos 5 puntos en su próximo turno. En lugar de continuar lanzando repetidamente, podría detenerse después de un solo lanzamiento si obtiene esos puntos, minimizando el riesgo de perder los acumulados.

4. **Estrategia basada en distancia mínima con el usuario**: La computadora puede evaluar la diferencia de puntos con el jugador humano, tanto si está por encima como por debajo en puntaje. Si esta diferencia es menor que un valor mínimo predeterminado (por ejemplo, 10 puntos), la computadora puede optar por arriesgarse y continuar lanzando para reducir la distancia si va detrás, o ampliarla si va adelante. Si la distancia es amplia, puede optar por detenerse y conservar sus puntos acumulados.

Estas estrategias pueden hacer que el juego sea más desafiante y agregar un componente de decisión similar al de un jugador humano.
