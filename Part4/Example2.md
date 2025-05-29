# 🧭 **Guía paso a paso – Ejercicio 402 (`add`)**

---

## 🎯 Objetivo

Construir una función que reciba:

* Un arreglo de números enteros.
* Un número entero.

Y retorne un **nuevo arreglo** donde cada elemento sea la suma del número recibido más el elemento original del arreglo.

---

## 📄 Parte 1: Archivo `MathOper.java`

Este archivo contiene la función `add` del Ejercicio 402.

---

### ✅ Paso 1: Crear el archivo `MathOper.java` (si no lo ha creado)

```java
public class MathOper {

    static int[] add(int[] nums, int value) {

        // Aquí implementaremos la función paso a paso

    }

}
```

---

### ✅ Paso 2: Declarar e inicializar las variables

```java
public class MathOper {

    static int[] add(int[] nums, int value) {
        int[] result = new int[nums.length];

        // Aquí llenaremos el nuevo arreglo
    }

}
```

* `nums.length`: tamaño del arreglo original.
* `result`: nuevo arreglo donde se almacenarán los valores calculados.

---

### ✅ Paso 3: Recorrer el arreglo y aplicar la operación

```java
public class MathOper {

    static int[] add(int[] nums, int value) {
        int[] result = new int[nums.length;];

        for (int k = 0; k < nums.length; k += 1) {
            result[k] = nums[k] + value;
        }

        return result;
    }

}
```

---

## 📄 Parte 2: Archivo `Ejer402.java`

Este archivo contiene el programa principal que prueba la función del Ejercicio 402.

---

### ✅ Estructura general

```java
import java.util.Scanner;
import java.io.PrintStream;

public class Ejer402 {
    static Scanner keyboard = new Scanner(System.in);
    static PrintStream screen = System.out;

    public static void main(String[] args) {
        // Instrucciones paso a paso
    }
}
```

---

### ✅ Paso 1: Declarar e inicializar variables al inicio

```java
int size = 0;
int[] numbers;
int[] results;
int value = 0;
```

* `size`: tamaño del arreglo.
* `numbers`: arreglo original ingresado por el usuario.
* `results`: nuevo arreglo con el resultado.
* `value`: número que se sumará a cada elemento del arreglo.

---

### ✅ Paso 2: Leer la cantidad de elementos

```java
screen.print("Enter the number of elements: ");
size = Integer.parseInt(keyboard.nextLine());
```

---

### ✅ Paso 3: Crear el arreglo con ese tamaño

```java
numbers = new int[size];
```

---

### ✅ Paso 4: Leer los valores que ingresa el usuario y asignarlos a una posición del arreglo

```java
for (int k = 0; k < numbers.length; k += 1) {
    screen.print("Enter number " + (k + 1) + ": ");
    numbers[k] = Integer.parseInt(keyboard.nextLine());
}
```

---

### ✅ Paso 5: Leer el número que se sumará a cada elemento

```java
screen.print("Enter the number to add to each element: ");
value = Integer.parseInt(keyboard.nextLine());
```

---

### ✅ Paso 6: Llamar la función y mostrar el resultado

```java
results = MathOper.add(numbers, value);

screen.println("New array:");
for (int k = 0; k < results.length; k += 1) {
    screen.println("Position " + k + ": " + results[k]);
}
```

---

## ✅ Código completo del archivo `Ejer402.java`

```java
import java.util.Scanner;
import java.io.PrintStream;

public class Ejer402 {
    static Scanner keyboard = new Scanner(System.in);
    static PrintStream screen = System.out;

    public static void main(String[] args) {
        int size = 0;
        int[] numbers;
        int[] results;
        int value = 0;

        screen.print("Enter the number of elements: ");
        size = Integer.parseInt(keyboard.nextLine());

        numbers = new int[size];

        for (int k = 0; k < numbers.length; k += 1) {
            screen.print("Enter number " + (k + 1) + ": ");
            numbers[k] = Integer.parseInt(keyboard.nextLine());
        }

        screen.print("Enter the number to add to each element: ");
        value = Integer.parseInt(keyboard.nextLine());

        results = MathOper.add(numbers, value);

        screen.println("New array:");
        for (int k = 0; k < results.length; k += 1) {
            screen.println("Position " + k + ": " + results[k]);
        }
    }
}
```

---

## ✅ Código completo del archivo `MathOper.java`

```java
public class MathOper {

    static int[] add(int[] nums, int value) {
        int[] result = new int[nums.length;];

        for (int k = 0; k < nums.length; k += 1) {
            result[k] = nums[k] + value;
        }

        return result;
    }

}
```
