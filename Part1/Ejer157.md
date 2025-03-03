### **Problema 057: Validación del código ISBN de 10 Dígitos**

**Descripción del problema:**

Escribe un algoritmo que valide un código **ISBN** de **10 dígitos**. El último dígito del ISBN es un dígito de control que se calcula a partir de los primeros 9 dígitos utilizando el siguiente algoritmo.

#### Algoritmo para calcular el dígito de control:

1. Multiplica el primer dígito por 10, el segundo por 9, el tercero por 8, y así sucesivamente hasta el noveno dígito, que se multiplica por 2.
   
2. Suma todos los resultados de las multiplicaciones.

3. El dígito de control es el número que, sumado al resultado anterior, hace que el total sea divisible por 11. Si el dígito de control es 10, se representa como `'X'`.

#### Ejemplo:

Para el ISBN **030640615**:

1. Multiplicamos los primeros 9 dígitos:
   - 0 × 10 = 0
   - 3 × 9 = 27
   - 0 × 8 = 0
   - 6 × 7 = 42
   - 4 × 6 = 24
   - 0 × 5 = 0
   - 6 × 4 = 24
   - 1 × 3 = 3
   - 5 × 2 = 10

2. Suma de los resultados:
   - 0 + 27 + 0 + 42 + 24 + 0 + 24 + 3 + 10 = **130**

3. Para que el total sea divisible por 11, el dígito de control debe ser:
   - 11 - (130 % 11) = 11 - 9 = **2**

Por lo tanto, el ISBN completo es **0306406152**.

#### Requisitos:

1. Escribe un algoritmo que reciba como entrada los primeros 9 dígitos de un ISBN y calcule el dígito de control.

2. El algoritmo debe devolver el ISBN completo, incluyendo el dígito de control. Si el dígito de control es 10, debe representarse como `'X'`.

#### Entrada:

- El programa recibirá como entrada un número de 9 dígitos.

#### Salida:

- El programa debe imprimir el ISBN completo de 10 dígitos, con el dígito de control calculado.

#### Ejemplo:

Entrada:
```
Introduce los primeros 9 dígitos del ISBN: 
030640615
```

Salida:
```
El ISBN completo es: 0306406152
```

Otro ejemplo donde el dígito de control es 10:

Entrada:
```
Introduce los primeros 9 dígitos del ISBN: 
030640613
```

Salida:
```
El ISBN completo es: 030640613X
```
