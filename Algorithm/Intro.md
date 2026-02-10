# Pseudocódigo

**Curso: Fundamentos de Programación**

---

## 1. Introducción

El presente documento introduce el **pseudocódigo** como herramienta fundamental para el desarrollo de la lógica de programación. Su propósito es que el estudiante aprenda a **describir algoritmos de forma clara, ordenada y comprensible**, antes de trabajar con lenguajes de programación formales.

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

En este curso se trabajarán los siguientes tipos de datos:

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
  En este curso, el tipo lógico se entiende en sentido **booleano**, no como representación binaria interna del computador.

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

## 6. Procesos

Los procesos son las operaciones que transforman los datos de entrada en resultados.

Se expresan mediante asignaciones.

Ejemplos:

```text
promedio ← (nota1 + nota2 + nota3) / 3
total ← cantidad × precio
```

Primero se realiza el cálculo y luego se asigna el resultado a la variable correspondiente.

---

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

Forma general:

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

## 9. Condiciones y notación lógica

Las condiciones se expresan utilizando **notación matemática y lógica estándar**.

Simbología utilizada:

* `>`  mayor que
* `<`  menor que
* `≥`  mayor o igual que
* `≤`  menor o igual que
* `=`  igual a
* `≠`  diferente de

Ejemplos:

```text
edad ≥ 18
nota < 3.0
```

Estas expresiones deben leerse en lenguaje natural.

---

## 10. Ejemplo completo de algoritmo

```text
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
* Recordar que el pseudocódigo **describe**, no ejecuta

