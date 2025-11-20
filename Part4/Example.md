# 🧭 **Guía paso a paso – Ejercicio 400**

---

## 🎯 Objetivo

Implementar una función llamada `add` que reciba un arreglo de números enteros y retorne la sumatoria de sus elementos. Luego, construir un programa principal que:

* Solicite al usuario cuántos números va a ingresar.
* Lea los valores del arreglo desde teclado.
* Llame a la función `add` y muestre el resultado.

---

## 📄 Parte 1: Archivo `MathOper.java`

Este archivo contiene la función `add`.

---

### ✅ Paso 1: Crear el archivo `MathOper.java`

```java
public class MathOper {

    static int add(int[] nums) {

        // Aquí implementaremos la función paso a paso

    }

}
```

---

### ✅ Paso 2: Declarar e inicializar la variable acumuladora

```java
public class MathOper {

    static int add(int[] nums) {
        int sum = 0;

        // Aquí recorreremos el arreglo para sumar sus elementos
    }

}
```

---

### ✅ Paso 3: Recorrer el arreglo y retornar la suma

```java
public class MathOper {

    static int add(int[] nums) {
        int sum = 0;

        for (int k = 0; k < nums.length; k += 1) {
            sum += nums[k];
        }

        return sum;
    }

}
```

---

## 📄 Parte 2: Archivo `Ejer400.java`

Este archivo contiene el programa principal que prueba la función `add`.

---

### ✅ Estructura general

```java
import java.util.Scanner;
import java.io.PrintStream;

public class Ejer400 {
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
int[] numbers = new int[]{};
int sum = 0;
```

* `size`: cantidad de números que ingresará el usuario.
* `numbers`: arreglo para almacenar esos números.
* `sum`: resultado final de la suma.

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
for (int k = 0; k < numbers.lenth; k += 1) {
    screen.print("Enter number " + (k + 1) + ": ");
    numbers[k] = Integer.parseInt(keyboard.nextLine());
}
```

* Se recorre el arreglo con un ciclo `for`.
* En cada iteración, se solicita al usuario un número y se guarda en la posición `k` del arreglo.

---

### ✅ Paso 5: Llamar la función y mostrar el resultado

```java
sum = MathOper.add(numbers);
screen.println("Sum: " + sum);
```

---

## ✅ Código completo del archivo `Ejer400.java`

```java
import java.util.Scanner;
import java.io.PrintStream;

public class Ejer400 {
    static Scanner keyboard = new Scanner(System.in);
    static PrintStream screen = System.out;

    public static void main(String[] args) {
        int size = 0;
        int[] numbers = new int[]{};
        int sum = 0;

        screen.print("Enter the number of elements: ");
        size = Integer.parseInt(keyboard.nextLine());

        numbers = new int[size];

        for (int k = 0; k < numbers.length; k += 1) {
            screen.print("Enter number " + (k + 1) + ": ");
            numbers[k] = Integer.parseInt(keyboard.nextLine());
        }

        sum = MathOper.add(numbers);
        screen.println("Sum: " + sum);
    }
}
```

---

## ✅ Código completo del archivo `MathOper.java`

```java
public class MathOper {

    static int add(int[] nums) {
        int sum = 0;

        for (int k = 0; k < nums.length; k += 1) {
            sum += nums[k];
        }

        return sum;
    }

}
```
