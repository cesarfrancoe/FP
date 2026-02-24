### Problema 154 – Evaluación de viabilidad de lote agrícola

Un ingeniero agrónomo debe determinar si un lote de terreno es apto para la siembra de un cultivo específico. Para realizar la evaluación, el sistema debe recibir como datos de entrada suministrados por el usuario: el nivel de pH del suelo (valor real), la altitud sobre el nivel del mar en metros (valor real), la disponibilidad de agua expresada como categoría (“Alta”, “Media” o “Baja”) y el porcentaje de materia orgánica del suelo (valor real). Ninguno de estos valores se calcula mediante fórmula dentro del algoritmo; todos son ingresados directamente.

Para este cultivo, los criterios técnicos establecidos son los siguientes:

El rango aceptable de pH está definido por la condición 6.0 ≤ pH ≤ 7.0.

El rango permitido de altitud está definido por la condición 1_600 ≤ altitud ≤ 2_000 metros.

Si el pH se encuentra fuera del intervalo [6.0, 7.0] o la altitud se encuentra fuera del intervalo [1_600, 2_000], el lote se clasifica inmediatamente como “No apto para la siembra”.

Si el lote cumple simultáneamente las condiciones de pH y altitud, la clasificación depende de la disponibilidad de agua:

* Si la disponibilidad es “Baja”, el lote se clasifica como “No apto para la siembra”.
* Si la disponibilidad es “Media”, el lote se clasifica como “Viable con manejo técnico adicional”.
* Si la disponibilidad es “Alta”, el lote se clasifica inicialmente como “Óptimo para la siembra”.

Existe una condición adicional relacionada con el contenido de materia orgánica. Para este cultivo, el porcentaje mínimo recomendado es 3.0%. Si la clasificación inicial es “Óptimo para la siembra” pero la materia orgánica es menor que 3.0%, la clasificación debe modificarse a “Viable con manejo técnico adicional”.

La materia orgánica no puede convertir un lote “No apto” en viable ni en óptimo; únicamente puede degradar una clasificación inicialmente óptima.

El algoritmo debe determinar si el lote es “No apto para la siembra”, “Viable con manejo técnico adicional” u “Óptimo para la siembra”.

## Ejemplos de prueba ##

**Ejemplo 1**
pH: 6.5

Altitud: 1_800

Disponibilidad de agua: Alta

Materia orgánica: 4.0

**Resultado esperado:**

Óptimo para la siembra

**Ejemplo 2**
pH: 6.8

Altitud: 1_750

Disponibilidad de agua: Alta

Materia orgánica: 2.0

**Resultado esperado:** 

Viable con manejo técnico adicional

**Ejemplo 3**

pH: 5.0

Altitud: 2_100

Disponibilidad de agua: Media

Materia orgánica: 5.0

**Resultado esperado:** 

No apto para la siembra

