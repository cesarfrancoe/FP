# **Guía de Ejemplos: Uso de la Estructura HACER…REPETIR HACER**

La presente guía reúne una serie de ejemplos clásicos y progresivos orientados a comprender el uso de la estructura iterativa *HACER…REPETIR HACER*. Cada 
ejemplo ha sido diseñado para ilustrar un patrón específico de aplicación, como el conteo, la acumulación, la validación de datos, el uso de valores centinela y 
el control de menús. Se emplea un pseudocódigo estandarizado que sigue las convenciones definidas en el curso, con el fin de reforzar buenas prácticas en 
la organización de algoritmos, la declaración de variables y la interacción con el usuario mediante instrucciones de entrada y salida. El objetivo es que 
no solo se entienda el funcionamiento de la estructura, sino que también identifique en qué contextos resulta más apropiada su utilización.

## 1. Patrón: Conteo (control por contador)

**Objetivo:** Repetir un bloque un número conocido de veces.

### Ejemplo 1: Mostrar números del 1 al 5

```text
ALGORITMO

VARIABLES
    contador COMO número entero

INICIO
    contador ← 1

    HACER
        ESCRIBIR contador
        contador ← contador + 1
    REPETIR HACER MIENTRAS QUE (contador ≤ 5)
FIN
```

---

## 2. Patrón: Acumulación

**Objetivo:** Acumular valores dentro del ciclo.

### Ejemplo 2: Sumar los primeros 5 números

```text
ALGORITMO

VARIABLES
    contador COMO número entero
    suma COMO número entero

INICIO
    contador ← 1
    suma ← 0

    HACER
        suma ← suma + contador
        contador ← contador + 1
    REPETIR HACER MIENTRAS QUE (contador ≤ 5)

    ESCRIBIR "Suma total:"
    ESCRIBIR suma
FIN
```

---

## 3. Patrón: Validación de entrada

**Objetivo:** Garantizar que el usuario ingrese datos válidos.

### Ejemplo 3: Validar número positivo

```text
ALGORITMO

VARIABLES
    numero COMO número entero

INICIO
    HACER
        ESCRIBIR "Ingrese un número positivo:"
        LEER numero

        SI (numero ≤ 0) ENTONCES
            ESCRIBIR "Error: el número debe ser mayor que cero"
        FIN SI
    REPETIR HACER MIENTRAS QUE (numero ≤ 0)

    ESCRIBIR "Número válido:"
    ESCRIBIR numero
FIN
```

---

### Ejemplo 4: Validar número en rango

```text
ALGORITMO

VARIABLES
    numero COMO número entero

INICIO
    HACER
        ESCRIBIR "Ingrese un número entre 10 y 20:"
        LEER numero

        SI (numero < 10 O numero > 20) ENTONCES
            ESCRIBIR "Error: el número debe estar entre 10 y 20"
        FIN SI
    REPETIR HACER MIENTRAS QUE (numero < 10 O numero > 20)

    ESCRIBIR "Número válido"
FIN
```

---

## 4. Patrón: Menú validado

**Objetivo:** Controlar opciones ingresadas por el usuario.

### Ejemplo 5: Validar opción de menú

```text
ALGORITMO

VARIABLES
    opcion COMO número entero

INICIO
    HACER
        HACER
            ESCRIBIR "1. Registrar"
            ESCRIBIR "2. Consultar"
            ESCRIBIR "3. Salir"
            ESCRIBIR "Seleccione una opción:"
            LEER opcion
    
            SI (opcion < 1 O opcion > 3) ENTONCES
                ESCRIBIR "Error: opción inválida"
            FIN_SI
        REPETIR HACER MIENTRAS QUE (opcion < 1 O opcion > 3)

        SI (opcion = 1) ENTONCES
            ESCRIBIR "Ralizar tarea de registrar..."
        SINO SI (opcion = 2) ENTONCES
            ESCRIBIR "Realizar tarea de consultar..."
        FIN_SI
        
    REPETIR HACE MIENTRAS QUE (opcion ≠ 3)
FIN
```

---

## 5. Patrón: Centinela

**Objetivo:** Repetir hasta que aparezca un valor especial de salida.

### Ejemplo 6: Sumar números hasta ingresar 0

```text
ALGORITMO

VARIABLES
    numero COMO número entero
    suma COMO número entero

INICIO
    suma ← 0

    HACER
        ESCRIBIR "Ingrese un número (0 para terminar):"
        LEER numero

        SI (numero ≠ 0) ENTONCES
            suma ← suma + numero
        FIN SI
    REPETIR HACER MIENTRAS QUE (numero ≠ 0)

    ESCRIBIR "Suma total:"
    ESCRIBIR suma
FIN
```

---

## 6. Patrón: Conteo condicional

**Objetivo:** Contar elementos que cumplen una condición.

### Ejemplo 7: Contar números pares

```text
ALGORITMO

VARIABLES
    numero COMO número entero
    contadorPares COMO número entero

INICIO
    contadorPares ← 0

    HACER
        ESCRIBIR "Ingrese un número (-1 para terminar):"
        LEER numero

        SI (numero ≠ -1) ENTONCES
            SI (numero MOD 2 = 0) ENTONCES
                contadorPares ← contadorPares + 1
            FIN SI
        FIN SI
    REPETIR HACER MIENTRAS QUE (numero ≠ -1)

    ESCRIBIR "Cantidad de números pares:"
    ESCRIBIR contadorPares
FIN
```

---

## 7. Patrón: Generación de series

**Objetivo:** Generar resultados sistemáticos.

### Ejemplo 8: Tabla de multiplicar del 3

```text
ALGORITMO

VARIABLES
    contador COMO número entero
    resultado COMO número entero

INICIO
    contador ← 1

    HACER
        resultado ← 3 * contador
        ESCRIBIR "3 x ", contador, " = ", resultado
        contador ← contador + 1
    REPETIR HACER MIENTRAS QUE (contador ≤ 10)
FIN
```
