# Técnica de diseño algorítmico basada en salidas

## 1. Introducción

En el proceso de construcción de algoritmos es habitual comenzar identificando variables o escribiendo directamente instrucciones. Sin embargo, existe una técnica alternativa especialmente útil en problemas de clasificación o toma de decisiones.

Esta técnica consiste en diseñar el algoritmo partiendo de las **salidas posibles** y determinando posteriormente las condiciones que conducen a cada una de ellas.

El enfoque permite estructurar la lógica de manera clara, evitar redundancias y reducir ambigüedades antes de escribir el pseudocódigo.

---

## 2. Principio fundamental

Todo algoritmo de decisión puede entenderse como un sistema que clasifica una situación en uno o varios resultados posibles.

La técnica se basa en identificar primero los resultados y luego construir la lógica necesaria para alcanzarlos.

---

## 3. Metodología paso a paso

### Paso 1: Identificación de salidas

El primer paso consiste en enumerar explícitamente todas las salidas finales que puede producir el algoritmo.

Las salidas deben ser:

* Claramente diferenciables.
* Coherentes con el enunciado.
* Exhaustivas respecto al problema planteado.

Definir primero las salidas delimita completamente el espacio lógico del algoritmo.

---

### Paso 2: Asociación de condiciones a cada salida

Una vez identificadas las salidas, se analizan las condiciones que producen cada una.

En esta etapa se deben:

* Agrupar las condiciones que conducen al mismo resultado.
* Identificar condiciones eliminatorias.
* Detectar posibles caminos alternativos hacia una misma salida.
* Determinar si existe jerarquía en la evaluación.

Este análisis permite visualizar la estructura lógica antes de escribir instrucciones.

---

### Paso 3: Identificación de variables

Las variables no se determinan de manera arbitraria.

Surgen directamente de las condiciones identificadas.

Cada elemento que deba evaluarse en una condición implica la existencia de una variable.

Este enfoque garantiza coherencia entre el problema y el algoritmo.

---

### Paso 4: Determinación de entradas y procesos

Una vez definidas las variables, se establecen:

* Cuáles deben leerse como entradas.
* Cuáles se calculan internamente.
* Qué procesos deben realizarse.

Los procesos pueden incluir:

* Comparaciones relacionales.
* Cálculos aritméticos.
* Evaluaciones por rangos.
* Combinaciones lógicas.
* Asignaciones intermedias.

---

## 4. Jerarquización de salidas

No todas las salidas tienen el mismo peso lógico dentro del algoritmo.

En muchos problemas conviene comenzar el análisis por:

* Salidas eliminatorias.
* Resultados altamente restrictivos.
* Decisiones que, por sí solas, determinan inmediatamente el resultado.

Posteriormente se analizan:

* Clasificaciones principales.
* Salidas residuales o por descarte.

La jerarquización no depende únicamente del número de condiciones, sino del nivel de restricción lógica que representan.

---

## 5. Problemas con múltiples salidas simultáneas

No todos los problemas generan una única clasificación final.

Algunos requieren producir varias salidas independientes en la misma ejecución.

En estos casos:

* Las decisiones no son excluyentes.
* Pueden coexistir varios mensajes o estados.
* No existe una única categoría global.

Cuando esto ocurre, se recomienda dividir el análisis en **grupos lógicos independientes**.

---

### Aplicación de la técnica por grupos

Cada grupo debe analizarse de manera independiente:

1. Identificar sus salidas.
2. Determinar las condiciones correspondientes.
3. Identificar las variables necesarias.
4. Estructurar el bloque condicional del grupo.

Luego, los grupos se integran dentro del algoritmo general.

Esta separación evita mezclar decisiones que no pertenecen al mismo conjunto lógico.

---

## 6. Construcción estructural del algoritmo

Después del análisis basado en salidas, el algoritmo puede organizarse de forma clara:

* Primero, condiciones eliminatorias (si existen).
* Luego, clasificación principal.
* Finalmente, condiciones modificadoras o ajustes adicionales.
* En caso de múltiples grupos, bloques independientes organizados secuencialmente.

El pseudocódigo se convierte en una formalización de una lógica previamente estructurada.

---

## 7. Ventajas de la técnica

El diseño basado en salidas permite:

* Comprender completamente el problema antes de programar.
* Reducir anidamientos innecesarios.
* Agrupar condiciones equivalentes.
* Detectar inconsistencias tempranamente.
* Mejorar la claridad estructural del algoritmo.

---

## 8. Idea central

Un algoritmo de decisión no debe comenzar escribiendo instrucciones.

Debe comenzar identificando:

* Qué resultados son posibles.
* Qué condiciones producen esos resultados.
* Qué información es necesaria para evaluarlos.

Cuando estos elementos están claramente definidos, la escritura del pseudocódigo se convierte en una consecuencia natural del análisis lógico.

