### **Estructuras de Control Selectivas**

Las **estructuras de control selectivas** permiten que un programa tome decisiones dependiendo de ciertas condiciones. Estas decisiones influyen en el flujo de ejecución, permitiendo ejecutar diferentes bloques de código según el resultado de las condiciones evaluadas.

### **1. Estructura `Si`**

La estructura más básica es la sentencia `Si`. Permite que se ejecute un bloque de código solo si una condición es verdadera.

**Sintaxis en pseudocódigo:**

```
Si (condición) Entonces
    // código a ejecutar si la condición es verdadera
Fin Si
```

**Ejemplo:**

```
Si (edad >= 18) Entonces
    Escribir "Eres mayor de edad"
Fin Si
```

### **2. Estructura `Si - Sino`**

El bloque `Si - Sino` permite ejecutar un bloque de código cuando la condición es verdadera y otro bloque cuando es falsa.

**Sintaxis en pseudocódigo:**

```
Si (condición) Entonces
    // código a ejecutar si la condición es verdadera
Sino
    // código a ejecutar si la condición es falsa
Fin Si
```

**Ejemplo:**

```
Si (numero > 0) Entonces
    Escribir "El número es positivo"
Sino
    Escribir "El número no es positivo"
Fin Si
```

### **3. Estructura `Si - Sino Si - Sino`**

Cuando se necesita evaluar múltiples condiciones, se pueden utilizar varios bloques `Sino Si`. De este modo, si la primera condición es falsa, se pasa a la siguiente, y así sucesivamente. Si ninguna condición es verdadera, se ejecuta el bloque `Sino`.

**Sintaxis en pseudocódigo:**

```
Si (condición1) Entonces
    // código a ejecutar si la condición1 es verdadera
Sino Si (condición2) Entonces
    // código a ejecutar si la condición2 es verdadera
Sino
    // código a ejecutar si ninguna condición es verdadera
Fin Si
```

**Ejemplo:**

```
Si (calificación >= 90) Entonces
    Escribir "Excelente"
Sino Si (calificación >= 70) Entonces
    Escribir "Aprobado"
Sino
    Escribir "Reprobado"
Fin Si
```

### **Comparación entre las Estructuras**

- **`Si`**: Evalúa una única condición. Si es verdadera, ejecuta el bloque de código; si es falsa, no hace nada.
- **`Si - Sino`**: Evalúa una condición. Si es verdadera, ejecuta un bloque de código; si es falsa, ejecuta otro bloque.
- **`Si - Sino Si - Sino`**: Permite evaluar múltiples condiciones de forma secuencial. Ejecuta el primer bloque de código cuya condición sea verdadera.

### **Resumen**

Las estructuras de control selectivas son fundamentales para que los programas tomen decisiones. Nos permiten controlar el flujo del programa dependiendo de las condiciones que se evalúan durante la ejecución. Usar las estructuras `Si`, `Si - Sino`, y `Si - Sino Si - Sino` de forma adecuada es esencial para la creación de programas que se adapten a diferentes situaciones.
