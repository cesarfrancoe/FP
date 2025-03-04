## **Problema 211: Simulación de 6N lanzamientos de un dado de 6 caras y estadísticas**

### **Descripción**  
Escribe un algoritmo que solicite al usuario ingresar un número entero **N**. Si el valor de **N** es positivo, el algoritmo debe simular **6N** lanzamientos de un dado de 6 caras y luego mostrar la cantidad de veces que cada número (del 1 al 6) fue obtenido. En caso de que **N** no sea positivo, el algoritmo debe mostrar un mensaje de error y solicitar nuevamente el valor de **N** hasta que se ingrese un número positivo.

---

### **Análisis**  
El problema consiste en simular **6N** lanzamientos de un dado de 6 caras y obtener estadísticas de las repeticiones de cada número obtenido, con la condición de que **N** debe ser un número positivo.  
1. Solicitar al usuario ingresar un número entero **N**.
2. Verificar si **N** es positivo:
   - Si **N** es positivo, calcular la cantidad total de lanzamientos como **6N** y proceder a simular los lanzamientos.
   - Si **N** no es positivo, mostrar un mensaje de error y solicitar nuevamente el valor de **N** hasta que se ingrese un valor positivo.
3. Simular **6N** lanzamientos del dado, generando un número aleatorio entre 1 y 6 para cada lanzamiento y contando la cantidad de veces que aparece cada número.
4. Mostrar el conteo de repeticiones de cada número del 1 al 6.

**Ejemplo**:  
Supongamos que el usuario ingresa **N = 3**. Esto significa que se realizarán **6 \* 3 = 18** lanzamientos. Los resultados de estos lanzamientos podrían generar las siguientes estadísticas:  

Estadisticas (Frecuencia):  
**"Número 1: 4"**  
**"Número 2: 3"**  
**"Número 3: 2"**  
**"Número 4: 5"**  
**"Número 5: 1"**  
**"Número 6: 3"**

---

### **Requerimientos**  
El algoritmo debe utilizar estructuras de control iterativas del tipo **"Hacer... Repetir"**.
