### **Tipos de Datos Primitivos en Lenguajes de Programación**

Los tipos de datos primitivos son los elementos fundamentales en la mayoría de los lenguajes de programación. Representan valores básicos que pueden ser almacenados y manipulados en la memoria del sistema sin necesidad de estructuras adicionales. Estos tipos incluyen números enteros, números de punto flotante, caracteres y valores booleanos.  

En esta clasificación, los tipos de datos pueden dividirse en dos grupos principales:
1. **Tipos de datos con signo:** Permiten representar tanto valores positivos como negativos.
2. **Tipos de datos sin signo:** Solo permiten representar valores positivos, lo que permite un mayor rango de valores en el mismo número de bits.

A continuación, se presentan dos tablas que muestran los tipos de datos primitivos en diferentes lenguajes de programación, junto con su tamaño en bytes y los valores mínimo y máximo que pueden almacenar.

Aquí tienes las tablas en formato de texto para que puedas copiarlas y pegarlas fácilmente:

### **Tabla 1: Tipos de Datos Primitivos con Signo**

| **Categoría**   | **Tipo de Dato** | **Tamaño (bytes)** | **Mínimo**                   | **Máximo**                    | **C**      | **Java**  | **C#**    | **Python**      | **Swift**  |
|---------------|---------------|------------------|------------------------|------------------------|---------|---------|---------|--------------|---------|
| **Enteros**   | `byte`        | 1                | -128                   | 127                    | `signed char` | `byte`  | `sbyte`  | `int`        | `Int8`   |
| **Enteros**   | `short`       | 2                | -32,768                | 32,767                 | `short` | `short` | `short` | `int`        | `Int16`  |
| **Enteros**   | `int`         | 4                | -2,147,483,648         | 2,147,483,647          | `int`   | `int`   | `int`   | `int`        | `Int32`  |
| **Enteros**   | `long`        | 8                | -9,223,372,036,854,775,808 | 9,223,372,036,854,775,807 | `long`  | `long`  | `long`  | `int`        | `Int64`  |
| **Punto Flotante** | `float` | 4                | -3.4E+38               | 3.4E+38                 | `float` | `float` | `float` | `float`       | `Float`  |
| **Punto Flotante** | `double` | 8                | -1.7E+308              | 1.7E+308                | `double` | `double` | `double` | `float`       | `Double`  |
| **Booleanos** | `bool`        | 1                | `false`                | `true`                  | `_Bool` | `boolean` | `bool` | `bool`        | `Bool`   |
| **Caracteres** | `char`       | 1                | 0                      | 255                     | `char`  | `char`  | `char`  | `str (1 char)` | `Character` |

---

### **Tabla 2: Tipos de Datos Primitivos Sin Signo**

| **Categoría**   | **Tipo de Dato**    | **Tamaño (bytes)** | **Mínimo** | **Máximo**                 | **C**              | **Java**        | **C#**      | **Python**       | **Swift**   |
|---------------|----------------|------------------|----------|----------------------|----------------|---------------|------------|----------------|----------|
| **Enteros**   | `unsigned byte`   | 1                | 0        | 255                  | `unsigned char` | No disponible | `byte`     | `int`          | `UInt8`   |
| **Enteros**   | `unsigned short`  | 2                | 0        | 65,535               | `unsigned short` | No disponible | `ushort`   | `int`          | `UInt16`  |
| **Enteros**   | `unsigned int`    | 4                | 0        | 4,294,967,295        | `unsigned int` | No disponible | `uint`     | `int`          | `UInt32`  |
| **Enteros**   | `unsigned long`   | 8                | 0        | 18,446,744,073,709,551,615 | `unsigned long` | No disponible | `ulong`    | `int`          | `UInt64`  |
| **Caracteres** | `unsigned char`  | 1                | 0        | 255                  | `unsigned char` | No disponible | No disponible | `str (1 char)` | `Character` |
