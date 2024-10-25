## **Problema 257: Validación del código ISBN de 10 dígitos**

### **Descripción**  
Escribe un algoritmo que valide si un número ingresado por el usuario es un código ISBN válido de 10 dígitos. Un código ISBN de 10 dígitos es válido si cumple con un criterio específico de validación matemática que involucra una fórmula de verificación. El algoritmo debe solicitar al usuario ingresar el código y verificar que tenga exactamente 10 dígitos; en caso contrario, debe mostrar un mensaje de error y pedir nuevamente el código.

---

### **Análisis**  
El problema consiste en verificar si un número ingresado por el usuario cumple con las propiedades de un código ISBN válido de 10 dígitos. Para esto:
1. Solicitar al usuario ingresar un número de 10 dígitos.
   - Si el número ingresado no tiene exactamente 10 dígitos, mostrar un mensaje de error y solicitar nuevamente el código.
2. Calcular el dígito de control usando la fórmula de verificación para ISBN-10:
   \[
   S = 1 \cdot d_1 + 2 \cdot d_2 + 3 \cdot d_3 + \dots + 10 \cdot d_{10}
   \]
   donde \(d_1, d_2, \dots, d_{10}\) son los dígitos del ISBN. El código es válido si el resultado de \( S \mod 11 = 0 \).
3. Mostrar el resultado al usuario, indicando si el código es un ISBN válido o no.

**Ejemplo**:  
Supongamos que el usuario ingresa el código ISBN `0306406152`.
- Cálculo de \( S = 1 \cdot 0 + 2 \cdot 3 + 3 \cdot 0 + 4 \cdot 6 + 5 \cdot 4 + 6 \cdot 0 + 7 \cdot 6 + 8 \cdot 1 + 9 \cdot 5 + 10 \cdot 2 = 176 \).
- Dado que \( 176 \mod 11 = 0 \), el código es válido.

El algoritmo debe mostrar: **"El código ISBN es válido."**

Si el usuario ingresa un número que no tiene 10 dígitos, el algoritmo debe mostrar:  
**"Error: El código ISBN debe tener exactamente 10 dígitos. Intente de nuevo."**

---

### **Requerimientos**  
- El algoritmo debe permitir que el usuario ingrese solo códigos ISBN de 10 dígitos.
- Si el número ingresado no tiene exactamente 10 dígitos, debe mostrar un mensaje de error y solicitar nuevamente el código.
- Debe utilizar estructuras de control iterativas del tipo **"Hacer... Repetir"**.
- No se pueden usar instrucciones rompedoras (como `romper`, `continuar` u otra similar) para finalizar el ciclo.
