### **Problema 058: Validación de Números de Tarjeta de Crédito**

**Descripción del problema:**

Escribe un algoritmo que valide si un número de tarjeta de crédito de **16 dígitos** es correcto utilizando el **algoritmo de Luhn**. Este algoritmo es utilizado ampliamente por las principales empresas de tarjetas de crédito para verificar que un número de tarjeta sea válido.

#### Explicación del algoritmo de Luhn:

El algoritmo de Luhn sigue los siguientes pasos:

1. **Comienza desde el último dígito** (el dígito de verificación) y avanza hacia el primer dígito.
   
2. **Duplica cada segundo dígito**, comenzando desde el penúltimo dígito hacia la izquierda. Si el resultado de la duplicación es mayor que 9, se deben sumar los dígitos del número resultante (o restar 9).
   
3. **Suma todos los dígitos**, tanto los duplicados como los no duplicados.

4. **Verifica**: Si la suma total es divisible entre 10, entonces el número de la tarjeta es válido.

#### Ejemplo de aplicación del algoritmo:

Consideremos el número de tarjeta **4539 1488 0343 6467**.

1. **Identificamos los dígitos en posiciones pares** (contando desde el penúltimo dígito):
   - Posición 2: **6**
   - Posición 4: **6**
   - Posición 6: **4**
   - Posición 8: **0**
   - Posición 10: **8**
   - Posición 12: **1**
   - Posición 14: **3**
   - Posición 16: **4**

2. **Duplicamos los dígitos en posiciones pares**:
   - 6 × 2 = 12 → 1 + 2 = 3
   - 6 × 2 = 12 → 1 + 2 = 3
   - 4 × 2 = 8
   - 0 × 2 = 0
   - 8 × 2 = 16 → 1 + 6 = 7
   - 1 × 2 = 2
   - 3 × 2 = 6
   - 4 × 2 = 8

3. **Sumamos los dígitos duplicados y ajustados**:
   - 3 + 3 + 8 + 0 + 7 + 2 + 6 + 8 = **37**

4. **Sumamos los dígitos en posiciones impares (sin duplicar)**:
   - 7 + 4 + 3 + 8 + 4 + 9 + 5 = **40**

5. **Suma total**:
   - 37 + 40 = **77**

6. Como **77 % 10 ≠ 0**, el número **no es válido**.

#### Requisitos:

1. Escribe un algoritmo que valide un número de tarjeta de crédito de **exactamente 16 dígitos** utilizando este algoritmo.

2. **No se permite el uso de ciclos**. El programa debe implementar el algoritmo de validación utilizando únicamente estructuras de control de selección (`if...else`).

#### Entrada:

- El programa debe recibir como entrada un número de tarjeta de crédito de **16 dígitos** (del tipo `long`).

#### Salida:

- El programa debe imprimir `"Válido"` si el número de tarjeta de crédito es correcto según el algoritmo de Luhn, o `"Inválido"` en caso contrario.

#### Ejemplo:

Entrada:
```
Introduce el número de tarjeta de crédito de 16 dígitos: 
4539148803436467
```

Salida:
```
Inválido
```

Otro ejemplo:

Entrada:
```
Introduce el número de tarjeta de crédito de 16 dígitos: 
1234567812345670
```

Salida:
```
Inválido
```
