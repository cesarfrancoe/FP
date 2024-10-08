### Problema 57: Validación de números de tarjeta de crédito

**Descripción del problema:**

Escribe un algoritmo que valide si un número de tarjeta de crédito de **16 dígitos** es correcto utilizando el **algoritmo de Luhn**. Este algoritmo es utilizado ampliamente por las principales empresas de tarjetas de crédito para verificar que un número de tarjeta sea válido.

#### Explicación del algoritmo de Luhn:

El algoritmo de Luhn sigue los siguientes pasos:

1. **Comienza desde el último dígito** (el dígito de verificación) y avanza hacia el primer dígito.
   
2. **Duplica cada segundo dígito** desde el penúltimo dígito hacia el primero. Si el resultado de la duplicación es mayor que 9, se debe restar 9 (o sumar los dígitos resultantes).
   
3. **Suma todos los dígitos** (tanto los duplicados como los no duplicados).

4. **Verifica**: Si la suma total es divisible entre 10, entonces el número de la tarjeta es válido.

#### Ejemplo de aplicación del algoritmo:

Para el número de tarjeta **4539 1488 0343 6467**:

1. Duplica cada segundo dígito desde el penúltimo:
   - Duplicar 6 → 6 × 2 = 12 → 1 + 2 = 3
   - Duplicar 4 → 4 × 2 = 8
   - Duplicar 3 → 3 × 2 = 6
   - Duplicar 0 → 0 × 2 = 0
   - Duplicar 8 → 8 × 2 = 16 → 1 + 6 = 7
   - Duplicar 9 → 9 × 2 = 18 → 1 + 8 = 9
   - Duplicar 5 → 5 × 2 = 10 → 1 + 0 = 1

2. Suma todos los dígitos:
   - 7 + 3 + 6 + 4 + 3 + 8 + 7 + 0 + 3 + 6 + 4 + 8 + 9 + 1 = **69**

3. Como **69 % 10 ≠ 0**, el número no es válido.

#### Requisitos:

1. Escribe un programa en Java que valide un número de tarjeta de crédito de **exactamente 16 dígitos** utilizando este algoritmo.

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
Válido
```

Entrada:
```
Introduce el número de tarjeta de crédito de 16 dígitos: 
1234567812345670
```

Salida:
```
Inválido
```

---
