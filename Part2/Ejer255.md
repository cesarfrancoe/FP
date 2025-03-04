## **Problema 255: Adivinanza de un número pensado por el usuario**

### **Descripción**  
Escribe un algoritmo en el cual el usuario piense en un número entre 1 y 15, y el computador intente adivinarlo en un máximo de 3 intentos. En cada intento, el algoritmo debe generar un número aleatorio entre los límites actuales (inicialmente de 1 a 15) y mostrarlo al usuario, quien responderá si ese es el número pensado o no. Si el número no es correcto, el usuario debe indicar si el número generado es "mayor" o "menor" que el número pensado, lo que permite al computador ajustar los límites mínimo o máximo para el siguiente intento. El algoritmo debe validar que el usuario responda "S" o "N" en cada pregunta; si la respuesta es diferente, debe mostrar un mensaje de error y solicitar nuevamente la respuesta. El juego termina cuando el computador adivina el número o se agotan los 3 intentos.

---

### **Análisis**  
El problema consiste en implementar un juego de adivinanza en el que:
1. El usuario piensa en un número entre 1 y 15.
2. El computador tiene un máximo de 3 intentos para adivinar el número pensado.
3. En cada intento, el algoritmo:
   - Genera un número aleatorio entre los límites actuales (inicialmente de 1 a 15).
   - Muestra el número generado al usuario y le pregunta:  
     **"¿Este es el número que pensaste (S/N)?"**
   - Valida la respuesta del usuario, repitiendo la pregunta hasta que responda "S" o "N". Si el usuario responde algo diferente, muestra un mensaje de error:  
     **"Respuesta no válida. Por favor, responde con 'S' o 'N'."**
   - Si el usuario responde "S", el computador ha adivinado y el juego termina.
   - Si el usuario responde "N", el computador pregunta:  
     **"¿Este número es mayor que el que pensaste (S/N)?"**
       - Valida nuevamente la respuesta hasta que el usuario ingrese "S" o "N". Si la respuesta es diferente, muestra el mensaje de error:  
         **"Respuesta no válida. Por favor, responde con 'S' o 'N'."**
       - Si el usuario responde "S", el computador ajusta el límite máximo para el próximo intento.
       - Si el usuario responde "N", el computador ajusta el límite mínimo para el próximo intento.
4. Si el computador no adivina el número en 3 intentos, el juego finaliza.

**Ejemplo**:  
Supongamos que el número pensado por el usuario es 7 y el computador genera las siguientes suposiciones:
- Intento 1: 10  
  - Pregunta: "¿Este es el número que pensaste (S/N)?" (Usuario responde "N")
  - Pregunta: "¿Este número es mayor que el que pensaste (S/N)?" (Usuario responde "S")
  - El nuevo límite máximo se ajusta a 9.
- Intento 2: 5  
  - Pregunta: "¿Este es el número que pensaste (S/N)?" (Usuario responde "N")
  - Pregunta: "¿Este número es mayor que el que pensaste (S/N)?" (Usuario responde "N")
  - El nuevo límite mínimo se ajusta a 6.
- Intento 3: 7  
  - Pregunta: "¿Este es el número que pensaste (S/N)?" (Usuario responde "S")

El algoritmo debe mostrar:  
**"¡Correcto! El computador ha adivinado el número en el intento 3."**

Si el computador no acierta en ninguno de los 3 intentos, el algoritmo debe mostrar:  
**"El computador no ha logrado adivinar el número en 3 intentos."**

---

### **Requerimientos**  
- El algoritmo debe utilizar estructuras de control iterativas del tipo **"Hacer... Repetir"**.
- No se pueden usar instrucciones rompedoras (como `romper`, `continuar` u otra similar) para finalizar el ciclo.
- El algoritmo debe validar las respuestas del usuario, mostrando un mensaje de error y solicitando nuevamente la respuesta hasta que el usuario responda "S" o "N".
