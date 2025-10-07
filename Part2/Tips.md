# Guía exprés de ciclos, contadores y acumuladores (con ejemplos en Java)

---

## 0) ¿Qué es un ciclo?

Un **ciclo** repite un bloque de instrucciones varias veces. En Java usaremos aquí solo `while` y `do...while`.

* `while (condición) { ... }` → **repite mientras** la condición sea **verdadera**.
* `do { ... } while (condición);` → ejecuta el bloque **al menos una vez** y luego **repite mientras** la condición sea **verdadera**.

---

## 1) Contador: ¿qué es y cuándo usarlo?

Un **contador** es una variable que **cuenta cuántas veces** ha pasado algo.
Casi siempre empieza en `0` y se incrementa de 1 en 1 (aunque puede ser otro paso).

**Plantilla (while):**

```java
import java.util.Scanner;

public class Example1 {
    static Scanner keyboard = new Scanner(System.in);

    public static void main(String[] args) {
        int count = 0;  // counts how many times something happens

        while (conditionIsTrue) {
            // ... do work
            count = count + 1;  // or: count += 1; or: count++;
        }
    }
}
```

**Plantilla (do...while):**

```java
import java.util.Scanner;

public class Example2 {
    static Scanner keyboard = new Scanner(System.in);

    public static void main(String[] args) {
        int count = 0;

        do {
            // ... do work
            count = count + 1;  // or: count += 1; or: count++;
        } while (conditionIsTrue);
    }
}
```

---

## 2) Acumulador: ¿qué es y por qué otra variable distinta?

Un **acumulador** guarda un **resultado parcial** que va **creciendo** (por ejemplo, una **suma** o un **producto**).

Debe ser una variable **diferente** al contador y al valor leído.

**Plantilla de suma con while:**

```java
import java.util.Scanner;

public class SumExample {
    static Scanner keyboard = new Scanner(System.in);

    public static void main(String[] args) {
        int sum = 0;  // accumulator
        int i = 0;    // counter

        System.out.print("How many numbers? ");
        int n = Integer.parseInt(keyboard.nextLine());

        while (i < n) {
            System.out.print("Enter number: ");
            int value = Integer.parseInt(keyboard.nextLine());

            sum = sum + value;  // or: sum += value;
            i = i + 1;          // or: i += 1; or: i++;
        }

        System.out.println("Sum = " + sum);
    }
}
```

---

## 3) “Haga **hasta**…” vs Java “haga **mientras**…”

En lenguaje natural decimos **“repetir hasta que pase X”**.
Eso significa que el ciclo **continúa mientras X no pase**.

En Java, la condición en el `while` se formula **en positivo**:

> “Repetir hasta que X ocurra” → `while (!X)`.

**Ejemplo:**

```java
do {
    // ...
} while (value != 0);   // "repetir hasta que value sea 0"
```

---

## 4) Patrones de oro

### A) N iteraciones conocidas (0 a N-1)

```java
import java.util.Scanner;

public class FixedLoop {
    static Scanner keyboard = new Scanner(System.in);

    public static void main(String[] args) {
        System.out.print("How many times? ");
        int n = Integer.parseInt(keyboard.nextLine());

        int i = 0;
        while (i < n) {
            System.out.println("Iteration: " + i);
            i = i + 1;  // or: i += 1; or: i++;
        }
    }
}
```

### B) Lista de datos hasta un “sentinela”

```java
import java.util.Scanner;

public class SentinelSum {
    static Scanner keyboard = new Scanner(System.in);

    public static void main(String[] args) {
        int sum = 0;
        int count = 0;

        System.out.print("Enter number (-1 to stop): ");
        int value = Integer.parseInt(keyboard.nextLine());  // priming read

        while (value != -1) {   // while NOT sentinel
            sum = sum + value;  // or: sum += value;
            count = count + 1;  // or: count += 1; or: count++;

            System.out.print("Enter number (-1 to stop): ");
            value = Integer.parseInt(keyboard.nextLine());  // update
        }

        System.out.println("Sum = " + sum);
        System.out.println("Count = " + count);
    }
}
```

### C) Validación de entrada (repetir hasta que sea válida)

```java
import java.util.Scanner;

public class ValidateInput {
    static Scanner keyboard = new Scanner(System.in);

    public static void main(String[] args) {
        int age;

        do {
            System.out.print("Enter age (0–120): ");
            age = Integer.parseInt(keyboard.nextLine());
        } while (age < 0 || age > 120);

        System.out.println("Valid age: " + age);
    }
}
```

### D) Búsqueda (repetir hasta encontrar)

```java
import java.util.Scanner;

public class FindNumber {
    static Scanner keyboard = new Scanner(System.in);

    public static void main(String[] args) {
        boolean found = false;
        int value;

        do {
            System.out.print("Enter a number: ");
            value = Integer.parseInt(keyboard.nextLine());

            if (value == 42) {
                found = true;
            }
        } while (!found);

        System.out.println("You found the secret number!");
    }
}
```

---

## 5) Ejemplos completos

### 5.1 Contar positivos (hasta ingresar 0)

```java
import java.util.Scanner;

public class CountPositives {
    static Scanner keyboard = new Scanner(System.in);

    public static void main(String[] args) {
        int count = 0;

        System.out.print("Enter number (0 to stop): ");
        int x = Integer.parseInt(keyboard.nextLine());

        while (x != 0) {
            if (x > 0) {
                count = count + 1;  // or: count += 1; or: count++;
            }
            System.out.print("Enter number (0 to stop): ");
            x = Integer.parseInt(keyboard.nextLine());
        }

        System.out.println("Positives: " + count);
    }
}
```

### 5.2 Promedio (sentinela = -1)

```java
import java.util.Scanner;

public class AveragePrices {
    static Scanner keyboard = new Scanner(System.in);

    public static void main(String[] args) {
        int sum = 0;
        int count = 0;

        System.out.print("Enter price (-1 to stop): ");
        int price = Integer.parseInt(keyboard.nextLine());

        while (price != -1) {
            sum = sum + price;      // or: sum += price;
            count = count + 1;      // or: count += 1; or: count++;
            System.out.print("Enter price (-1 to stop): ");
            price = Integer.parseInt(keyboard.nextLine());
        }

        if (count == 0) {
            System.out.println("No data.");
        } else {
            double average = (double) sum / (double) count;
            System.out.println("Average = " + average);
        }
    }
}
```

### 5.3 Menú (do...while)

```java
import java.util.Scanner;

public class SimpleMenu {
    static Scanner keyboard = new Scanner(System.in);

    public static void main(String[] args) {
        int option;

        do {
            System.out.println("1) Add");
            System.out.println("2) Subtract");
            System.out.println("3) Exit");

            option = Integer.parseInt(keyboard.nextLine());

            if (option == 1) {
                System.out.println("Adding...");
            } else if (option == 2) {
                System.out.println("Subtracting...");
            } else if (option != 3) {
                System.out.println("Invalid option");
            }
        } while (option != 3);
    }
}
```

---

## 6) Mini ejercicios (con tu configuración de lectura)

### A) Contar pares

```java
import java.util.Scanner;

public class CountEvens {
    static Scanner keyboard = new Scanner(System.in);

    public static void main(String[] args) {
        System.out.print("How many numbers? ");
        int n = Integer.parseInt(keyboard.nextLine());

        int i = 0;
        int countEven = 0;

        while (i < n) {
            System.out.print("Enter number: ");
            int x = Integer.parseInt(keyboard.nextLine());

            if (x % 2 == 0) {
                countEven = countEven + 1;  // or: countEven += 1; or: countEven++;
            }

            i = i + 1;  // or: i += 1; or: i++;
        }

        System.out.println("Even numbers: " + countEven);
    }
}
```

### B) Sumar hasta ingresar 0

```java
import java.util.Scanner;

public class SumUntilZero {
    static Scanner keyboard = new Scanner(System.in);

    public static void main(String[] args) {
        int sum = 0;

        System.out.print("Enter number (0 to stop): ");
        int x = Integer.parseInt(keyboard.nextLine());

        while (x != 0) {
            sum = sum + x;  // or: sum += x;
            System.out.print("Enter number (0 to stop): ");
            x = Integer.parseInt(keyboard.nextLine());
        }

        System.out.println("Total = " + sum);
    }
}
```

### C) Validar contraseña (máx. 3 intentos)

```java
import java.util.Scanner;

public class PasswordRetry {
    static Scanner keyboard = new Scanner(System.in);

    public static void main(String[] args) {
        String correct = "secret";
        int tries = 0;
        boolean ok = false;

        while (tries < 3 && !ok) {
            System.out.print("Enter password: ");
            String attempt = keyboard.nextLine();

            if (attempt.equals(correct)) {
                ok = true;
            } else {
                tries = tries + 1;  // or: tries += 1; or: tries++;
            }
        }

        if (ok) {
            System.out.println("Welcome!");
        } else {
            System.out.println("Blocked.");
        }
    }
}
