## **Problema 256: Número mágico de hasta 6 dígitos**

### **Descripción**  
Escribe un algoritmo que permita verificar si un número de hasta 6 dígitos ingresado por el usuario cumple con ciertas propiedades específicas para ser considerado un "número mágico". Si el usuario ingresa un número que no sea positivo o que tenga más de 6 dígitos, el algoritmo debe mostrar un mensaje de error y solicitar nuevamente el número hasta que se ingrese uno válido.

---

### **Análisis**  
El problema consiste en verificar si un número positivo de hasta 6 dígitos cumple con las condiciones de un "número mágico". Los pasos son los siguientes:
1. Solicitar al usuario ingresar un número positivo de hasta 6 dígitos.
   - Si el número ingresado no es positivo o tiene más de 6 dígitos, mostrar un mensaje de error y pedir otro número.
2. Realizar la verificación según las propiedades definidas para el "número mágico".
3. Mostrar el resultado al usuario, indicando si el número ingresado es o no un "número mágico".

**Ejemplo**:  
Supongamos que el usuario ingresa el número 123456.  
- Si el número cumple con las propiedades requeridas, el algoritmo debe mostrar: **"123456 es un número mágico"**.
- Si el número no cumple con las propiedades, el algoritmo debe mostrar: **"123456 no es un número mágico"**.

Si el usuario ingresa un número mayor de 6 dígitos o un número negativo, el algoritmo debe mostrar:  
**"Error: El número debe ser positivo y tener hasta 6 dígitos. Intente de nuevo."**

---

### **Requerimientos**  
- El algoritmo debe permitir que el usuario ingrese solo números positivos de hasta 6 dígitos.
- Si el número ingresado es mayor de 6 dígitos o no es positivo, debe mostrar un mensaje de error y solicitar nuevamente un número válido.
- Debe utilizar estructuras de control iterativas del tipo **"Hacer... Repetir"**.
- No se pueden usar instrucciones rompedoras (como `romper`, `continuar` u otra similar) para finalizar el ciclo.
