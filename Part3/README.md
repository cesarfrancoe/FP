# **Estructuras de Control Iterativas**

Las **estructuras de control iterativas** permiten que un bloque de código se ejecute repetidamente bajo ciertas condiciones. En este documento unificamos todas las variantes de los ciclos iterativos bajo la estructura **"Hacer...Repetir"**, con dos opciones principales: **"Mientras que"** para evaluar condiciones verdaderas y **"Hasta que"** para evaluar cuando una condición se satisfaga.

---

### **1. `Hacer Mientras que...Repetir Hacer`**

En esta variante, el ciclo se ejecuta **mientras** la condición sea verdadera. La condición se evalúa **antes** de ejecutar el bloque de instrucciones. Si la condición es falsa desde el inicio, el ciclo no se ejecuta.

**Seudocódigo:**

```
Hacer Mientras que (condición)
    // Instrucciones a ejecutar mientras la condición sea verdadera
Repetir Hacer
```

**Ejemplo:**

```
k ← 1
Hacer Mientras que (k ≤ 5)
    Escribir "El valor de k es: ", k
    k ← k + 1
Repetir Hacer
```

En este caso, el ciclo se ejecuta mientras `k` sea menor o igual a 5.

---

### **2. `Hacer...Mientras que (condición) Repetir Hacer`**

En esta variante, el ciclo ejecuta las instrucciones **al menos una vez** y luego repite **mientras** la condición sea verdadera. La condición se evalúa **después** de ejecutar el bloque.

**Seudocódigo:**

```
Hacer
    // Instrucciones a ejecutar
Mientras que (condición) Repetir Hacer
```

**Ejemplo:**

```
k ← 1
Hacer
    Escribir "El valor de k es: ", k
    k ← k + 1
Mientras que (k ≤ 5) Repetir Hacer
```

En este caso, el ciclo se ejecutará al menos una vez y seguirá repitiendo mientras `k` sea menor o igual a 5.

---

### **3. `Hacer Hasta que...Repetir Hacer`**

En esta variante, el ciclo se ejecuta **hasta** que la condición se cumpla. La condición se evalúa **antes** de ejecutar el bloque de código, lo que significa que si la condición es verdadera desde el inicio, el ciclo no se ejecutará.

**Seudocódigo:**

```
Hacer Hasta que (condición)
    // Instrucciones a ejecutar mientras la condición sea falsa
Repetir Hacer
```

**Ejemplo:**

```
k ← 1
Hacer Hasta que (k > 5)
    Escribir "El valor de k es: ", k
    k ← k + 1
Repetir Hacer
```

En este caso, el ciclo seguirá ejecutándose hasta que `k` sea mayor que 5.

**Nota**: En lugar de usar **Hasta que (condición)**, podemos usar **Mientras que NO (condición)** para obtener el mismo comportamiento. Por ejemplo:

```
Hacer Mientras que NO (k > 5)
    // Instrucciones a ejecutar
Repetir Hacer
```

Además, otra forma de obtener el mismo comportamiento es invertir la condición. En lugar de **Hasta que (k > 5)**, podrías usar **Mientras que (k ≤ 5)**. Por ejemplo:

```
Hacer Mientras que (k ≤ 5)
    // Instrucciones a ejecutar
Repetir Hacer
```

Ambas soluciones ofrecen el mismo comportamiento en cuanto a la ejecución del ciclo.

---

### **4. `Hacer...Hasta que (condición) Repetir Hacer`**

En esta variante, el ciclo ejecuta las instrucciones **al menos una vez** y luego sigue repitiendo **hasta** que la condición se cumpla. La condición se evalúa **después** de ejecutar el bloque de código.

**Seudocódigo:**

```
Hacer
    // Instrucciones a ejecutar
Hasta que (condición) Repetir Hacer
```

**Ejemplo:**

```
k ← 1
Hacer
    Escribir "El valor de k es: ", k
    k ← k + 1
Hasta que (k > 5) Repetir Hacer
```

En este caso, el ciclo se ejecutará al menos una vez y seguirá repitiéndose hasta que `k` sea mayor que 5.

**Nota**: En lugar de **Repetir Hasta que (condición)**, podemos usar **Repetir Mientras que NO (condición)** después de la primera ejecución. Por ejemplo:

```
Hacer
    // Instrucciones a ejecutar
Mientras que NO (k > 5) Repetir Hacer
```

Además, otra alternativa es invertir la condición. En lugar de **Hasta que (k > 5)**, podemos usar **Mientras que (k ≤ 5)**. Por ejemplo:

```
Hacer
    // Instrucciones a ejecutar
Mientras que (k ≤ 5) Repetir Hacer
```

Ambas soluciones ofrecen el mismo comportamiento en cuanto a la ejecución del ciclo.

---

### **Resumen**

1. **`Hacer Mientras que (condición)...Repetir Hacer`**: Evalúa la condición al inicio, el ciclo se ejecuta solo si la condición es verdadera y continúa mientras lo siga siendo.
2. **`Hacer...Mientras que (condición) Repetir Hacer`**: Evalúa la condición al final, el ciclo se ejecuta al menos una vez y continúa mientras la condición sea verdadera.
3. **`Hacer Hasta que (condición)...Repetir Hacer`**: Evalúa la condición al inicio, el ciclo se ejecuta mientras la condición sea falsa y continúa hasta que se cumpla. Esta estructura puede reemplazarse por **Hacer Mientras que NO (condición)** o invertir la condición directamente.
4. **`Hacer...Hasta que (condición) Repetir Hacer`**: Evalúa la condición al final, el ciclo se ejecuta al menos una vez y continúa hasta que la condición se cumpla. Esta estructura puede reemplazarse por **Repetir Mientras que NO (condición)** o invertir la condición directamente.
