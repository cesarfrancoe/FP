## **Problema 210: Suma de N números enteros**

### **Descripción**  
Escribe un algoritmo que solicite al usuario ingresar un número entero **N**. Si el valor de **N** es positivo, el algoritmo debe pedir al usuario ingresar **N** números enteros, calcular y mostrar la suma de esos **N** números. En caso de que **N** no sea positivo, el algoritmo debe mostrar un mensaje de error y solicitar nuevamente el valor de **N** hasta que se ingrese un número positivo.

---

### **Análisis**  
El problema consiste en sumar **N** números enteros ingresados por el usuario, con la condición de que **N** debe ser un número positivo.  
1. Solicitar al usuario ingresar un número entero **N**.
2. Verificar si **N** es positivo:
   - Si **N** es positivo, proceder a solicitar **N** números enteros.
   - Si **N** no es positivo, mostrar un mensaje de error y solicitar nuevamente el valor de **N** hasta que se ingrese un valor positivo.
3. Calcular la suma acumulada de los **N** números ingresados.
4. Finalmente, mostrar el resultado de la suma.

**Ejemplo**:  
Supongamos que el usuario ingresa **N = -3**. El algoritmo debe mostrar un mensaje de error y solicitar nuevamente el valor de **N**.  
Si luego ingresa **N = 4** y los números: 2, 5, -3, y 8, la suma de estos números sería:  
\( 2 + 5 + (-3) + 8 = 12 \)  
El algoritmo debe mostrar: **"La suma de los 4 números es: 12"**

---

### **Requerimientos**  
El algoritmo debe utilizar estructuras de control iterativas del tipo **"Hacer... Repetir"**.
