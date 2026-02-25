# Pruebas de Escritorio (Desk Check)

Las pruebas de escritorio, también conocidas como *desk check*, son una técnica de verificación lógica que consiste en simular manualmente la ejecución de un algoritmo, registrando paso a paso el estado de sus variables y el flujo de control. No se ejecuta el algoritmo en un lenguaje de programación; se analiza su comportamiento siguiendo estrictamente el orden de las instrucciones.

Esta técnica permite detectar errores lógicos antes de la implementación, tales como condiciones mal formuladas, asignaciones incorrectas, variables no inicializadas o rutas que no se ejecutan. En el contexto formativo, fortalece la comprensión estructurada del flujo de ejecución y desarrolla el razonamiento algorítmico.

## ¿Para qué sirven las pruebas de escritorio?

Las pruebas de escritorio permiten:

* Verificar la coherencia lógica de un algoritmo.
* Detectar errores antes de programar.
* Validar que todas las ramas condicionales funcionen correctamente.
* Comprobar que las variables reciben valores adecuados.
* Analizar casos borde o situaciones especiales.
* Justificar formalmente el resultado de un algoritmo.

## Procedimiento para realizar una prueba de escritorio

1. Definir el objetivo del algoritmo.
2. Establecer valores de prueba para las entradas.
3. Numerar las líneas del algoritmo (entre INICIO y FIN).
4. Construir una tabla que contenga las variables relevantes.
5. Ejecutar línea por línea registrando los cambios de estado.
6. Comparar el resultado obtenido con el esperado.

---

# Ejemplo Completo

## Objetivo del algoritmo

Clasificar a una persona según su edad y determinar si puede ingresar a un evento.

## Valores de prueba

edad = 22

tieneBoleta = 1

Resultado esperado:

estadoEdad = "Mayor de edad"

categoria = "Adulto"

puedeIngresar = "Autorizado"

---

## Pseudocódigo

```text
ALGORITMO
VARIABLES
    edad COMO Entero
    tieneBoleta COMO Entero
    estadoEdad COMO Cadena
    categoria COMO Cadena
    puedeIngresar COMO Cadena

INICIO
1   ESCRIBIR "Ingrese la edad:"
2   LEER edad

3   ESCRIBIR "¿Tiene boleta? (1 = Sí, 0 = No):"
4   LEER tieneBoleta

5   SI (edad < 0) ENTONCES
6       estadoEdad ← "Edad inválida"
7   FIN SI

8   SI (edad ≥ 18) ENTONCES
9       estadoEdad ← "Mayor de edad"
10  FIN SI

11  SI (edad < 13) ENTONCES
12      categoria ← "Niño"
13  SINO SI (edad < 18) ENTONCES
14      categoria ← "Adolescente"
15  SINO
16      categoria ← "Adulto"
17  FIN SI

18  SI (edad ≥ 18 y tieneBoleta = 1) ENTONCES
19      puedeIngresar ← "Autorizado"
20  SINO
21      puedeIngresar ← "No autorizado"
22  FIN SI

23  ESCRIBIR categoria
24  ESCRIBIR estadoEdad
25  ESCRIBIR puedeIngresar
FIN
```

Características del ejemplo:

* Dos condicionales simples (líneas 5–7 y 8–10).
* Un condicional múltiple (líneas 11–17).
* Un condicional compuesto con lógica expresada en lenguaje natural (línea 18).
* Uso de simbología matemática (≥, <, =).
* Asignaciones realizadas con el operador ←.

---

## Tabla de prueba de escritorio

(edad = 22, tieneBoleta = 1)

| Paso | Línea ejecutada | edad | tieneBoleta | estadoEdad      | categoria | puedeIngresar |
| ---- | --------------- | ---- | ----------- | --------------- | --------- | ------------- |
| 1    | 1               | —    | —           | —               | —         | —             |
| 2    | 2               | 22   | —           | —               | —         | —             |
| 3    | 3               | 22   | —           | —               | —         | —             |
| 4    | 4               | 22   | 1           | —               | —         | —             |
| 5    | 5               | 22   | 1           | —               | —         | —             |
| 6    | 8               | 22   | 1           | —               | —         | —             |
| 7    | 9               | 22   | 1           | "Mayor de edad" | —         | —             |
| 8    | 11              | 22   | 1           | "Mayor de edad" | —         | —             |
| 9    | 16              | 22   | 1           | "Mayor de edad" | "Adulto"  | —             |
| 10   | 18              | 22   | 1           | "Mayor de edad" | "Adulto"  | —             |
| 11   | 19              | 22   | 1           | "Mayor de edad" | "Adulto"  | "Autorizado"  |
| 12   | 23              | 22   | 1           | "Mayor de edad" | "Adulto"  | "Autorizado"  |
| 13   | 24              | 22   | 1           | "Mayor de edad" | "Adulto"  | "Autorizado"  |
| 14   | 25              | 22   | 1           | "Mayor de edad" | "Adulto"  | "Autorizado"  |

---

## Análisis del resultado

* La condición edad < 0 es falsa, por lo tanto no se ejecuta la línea 6.
* La condición edad ≥ 18 es verdadera, por lo que se asigna estadoEdad.
* En el condicional múltiple, se ejecuta la rama SINO (línea 16).
* En el último condicional, ambas condiciones se cumplen (edad ≥ 18 y tieneBoleta = 1), por lo tanto se asigna puedeIngresar ← "Autorizado".

La prueba de escritorio confirma que el algoritmo produce el resultado esperado para los valores de prueba definidos.

---

## Conclusión

La prueba de escritorio es una técnica sistemática de verificación que permite analizar la ejecución de un algoritmo sin necesidad de implementarlo en un lenguaje de programación. Al registrar paso a paso el estado de las variables y asociarlo con la numeración de líneas, se obtiene una trazabilidad completa del flujo lógico, lo que facilita la detección temprana de errores y mejora la calidad del diseño algorítmico.
