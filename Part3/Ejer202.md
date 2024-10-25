## **Problema 202: Cálculo del promedio de números positivos ingresados**

### **Descripción**  
Escribe un algoritmo que solicite al usuario ingresar números enteros de forma continua. El algoritmo debe calcular y mostrar el promedio de los números positivos ingresados. Si el usuario ingresa un número menor que 1, el ciclo debe finalizar y mostrarse el promedio de los números positivos ingresados hasta ese momento.

---

### **Análisis**  
El problema consiste en solicitar números enteros al usuario, sumar los números positivos y calcular su promedio, con la condición de terminar el ciclo si se ingresa un número menor que 1.  
1. Solicitar al usuario ingresar un número entero.
2. Verificar si el número ingresado es positivo:
   - Si es positivo, añadirlo a una suma acumulada y aumentar el contador de números positivos ingresados.
   - Si es menor que 1, terminar el ciclo.
3. Calcular el promedio dividiendo la suma acumulada por el contador de números positivos ingresados.
4. Mostrar el promedio de los números positivos. Si no se ingresaron números positivos, mostrar un mensaje indicando que no hay datos para calcular el promedio.

**Ejemplo**:  
Supongamos que el usuario ingresa los números: 4, 7, -3, 8, y 0.  
- Números positivos ingresados: 4, 7, y 8  
- La suma es: \( 4 + 7 + 8 = 19 \)  
- El promedio es: \( 19 / 3 = 6.33 \)  

El algoritmo debe mostrar: **"El promedio de los números positivos es: 6.33"**

---

### **Requerimientos**  
- El algoritmo debe utilizar estructuras de control iterativas del tipo **"Hacer... Repetir"**.
- No se pueden usar instrucciones rompedoras (como `romper`, `continuar` u otra similar) para finalizar el ciclo.
