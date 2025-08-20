# Java para principiantes

## Introducción

El lenguaje de programación Java es uno de los más utilizados en la enseñanza de la programación debido a su sintaxis clara y a su amplia difusión en la industria. Sin embargo, Java es un lenguaje orientado a objetos y contiene muchos elementos que no son necesarios para un curso inicial de fundamentos de programación. En este documento se presentan únicamente los elementos básicos necesarios para que un estudiante principiante pueda comprender y desarrollar sus primeros programas. El objetivo es enfocarse en la lógica, el uso de variables, las estructuras de control, las entradas y salidas, y las funciones sencillas, dejando de lado conceptos avanzados como modificadores de acceso, herencia o polimorfismo.

## 1. Identificadores en Java

En el lenguaje de programación Java, un **identificador** es el nombre que se le da a un elemento del programa, como un contenedor de código, una variable o una función. Los identificadores permiten referirse a estos elementos de manera única dentro del programa.

Las reglas básicas para escribir identificadores son:

* Deben comenzar con una letra, un guion bajo `_` o el signo dólar `$`.
* Después pueden incluir letras, números, guiones bajos o signos de dólar.
* No pueden contener espacios.
* No pueden ser palabras reservadas del lenguaje (por ejemplo, `class`, `int`, `if`).

Ejemplos de identificadores válidos:

```
age
userName
BankAccount
_sum
$counter
```

Ejemplos de identificadores no válidos:

```
1number   // no puede empezar por número
user name // no puede contener espacios
class     // es palabra reservada
```

Aunque en el lenguaje de programación Java es posible usar identificadores en español, **es altamente recomendado** escribirlos en inglés, ya que este es el idioma estándar en el desarrollo de software a nivel mundial. Esto facilita la compatibilidad internacional, el acceso a documentación y librerías, y responde a las buenas prácticas profesionales.

### Convenciones de escritura

Además de las reglas formales, existen convenciones de escritura habituales y recomendadas en el lenguaje de programación Java que facilitan la lectura y el mantenimiento del código.

**Upper Camel Case**
La mecánica consiste en escribir varias palabras sin usar ningún tipo de carácter de separación, donde la primera letra de cada palabra se escribe en mayúscula y las demás en minúscula.

| Identificador válido | Ejemplo válido |
| -------------------- | -------------- |
| `BankAccount`        | Ejemplo válido |
| `StudentRecord`      | Ejemplo válido |

**Camel Case**
La mecánica consiste en escribir varias palabras sin usar ningún tipo de carácter de separación, donde la primera palabra se escribe completamente en minúscula y la primera letra de cada palabra siguiente se escribe en mayúscula y las demás en minúscula.

| Identificador válido | Ejemplo válido |
| -------------------- | -------------- |
| `userName`           | Ejemplo válido |
| `calculateTotal`     | Ejemplo válido |

Aunque el uso de `_` o `$` al inicio de un identificador es válido en el lenguaje de programación Java, no es recomendable en el ámbito académico ni profesional, ya que puede causar confusión. **Es altamente recomendado** iniciar siempre con una letra y seguir estas convenciones.

## 2. Estructura mínima de un programa en Java

En el lenguaje de programación Java, todo programa debe escribirse dentro de un **contenedor de código de tipo clase (class)**. Para crearlo se utiliza la palabra reservada `class`, que el lenguaje tiene definida específicamente con ese propósito. Este contenedor necesita un identificador, que en el ejemplo es `Program`. El nombre puede ser cualquiera mientras sea un identificador válido y el archivo debe guardarse con ese mismo nombre seguido de la extensión `.java`.

Todo contenedor de código debe tener un **bloque de código**, el cual se escribe entre llaves `{ }`. Dentro de ese bloque se colocarán los elementos que pertenezcan al contenedor.

### Ejemplo de contenedor tipo clase vacío:

```java
class Program {
    // Aquí se escribirá el contenido del programa
}
```

En este punto, el programa no hace nada, pero la estructura mínima ya está definida: un contenedor de código de tipo clase (class) con su identificador y su bloque de código.

* **`class`** es una **palabra reservada** del lenguaje de programación Java utilizada para crear un contenedor de código de tipo clase (class).
* **`Program`** es el **identificador** de este contenedor y **es altamente recomendado** escribirlo usando **Upper Camel Case**.
* Cada contenedor tiene un **bloque de código** delimitado por llaves `{ }`, dentro del cual se ubican todo lo que pertenezca a este contenedor.
  
Dentro de este contenedor se debe incluir la **función principal (main function)** llamada `main`. Esta función es obligatoria en todos los programas y señala el punto donde inicia la ejecución.

### Ejemplom de contenedor tipo función (dentro de un contenedor tipo clase):

```java
class Program {
    public static void main(String[] args) {
        // Aquí irán las instrucciones del programa
    }
}
```

### Explicación

* Dentro de este contenedor  de clase `Program` se encuentra un contenedor tipo **función** llamada `main` (main es un contenedor especial tipo funcion).
* Cada contenedor tiene un **bloque de código** delimitado por llaves `{ }`, dentro del cual se ubican las instrucciones correspondientes.

### Notas sobre la main function

* **`public`**: palabra reservada necesaria en la definición de la main function. Su explicación detallada no es relevante en este curso inicial.
* **`static`**: palabra reservada necesaria para que la main function pueda ejecutarse correctamente. Su explicación detallada no es necesaria en este curso, ya que pertenece al paradigma de programación orientado a objetos.
* **`void`**: palabra reservada que indica que la función no devuelve ningún valor. Se verá en detalle más adelante, cuando se estudie el tema completo de contenedores de código de tipo función.
* **`String`**: es un **tipo de dato no primitivo** que debe escribirse tal como aparece en la main function. Todavía no es necesario comprenderlo; se explicará más adelante en el tema de tipos de datos no primitivos.
* **`[]`**: indica que se trata de un arreglo estático. Por ahora basta con reconocerlo como parte de la sintaxis obligatoria de la main function.
* **`args`**: es el identificador del arreglo de parámetros de la main function. Aunque no se utilizará en esta etapa, siempre debe escribirse de esta forma para que la función principal sea válida.
