# **Tipos de Datos en Lenguajes de Programación**

Los tipos de datos son fundamentales en los lenguajes de programación, ya que determinan qué tipo de valores pueden almacenarse y cómo pueden manipularse en memoria. Se dividen en dos grandes categorías: **tipos de datos primitivos** y **tipos de datos no primitivos**.

---

## **1. Tipos de Datos Primitivos**
Los **tipos de datos primitivos** son los más básicos y esenciales dentro de un lenguaje de programación. Se almacenan directamente en la memoria y representan valores simples como números enteros, números de punto flotante, caracteres y valores booleanos.

### **1.1. Tipos de Datos con Signo**
Estos tipos de datos permiten representar tanto valores positivos como negativos.

| **Categoría**       | **Tipo de Dato** | **Tamaño (bytes)** | **Mínimo**                   | **Máximo**                    | **C**      | **Java**  | **C#**    | **Python**      | **Swift**  |
|---------------------|----------------|------------------|------------------------|------------------------|---------|---------|---------|--------------|---------|
| **Número Entero**        | `byte`         | 1                | -128                   | 127                    | `signed char` | `byte`  | `sbyte`  | `int`        | `Int8`   |
| **Número Entero**        | `short`        | 2                | -32,768                | 32,767                 | `short` | `short` | `short` | `int`        | `Int16`  |
| **Número Entero**        | `int`          | 4                | -2,147,483,648         | 2,147,483,647          | `int`   | `int`   | `int`   | `int`        | `Int32`  |
| **Número Entero**        | `long`         | 8                | -9,223,372,036,854,775,808 | 9,223,372,036,854,775,807 | `long`  | `long`  | `long`  | `int`        | `Int64`  |
| **Número Real** | `float`      | 4                | -3.4E+38               | 3.4E+38                 | `float` | `float` | `float` | `float`       | `Float`  |
| **Número Real** | `double`     | 8                | -1.7E+308              | 1.7E+308                | `double` | `double` | `double` | `float`       | `Double`  |
| **Booleano**      | `bool`         | 1                | `false`                | `true`                  | `_Bool` | `boolean` | `bool` | `bool`        | `Bool`   |
| **Caracter**     | `char`         | 1                | 0                      | 255                     | `char`  | `char`  | `char`  | `str (1 char)` | `Character` |

---

### **1.2. Tipos de Datos Sin Signo**
Estos tipos de datos solo permiten representar valores positivos, lo que les permite manejar un mayor rango de valores dentro del mismo tamaño en memoria.

| **Categoría**       | **Tipo de Dato**    | **Tamaño (bytes)** | **Mínimo** | **Máximo**                 | **C**              | **Java**        | **C#**      | **Python**       | **Swift**   |
|---------------------|----------------|------------------|----------|----------------------|----------------|---------------|------------|----------------|----------|
| **Número Entero**        | `unsigned byte`   | 1                | 0        | 255                  | `unsigned char` | No disponible | `byte`     | `int`          | `UInt8`   |
| **Número Entero**        | `unsigned short`  | 2                | 0        | 65,535               | `unsigned short` | No disponible | `ushort`   | `int`          | `UInt16`  |
| **Número Entero**        | `unsigned int`    | 4                | 0        | 4,294,967,295        | `unsigned int` | No disponible | `uint`     | `int`          | `UInt32`  |
| **Número Entero**        | `unsigned long`   | 8                | 0        | 18,446,744,073,709,551,615 | `unsigned long` | No disponible | `ulong`    | `int`          | `UInt64`  |
| **Caracter**     | `unsigned char`  | 1                | 0        | 255                  | `unsigned char` | No disponible | No disponible | `str (1 char)` | `Character` |

---

## **2. Tipos de Datos No Primitivos**
Los **tipos de datos no primitivos** son estructuras más complejas que agrupan múltiples valores y permiten manipular grandes volúmenes de información. Un ejemplo común es la **cadena de caracteres (`string`)**, la cual almacena secuencias de texto.

| **Categoría**       | **Tipo de Dato** | **Tamaño (bytes)**           | **Mínimo**      | **Máximo**      | **C**                     | **Java**   | **C#**    | **Python** | **Swift**  |
|---------------------|----------------|-----------------------------|---------------|---------------|-------------------------|------------|-----------|------------|-----------|
| **Cadenas de Texto** | `string` *     | Depende de la implementación | 0 caracteres  | Ilimitado    | `char[]` (arreglo de `char`) | `String`   | `string`  | `str`      | `String`  |

> *Nota:* `string` no es un tipo de dato primitivo, sino una estructura más compleja que almacena una secuencia de caracteres.

---

## **Conclusión**
Los tipos de datos primitivos son esenciales en la programación, ya que determinan cómo se almacenan y manipulan los valores en la memoria del sistema. Mientras que los **tipos primitivos** permiten representar valores numéricos, booleanos y caracteres de manera eficiente, los **tipos no primitivos** ofrecen mayor flexibilidad para manejar estructuras más complejas, como cadenas de texto y colecciones de datos.
