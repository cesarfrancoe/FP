## **Problema 254: Adivinanza de un número aleatorio entre 1 y 15**

### **Descripción**  
Escribe un algoritmo en el cual el computador genere un número aleatorio entre 1 y 15, y el usuario deba adivinarlo en un máximo de 3 intentos. El algoritmo debe informar al usuario si su suposición es correcta o incorrecta después de cada intento y finalizar una vez que el número sea adivinado o se hayan agotado los intentos.

---

### **Análisis**  
El problema consiste en implementar un juego de adivinanza en el que:
1. El computador genera un número aleatorio entre 1 y 15.
2. El usuario tiene un máximo de 3 intentos para adivinar el número.
3. Después de cada intento, el algoritmo verifica si la suposición es correcta o incorrecta:
   - Si es correcta, se informa al usuario y el juego termina.
   - Si es incorrecta, se le permite un nuevo intento hasta alcanzar el máximo de 3 intentos.
4. Si el usuario no adivina el número en 3 intentos, el juego finaliza.

**Ejemplo**:  
Si el número aleatorio generado es 7 y el usuario ingresa las siguientes suposiciones:
- Intento 1: 4 (Incorrecto)
- Intento 2: 9 (Incorrecto)
- Intento 3: 7 (Correcto)

El algoritmo debe mostrar:  
**"¡Correcto! Has adivinado el número en el intento 3."**

Si el usuario no acierta en ninguno de los 3 intentos, el algoritmo debe mostrar:  
**"Lo siento, has agotado los 3 intentos. El número era 7."**

---

### **Requerimientos**  
- El algoritmo debe utilizar estructuras de control iterativas del tipo **"Hacer... Repetir"**.
- No se pueden usar instrucciones rompedoras (como `romper`, `continuar` u otra similar) para finalizar el ciclo.
