## **Problema 258: Validación de números de tarjeta de crédito de 16 dígitos**

### **Descripción**  
Escribe un algoritmo que valide si un número ingresado por el usuario es un número de tarjeta de crédito válido de **16 dígitos**. El número de la tarjeta debe cumplir con el **algoritmo de Luhn** para considerarse válido. El algoritmo debe solicitar al usuario ingresar el número y verificar que tenga exactamente 16 dígitos; en caso contrario, debe mostrar un mensaje de error y pedir nuevamente el número.

---

### **Análisis**  
El problema consiste en verificar si un número ingresado por el usuario cumple con el **algoritmo de Luhn** para validar tarjetas de crédito de **16 dígitos**. Para esto:

1. Solicitar al usuario ingresar un número de tarjeta de crédito de **16 dígitos**.
   - Si el número ingresado no tiene exactamente 16 dígitos, mostrar un mensaje de error y solicitar nuevamente el número.
2. Aplicar el **algoritmo de Luhn** para validar el número de tarjeta:
   - Comenzando desde el segundo dígito desde la derecha, duplicar cada segundo dígito. Si el resultado de la duplicación es mayor a 9, restar 9 al resultado.
   - Sumar todos los dígitos, incluidos los duplicados y no duplicados.
   - Si el total es divisible por 10, el número de tarjeta es válido.
3. Mostrar el resultado al usuario, indicando si el número de tarjeta es válido o no.

**Ejemplo**:  
Supongamos que el usuario ingresa el número de tarjeta `4532015112830366`.

1. Comenzando desde el segundo dígito desde la derecha y duplicando cada segundo dígito:
   - Último dígito: `6` (no se duplica)
   - Segundo dígito desde la derecha: `3 * 2 = 6`
   - Tercer dígito desde la derecha: `6` (no se duplica)
   - Cuarto dígito desde la derecha: `8 * 2 = 16` → `16 - 9 = 7`
   - Quinto dígito desde la derecha: `3` (no se duplica)
   - Sexto dígito desde la derecha: `2 * 2 = 4`
   - Séptimo dígito desde la derecha: `1` (no se duplica)
   - Octavo dígito desde la derecha: `5 * 2 = 10` → `10 - 9 = 1`
   - Noveno dígito desde la derecha: `1` (no se duplica)
   - Décimo dígito desde la derecha: `0 * 2 = 0`
   - Undécimo dígito desde la derecha: `2` (no se duplica)
   - Duodécimo dígito desde la derecha: `3 * 2 = 6`
   - Décimo tercer dígito desde la derecha: `5` (no se duplica)
   - Décimo cuarto dígito desde la derecha: `4 * 2 = 8`
   - Décimo quinto dígito desde la derecha: `5` (no se duplica)
   - Décimo sexto dígito desde la derecha (primero desde la izquierda): `4 * 2 = 8`

2. Sumando todos los dígitos, incluidos los duplicados y no duplicados:
   ```
   Suma total = 8 + 5 + 8 + 3 + 6 + 1 + 1 + 4 + 0 + 3 + 8 + 7 + 6 + 4 + 6 + 6 = 76
   ```

3. Verificación:
   - Dado que el residuo de la división de 76 entre 10 es diferente de 0, el número de tarjeta no es válido.

El algoritmo debe mostrar: **"El número de tarjeta es inválido."**

Si el usuario ingresa un número que no tiene exactamente 16 dígitos, el algoritmo debe mostrar:  
**"Error: El número de tarjeta debe tener exactamente 16 dígitos. Intente de nuevo."**

---

### **Requerimientos**  
- El algoritmo debe permitir que el usuario ingrese solo números de tarjeta de crédito de **16 dígitos**.
- Si el número ingresado no tiene exactamente 16 dígitos, debe mostrar un mensaje de error y solicitar nuevamente el número.
- Debe utilizar estructuras de control iterativas del tipo **"Hacer... Repetir"**.
- No se pueden usar instrucciones rompedoras (como `romper`, `continuar` u otra similar) para finalizar el ciclo.
