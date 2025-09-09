# Guía: Creación y uso de la clase `SysIO.java`

## 1) ¿Qué es `SysIO` y para qué sirve?

`SysIO` es un **contenedor de código de tipo clase (class)** que centraliza las operaciones básicas de **entrada** (leer desde el teclado) y **salida** (escribir en pantalla).

Ventajas para principiantes:

* Simplifica el uso de `System.in` y `System.out`.
* Evita repetir código de configuración de entrada/salida.
* Evita el error clásico de mezclar `nextInt()` y `nextLine()`: aquí siempre se lee con `readLine()` y luego se convierte al tipo numérico necesario.

---

## 2) Crear el archivo `SysIO.java`

1. En tu proyecto Java, ubica la carpeta de código fuente (por ejemplo, `src/`).
2. Crea un archivo nuevo llamado **`SysIO.java`**.
3. Pega el código:

```java
import java.io.PrintStream;
import java.util.Scanner;

public class SysIO {

    // Single, shared input stream from keyboard
    private static Scanner keyboard = new Scanner(System.in);

    // Single, shared output stream to screen
    private static PrintStream screen = System.out;

    // Reads a full line from the keyboard and returns it as String
    public static String readLine(){
        return keyboard.nextLine();
    }

    // Prints any object followed by a newline
    public static void writeLine(Object object){
        screen.println(object);
    }
}
```

---

## 3) ¿Cómo usar `SysIO` en tus programa?

Creamos una clase llamada `Program.java` que **extiende** de `SysIO`.
De esta manera, podemos usar directamente `readLine()` y `writeLine()`.

```java
public class Program extends SysIO {
    public static void main(String[] args) {
        // Direct use of inherited static methods
        writeLine("What is your name?");
        String name = readLine();

        writeLine("How old are you?");
        String ageText = readLine();
        
        int age = Integer.parseInt(ageText);

        writeLine("Hello, " + name + "! You are " + age + " years old.");
    }
}
```

---

## 4) Ejecución típica

```
What is your name?
> Ana
How old are you?
> 20
Hello, Ana! You are 20 years old.
```

---

## 5) Mensaje final

* `SysIO` **centraliza** la entrada/salida.
* Con `extends SysIO`, el código se hace aún más simple y legible.
* Siempre lee cadenas (`String`) y conviértelas a números solo cuando lo necesites.
* Practica creando tus propios métodos en `SysIO` para validar entradas.
