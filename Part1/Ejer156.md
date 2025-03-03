### **Problema 156: Número mágico de 4 dígitos**

**Descripción del problema:**

Escribe un algoritmo que verifique si un número de **4 dígitos** es un **número mágico**. Un número mágico es aquel que, al sumar sus dígitos repetidamente hasta obtener un solo dígito, el resultado es **1**.

#### Reglas:

1. El programa debe recibir un número entero positivo de **4 dígitos**.

2. El programa debe sumar los dígitos del número. Si el resultado tiene más de un dígito, debe sumar los dígitos de ese resultado y repetir hasta que obtenga un solo dígito.

3. Si el resultado final es **1**, el número es un número mágico.

#### Ejemplo:

- Para el número **1234**:
  - 1 + 2 + 3 + 4 = 10
  - 1 + 0 = 1 (Número mágico)

- Para el número **9876**:
  - 9 + 8 + 7 + 6 = 30
  - 3 + 0 = 3 (No es un número mágico)

#### Requisitos:

1. Escribe un algoritmo que reciba un número entero positivo de **4 dígitos**.

2. El algoritmo debe realizar las sumas de los dígitos de manera fija, utilizando solo estructuras de control de selección (`if...else`) para determinar si es necesario realizar una segunda suma.

#### Entrada:

- El programa recibirá como entrada un número entero positivo de 4 dígitos.

#### Salida:

- El programa debe imprimir `"Es un número mágico"` si la suma de los dígitos termina en 1, o `"No es un número mágico"` en caso contrario.

#### Ejemplo:

Entrada:
```
Introduce un número de 4 dígitos: 
1234
```

Salida:
```
Es un número mágico
```

Otro ejemplo:

Entrada:
```
Introduce un número de 4 dígitos: 
9876
```

Salida:
```
No es un número mágico
```
