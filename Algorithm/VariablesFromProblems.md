# Guía para identificar variables a partir de problemas

**Curso: Fundamentos de Programación**

---

## 1. Propósito de esta guía

El propósito de esta guía es ayudar a **identificar correctamente las variables** que se necesitan para resolver un problema, **antes** de escribir pseudocódigo.

Aprender a identificar variables es un paso fundamental, ya que:

* Permite comprender mejor el problema.
* Evita errores lógicos posteriores.
* Facilita la construcción del bloque VARIABLES del algoritmo.

Esta guía se centra únicamente en **análisis del problema**, no en programación.

---

## 2. ¿Qué es una variable?

Una variable representa **una información que puede cambiar** durante la ejecución de un algoritmo.

En un problema redactado, una variable suele corresponder a:

* Un dato que el usuario ingresa.
* Un valor que se calcula.
* Un resultado que se muestra.

Las variables **no son acciones**, **no son preguntas** y **no son decisiones**.

---

## 3. Lectura correcta del problema

Antes de pensar en variables, es necesario **leer el problema completo**, sin intentar resolverlo todavía.

Durante la lectura, el estudiante debe preguntarse:

* ¿Qué información se menciona?
* ¿Qué datos cambian de un caso a otro?
* ¿Qué valores se necesitan para obtener el resultado?

Las variables se identifican **a partir del texto**, no de la solución.

---

## 4. Identificación de variables de entrada

Las **variables de entrada** corresponden a los datos que el usuario debe proporcionar al algoritmo.

Preguntas guía:

* ¿Qué datos debe ingresar el usuario?
* ¿Qué información no conoce el algoritmo hasta que el usuario la escribe?
* ¿Qué valores aparecen como datos iniciales del problema?

### Ejemplo 1

**Problema:**
Un estudiante ingresa tres notas y el sistema calcula el promedio.

Variables de entrada:

* nota1
* nota2
* nota3

---

## 5. Identificación de variables de proceso

Las **variables de proceso** almacenan resultados intermedios o cálculos realizados por el algoritmo.

Preguntas guía:

* ¿Qué valores se calculan?
* ¿Qué resultados intermedios aparecen?
* ¿Qué operaciones matemáticas se realizan?

### Ejemplo 2

**Problema:**
Un estudiante ingresa tres notas y el sistema calcula el promedio.

Variable de proceso:

* promedio

---

## 6. Identificación de variables de salida

Las **variables de salida** corresponden a la información que el algoritmo muestra al usuario.

Preguntas guía:

* ¿Qué información se debe mostrar?
* ¿Cuál es el resultado final?
* ¿Qué espera ver el usuario?

### Ejemplo 3

**Problema:**
Un estudiante ingresa tres notas y el sistema calcula el promedio.

Variable de salida:

* promedio

Una misma variable puede ser **de proceso y de salida**.

---

## 7. Diferenciar variables de otros elementos

No todo lo que aparece en un problema es una variable.

### No son variables

* Acciones: calcular, mostrar, leer.
* Decisiones: aprobar, reprobar.
* Mensajes fijos: “Aprueba”, “Reprueba”.
* Operadores o comparaciones.

### Ejemplo

**Problema:**
Si el promedio es mayor o igual a 3.0, el estudiante aprueba.

Variables:

* promedio

No son variables:

* 3.0
* “Aprueba”
* “mayor o igual”

---

## 8. Asignación de tipo de dato a las variables

Una vez identificadas las variables, se asigna el **tipo de dato adecuado**, según la información que representan.

Guía general:

* Cantidades enteras → número entero
* Valores con decimales → número real
* Texto → cadena de caracteres
* Valores de verdad → lógico (booleano)

### Ejemplo

* edad → número entero
* promedio → número real
* nombre → cadena de caracteres
* aprobado → lógico (booleano)

---

## 9. Construcción del bloque VARIABLES

Después de identificar las variables y su tipo de dato, se construye el bloque VARIABLES.

### Ejemplo

**Problema:**
Un estudiante ingresa tres notas y se calcula el promedio.

```text
VARIABLES
    nota1 COMO número real
    nota2 COMO número real
    nota3 COMO número real
    promedio COMO número real
```

Este bloque se escribe **antes del INICIO** del algoritmo.

---

## 10. Ejercicio guiado

**Problema:**
Un empleado ingresa el número de horas trabajadas y el valor por hora.
El sistema calcula el salario total.

### Paso 1: Variables de entrada

* horasTrabajadas
* valorHora

### Paso 2: Variable de proceso

* salario

### Paso 3: Tipos de dato

* horasTrabajadas → número entero
* valorHora → número real
* salario → número real

### Paso 4: Bloque VARIABLES

```text
VARIABLES
    horasTrabajadas COMO número entero
    valorHora COMO número real
    salario COMO número real
```

---

## 11. Reglas generales

* Toda variable debe surgir del texto del problema.
* No se deben inventar variables innecesarias.
* Una variable representa una sola información.
* Los nombres deben ser claros y representativos.
* Primero se identifican variables, luego se escribe pseudocódigo.

