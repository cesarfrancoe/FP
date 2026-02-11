# Pseudocódigo

**Curso: Fundamentos de Programación**

---

## 1. Introducción

El presente documento introduce el **pseudocódigo** como herramienta fundamental para el desarrollo de la lógica de programación. Su propósito es **describir algoritmos de forma clara, ordenada y comprensible**, antes de trabajar con lenguajes de programación formales.

El enfoque del documento se centra en:

* Identificación de entradas, procesos y salidas
* Uso del pseudocódigo como lenguaje descriptivo
* Empleo de notación matemática y lógica estándar
* Uso de estructuras de control secuenciales y selectivas

---

## 2. Pseudocódigo

El pseudocódigo es una forma de describir un algoritmo utilizando **lenguaje natural estructurado**, apoyado en notación matemática y lógica.

El pseudocódigo:

* No se ejecuta
* No se compila
* No pertenece a ningún lenguaje de programación

Su función es **representar la lógica de una solución**, no su implementación técnica.

---

## 3. Estructura general de un algoritmo

Todo algoritmo descrito en pseudocódigo debe presentar:

* Un bloque de variables
* Un inicio claramente definido
* Un conjunto ordenado de instrucciones
* Un final explícito

Estructura general:

```text
ALGORITMO
VARIABLES
    declaración de variables

INICIO
    instrucciones
FIN
```

Las instrucciones se ejecutan **en el orden en que aparecen**, de arriba hacia abajo.

---

## 4. Variables

### 4.1 Bloque VARIABLES

El bloque **VARIABLES** se utiliza para indicar **qué información** empleará el algoritmo y **qué tipo de dato** almacena cada variable.

Este bloque es **descriptivo** y se escribe **antes del INICIO**, ya que no representa ejecución de instrucciones.

Forma general:

```text
VARIABLES
    nombreVariable COMO tipoDeDato
```

---

### 4.2 Tipos de datos básicos

* **Número entero**
  Valores numéricos sin parte decimal.

* **Número real**
  Valores numéricos que pueden contener parte decimal.

* **Carácter**
  Un único símbolo.

* **Cadena de caracteres**
  Texto.

* **Lógico (booleano)**
  Representa valores de verdad: **Verdadero** o **Falso**.
  El tipo lógico se entiende en sentido **booleano**, es decir, como representación de valores de verdad, y no como representación binaria interna.

Estos tipos de datos se utilizan para **razonar sobre la información**, no para validar sintaxis ni estudiar representación física.

---

## 5. Entrada de datos

La entrada de datos corresponde a la información que el usuario ingresa al algoritmo **mediante el teclado**.

Se representa mediante la instrucción:

* **LEER**

Ejemplos:

```text
LEER edad
LEER nota
```

Todo dato que se utilice en el algoritmo debe haber sido leído previamente.

---

## 6. Procesos y asignación

Los procesos son las operaciones que transforman los datos de entrada en resultados.

En pseudocódigo, los procesos se expresan mediante **asignaciones**.

Una asignación es una instrucción que:

* Evalúa una expresión.
* Almacena el resultado en una variable.

La asignación modifica el valor almacenado en una variable.

Se utiliza como símbolo:

```
←
```

Este símbolo se lee como:

> “recibe”, “guarda” o “almacena”.

Se emplea este símbolo de forma generalizada en pseudocódigo porque permite diferenciar claramente la **asignación** de la **igualdad matemática**. El símbolo `=` se utiliza en expresiones relacionales para establecer igualdad, mientras que `←` representa una operación de almacenamiento.

La forma general de una asignación es:

```text
variable ← expresión
```

Reglas para escribir una asignación:

* A la izquierda debe haber **una sola variable**.
* A la derecha puede haber:

  * Un valor.
  * Otra variable.
  * Una expresión matemática.
  * Una expresión relacional.
  * Una expresión lógica.

Ejemplos:

```text
promedio ← (nota1 + nota2 + nota3) / 3
total ← cantidad × precio
edad ← 18
esMayor ← edad ≥ 18
resultado ← numero1 > numero2
```

En los últimos ejemplos, la expresión produce un valor lógico (Verdadero o Falso), que puede almacenarse en una variable de tipo lógico.

Orden de ejecución:

1. Primero se evalúa la expresión que está a la derecha.
2. Luego el resultado se almacena en la variable que está a la izquierda.


## 7. Salida de datos

La salida de datos corresponde a la información que el algoritmo entrega al usuario **a través de la pantalla**.

Se representa mediante la instrucción:

* **ESCRIBIR**

Ejemplos:

```text
ESCRIBIR promedio
ESCRIBIR "Aprueba"
```

Todo algoritmo debe producir al menos una salida.

---

## 8. Estructuras de control

### 8.1 Estructura secuencial

Es la estructura básica del algoritmo.
Las instrucciones se ejecutan una después de la otra, en el orden establecido.

---

### 8.2 Estructura selectiva (SI)

La estructura selectiva permite ejecutar diferentes instrucciones dependiendo de una condición lógica.

### Forma básica

```text
SI (condición) ENTONCES
    instrucciones
FIN SI
```

Con alternativa:

```text
SI (condición) ENTONCES
    instrucciones
SINO
    instrucciones
FIN SI
```

Solo uno de los bloques se ejecuta.

---

### Forma extendida con múltiples condiciones

Cuando se necesitan evaluar varias condiciones excluyentes, se puede utilizar la forma:

```text
SI (condición1) ENTONCES
    instrucciones
SINO SI (condición2) ENTONCES
    instrucciones
SINO
    instrucciones
FIN SI
```

Las condiciones se evalúan en el orden en que aparecen.
Solo se ejecuta el bloque correspondiente a la **primera condición verdadera**.

Las condiciones deben ser mutuamente excluyentes para evitar ambigüedad en la ejecución.

---

## 9. Condiciones, operadores y expresiones lógicas

Una **condición** es una expresión que produce un valor lógico:
**Verdadero** o **Falso**.

Las condiciones se utilizan en las estructuras selectivas.

---

### 9.1 Operadores relacionales

Permiten comparar valores.

Simbología utilizada:

* `>`   mayor que
* `<`   menor que
* `≥`   mayor o igual que
* `≤`   menor o igual que
* `=`   igual a
* `≠`   diferente de

Ejemplos:

```text
edad ≥ 18
nota < 3.0
numero1 = numero2
```

Una expresión relacional produce un valor lógico.

---

### 9.2 Operadores lógicos

Permiten combinar condiciones.

Operadores utilizados:

* **Y**   (conjunción lógica)
* **O**   (disyunción lógica)
* **NO**  (negación lógica)

---

### 9.3 Expresiones lógicas compuestas

Una expresión lógica compuesta combina dos o más condiciones mediante operadores lógicos.

Ejemplos:

```text
edad ≥ 18 Y edad ≤ 60
nota ≥ 3.0 O recuperacion = Verdadero
NO (edad ≥ 18)
```

Reglas básicas:

* La expresión completa debe producir un valor lógico.
* Las condiciones combinadas deben estar claramente delimitadas.
* Las condiciones deben ser mutuamente excluyentes para evitar ambigüedad en la ejecución.

---

### 9.4 Diferencia entre asignación y comparación

Es importante diferenciar:

* `←`  asignación (almacena un valor).
* `=`  comparación (evalúa igualdad).

Ejemplo:

```text
edad ← 18        ← asignación
edad = 18        ← comparación
```

La asignación no produce un valor lógico, mientras que la comparación sí genera un resultado Verdadero o Falso.

---

## 10. Ejemplo completo de algoritmo

```text
ALGORITMO
VARIABLES
    nota COMO número real

INICIO
    LEER nota

    SI (nota ≥ 3.0) ENTONCES
        ESCRIBIR "Aprueba"
    SINO
        ESCRIBIR "Reprueba"
    FIN SI
FIN
```

---

## 11. Reglas generales para escribir pseudocódigo

* Usar nombres de variables claros y representativos
* Declarar todas las variables en el bloque VARIABLES
* Leer los datos antes de utilizarlos
* Usar notación matemática y lógica
* Mantener una escritura clara y ordenada
* El pseudocódigo describe la lógica de un algoritmo, no su ejecución.

