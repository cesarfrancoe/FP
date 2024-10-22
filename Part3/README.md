### **Estructuras de Control Iterativas**

Las **estructuras de control iterativas** permiten que un bloque de código se ejecute repetidamente mientras se cumpla una condición o hasta que una condición se satisfaga. En este documento, unificaremos las variantes del ciclo iterativo bajo la estructura **"Hacer...Repetir"**.

---

### **1. `Hacer...Repetir Mientras`**

Esta estructura ejecuta un bloque de código **mientras** una condición sea verdadera. La condición se evalúa **después** de ejecutar el bloque de código, garantizando que el ciclo se ejecute al menos una vez.

**Sintaxis en pseudocódigo:**

```
Hacer
    // Instrucciones a ejecutar
Repetir Mientras (condición)
```

**Ejemplo:**

```
i = 1
Hacer
    Escribir "El valor de i es: ", i
    i = i + 1
Repetir Mientras (i <= 5)
```

En este caso, el ciclo se ejecutará al menos una vez, y seguirá repitiendo mientras `i` sea menor o igual a 5.

---

### **2. `Hacer...Repetir Hasta`**

Esta estructura ejecuta un bloque de código **hasta** que una condición se cumpla. La condición se evalúa **después** de ejecutar el bloque de código, lo que garantiza que el ciclo se ejecute al menos una vez.

**Sintaxis en pseudocódigo:**

```
Hacer
    // Instrucciones a ejecutar
Repetir Hasta (condición)
```

**Ejemplo:**

```
i = 1
Hacer
    Escribir "El valor de i es: ", i
    i = i + 1
Repetir Hasta (i > 5)
```

En este ejemplo, el ciclo se ejecutará al menos una vez, y seguirá repitiendo hasta que `i` sea mayor que 5.

---

### **3. `Repetir Mientras`**

En esta estructura, el ciclo se ejecuta **mientras** la condición sea verdadera. La condición se evalúa **antes** de ejecutar el bloque de código, por lo que si la condición es falsa desde el principio, el ciclo no se ejecutará.

**Sintaxis en pseudocódigo:**

```
Repetir Mientras (condición)
    // Instrucciones a ejecutar mientras la condición sea verdadera
Fin Repetir
```

**Ejemplo:**

```
i = 1
Repetir Mientras (i <= 5)
    Escribir "El valor de i es: ", i
    i = i + 1
Fin Repetir
```

En este caso, el ciclo seguirá repitiéndose mientras `i` sea menor o igual a 5.

---

### **4. `Repetir Hasta`**

En esta estructura, el ciclo se ejecuta **hasta** que la condición se cumpla. La condición se evalúa **antes** de ejecutar el bloque de código, por lo que si la condición es verdadera desde el principio, el ciclo no se ejecutará.

**Sintaxis en pseudocódigo:**

```
Repetir Hasta (condición)
    // Instrucciones a ejecutar mientras la condición sea falsa
Fin Repetir
```

**Ejemplo:**

```
i = 1
Repetir Hasta (i > 5)
    Escribir "El valor de i es: ", i
    i = i + 1
Fin Repetir
```

En este caso, el ciclo se repetirá hasta que `i` sea mayor que 5.

---

### **Resumen de las Variantes del Ciclo `Hacer...Repetir` en Seudocódigo:**

1. **`Hacer...Repetir Mientras (condición)`**: Evalúa la condición al final; el ciclo se ejecuta al menos una vez y se repite mientras la condición sea verdadera.
2. **`Hacer...Repetir Hasta (condición)`**: Evalúa la condición al final; el ciclo se ejecuta al menos una vez y se repite hasta que la condición se cumpla.
3. **`Repetir Mientras (condición)`**: Evalúa la condición al inicio; el ciclo se repite mientras la condición sea verdadera.
4. **`Repetir Hasta (condición)`**: Evalúa la condición al inicio; el ciclo se repite hasta que la condición se cumpla.
