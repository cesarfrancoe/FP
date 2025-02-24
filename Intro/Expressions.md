# Expresiones

Las expresiones son combinaciones de valores, operadores y variables que producen un resultado. Se utilizan en la programación para realizar cálculos, comparaciones y toma de decisiones. A continuación, se explican los principales tipos de expresiones.

---

## 1. Expresiones Matemáticas

Las expresiones matemáticas (también llamadas aritméticas) utilizan operadores matemáticos para realizar cálculos numéricos. Los operadores principales son:

| Operador | Descripción            | Ejemplo       | Resultado |
| -------- | ---------------------- | ------------- | --------- |
| `+`      | Suma                   | `5 + 3`       | `8`       |
| `-`      | Resta                  | `10 - 4`      | `6`       |
| `×`      | Multiplicación         | `7 × 2`       | `14`      |
| `÷`      | División               | `20 ÷ 5`      | `4`       |
| `mod`    | Módulo (residuo)       | `10 mod 3`    | `1`       |
| `^`      | Exponenciación         | `2 ^ 3`       | `8`       |
| `()`     | Paréntesis (prioridad) | `(2 + 3) × 4` | `20`      |

> **Nota:** Aunque en matemáticas la expresión `a = b = c` puede interpretarse como una cadena de igualdades, en la mayoría de los lenguajes de programación no está permitida de esta forma. En su lugar, debe escribirse de manera explícita como `(a = b) ∧ (b = c)`, asegurando que cada comparación se evalúe correctamente.

---

## 2. Expresiones Relacionales

Las expresiones relacionales comparan dos valores y devuelven un resultado booleano (`verdadero` o `falso`). Los operadores relacionales son:

| Operador | Descripción       | Ejemplo | Resultado   |
| -------- | ----------------- | ------- | ----------- |
| `>`      | Mayor que         | `5 > 3` | `verdadero` |
| `<`      | Menor que         | `2 < 7` | `verdadero` |
| `≥`      | Mayor o igual que | `4 ≥ 4` | `verdadero` |
| `≤`      | Menor o igual que | `3 ≤ 5` | `verdadero` |
| `=`      | Igualdad          | `5 = 5` | `verdadero` |
| `≠`      | Diferente         | `5 ≠ 3` | `verdadero` |

Las expresiones relacionales se utilizan en estructuras de control como condicionales (`SI`, `SEGÚN`) y bucles (`MIENTRAS`, `PARA`).

---

## 3. Expresiones Lógicas

Las expresiones lógicas permiten combinar valores booleanos utilizando operadores lógicos. Se utilizan principalmente para la toma de decisiones en los programas. Los operadores principales son:

| Operador | Descripción     | Ejemplo             | Resultado   |
| -------- | --------------- | ------------------- | ----------- |
| `∧`      | Y lógico        | `(5 > 3) ∧ (2 < 4)` | `verdadero` |
| `∨`      | O lógico        | `(5 > 3) ∨ (2 > 4)` | `verdadero` |
| `¬`      | Negación lógica | `¬(5 > 3)`          | `falso`     |

> **Nota:** En matemáticas, la notación `a(b + c)` es válida e implica una multiplicación implícita. Sin embargo, en la mayoría de los lenguajes de programación, es necesario escribirla de forma explícita como `a * (b + c)` para evitar errores de interpretación.

### Tabla de la Verdad

La tabla de la verdad muestra el resultado de las combinaciones posibles de los operadores lógicos:

| A         | B         | A ∧ B     | A ∨ B     | ¬A        |
| --------- | --------- | --------- | --------- | --------- |
| verdadero | verdadero | verdadero | verdadero | falso     |
| verdadero | falso     | falso     | verdadero | falso     |
| falso     | verdadero | falso     | verdadero | verdadero |
| falso     | falso     | falso     | falso     | verdadero |

Las expresiones lógicas son esenciales en las decisiones de flujo de control y validaciones en programación.

---

## Conclusión

Las expresiones matemáticas, relacionales y lógicas son fundamentales en la programación. Se combinan para construir condiciones complejas, realizar cálculos y controlar el flujo de ejecución de los programas. Comprender su funcionamiento es esencial para escribir código eficiente y lógico.

