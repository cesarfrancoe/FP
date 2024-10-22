# **Estructuras de Control Iterativas**

Las **estructuras de control iterativas** permiten que un bloque de código se ejecute repetidamente bajo ciertas condiciones. En este documento unificamos todas las variantes de los ciclos iterativos bajo la estructura **"Hacer...Repetir"**, con dos opciones principales: **"Mientras que"** para evaluar condiciones verdaderas y **"Hasta que"** para evaluar cuando una condición se satisfaga.

---

### **1. `Hacer Mientras que...Repetir`**

En esta variante, el ciclo se ejecuta **mientras** la condición sea verdadera. La condición se evalúa **antes** de ejecutar el bloque de instrucciones. Si la condición es falsa desde el inicio, el ciclo no se ejecuta.

**Seudocódigo:**

```
Hacer Mientras que (condición)
    // Instrucciones a ejecutar mientras la condición sea verdadera
Repetir
```

**Ejemplo:**

```
k ← 1
Hacer Mientras que (k ≤ 5)
    Escribir "El valor de k es: ", k
    k ← k + 1
Repetir
```

En este caso, el ciclo se ejecuta mientras `k` sea menor o igual a 5.

---

### **2. `Hacer...Repetir Mientras que`**

En esta variante, el ciclo ejecuta las instrucciones **al menos una vez** y luego repite **mientras** la condición sea verdadera. La condición se evalúa **después** de ejecutar el bloque.

**Seudocódigo:**

```
Hacer
    // Instrucciones a ejecutar
Repetir Mientras que (condición)
```

**Ejemplo:**

```
k ← 1
Hacer
    Escribir "El valor de k es: ", k
    k ← k + 1
Repetir Mientras que (k ≤ 5)
```

En este caso, el ciclo se ejecutará al menos una vez y seguirá repitiendo mientras `k` sea menor o igual a 5.

---

### **3. `Hacer Hasta que...Repetir`**

En esta variante, el ciclo se ejecuta **hasta** que la condición se cumpla. La condición se evalúa **antes** de ejecutar el bloque de código, lo que significa que si la condición es verdadera desde el inicio, el ciclo no se ejecutará.

**Seudocódigo:**

```
Hacer Hasta que (condición)
    // Instrucciones a ejecutar mientras la condición sea falsa
Repetir
```

**Ejemplo:**

```
k ← 1
Hacer Hasta que (k > 5)
    Escribir "El valor de k es: ", k
    k ← k + 1
Repetir
```

En este caso, el ciclo seguirá ejecutándose hasta que `k` sea mayor que 5.

---

### **4. `Hacer...Repetir Hasta que`**

En esta variante, el ciclo ejecuta las instrucciones **al menos una vez** y luego sigue repitiendo **hasta** que la condición se cumpla. La condición se evalúa **después** de ejecutar el bloque de código.

**Seudocódigo:**

```
Hacer
    // Instrucciones a ejecutar
Repetir Hasta que (condición)
```

**Ejemplo:**

```
k ← 1
Hacer
    Escribir "El valor de k es: ", k
    k ← k + 1
Repetir Hasta que (k > 5)
```

En este caso, el ciclo se ejecutará al menos una vez y seguirá repitiéndose hasta que `k` sea mayor que 5.

---

### **Resumen de las Variantes del Ciclo `Hacer...Repetir` en Seudocódigo:**

1. **`Hacer Mientras que (condición)...Repetir`**: Evalúa la condición al inicio, el ciclo se ejecuta solo si la condición es verdadera y continúa mientras lo siga siendo.
2. **`Hacer...Repetir Mientras que (condición)`**: Evalúa la condición al final, el ciclo se ejecuta al menos una vez y continúa mientras la condición sea verdadera.
3. **`Hacer Hasta que (condición)...Repetir`**: Evalúa la condición al inicio, el ciclo se ejecuta mientras la condición sea falsa y continúa hasta que se cumpla.
4. **`Hacer...Repetir Hasta que (condición)`**: Evalúa la condición al final, el ciclo se ejecuta al menos una vez y continúa hasta que la condición se cumpla.
