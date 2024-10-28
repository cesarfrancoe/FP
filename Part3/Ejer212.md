## **Problema 212: Validación de Rango**

### **Descripción**  
Escribe un algoritmo que permita a un usuario ingresar un número y valide que el número ingresado esté entre 1 y 100, inclusive. Si el número no se encuentra en este rango, el sistema debe mostrar un mensaje de error y solicitar nuevamente el número hasta que cumpla con la condición.

---

### **Análisis**  
El problema consiste en validar que el número ingresado por el usuario se encuentre dentro de un rango específico (1 a 100). Para lograrlo:

1. Solicitar al usuario que ingrese un número.
2. Verificar si el número está en el rango de 1 a 100, inclusive.
   - Si el número ingresado no está en este rango, mostrar un mensaje de error y solicitar nuevamente el número hasta que sea válido.
3. Cuando el usuario ingrese un número dentro del rango permitido, finalizar el proceso.

**Ejemplo**:  
- El usuario ingresa el número `105`. El sistema muestra un mensaje de error: **"Error: El número debe estar entre 1 y 100. Intente de nuevo."**
- El usuario ingresa el número `50`. El sistema acepta el número y finaliza el proceso.

---

### **Requerimientos**  
- El algoritmo debe utilizar una estructura de control iterativa del tipo **"Hacer... Repetir"** para validar el número.
- Si el número ingresado no está en el rango de 1 a 100, debe mostrar un mensaje de error.
- No se pueden usar instrucciones rompedoras (como `romper`, `continuar` u otra similar) para finalizar el ciclo.
