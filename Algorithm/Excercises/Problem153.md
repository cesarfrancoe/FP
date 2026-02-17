## Problema 153 – Evaluación de estado fisiológico en medicina deportiva

Un centro de medicina deportiva analiza el estado fisiológico de un atleta luego de una sesión de entrenamiento intensivo. El objetivo no es determinar una única categoría final, sino construir un perfil de recuperación basado en múltiples indicadores biométricos.

Se registran tres valores principales:

* Frecuencia cardiaca en reposo posterior al entrenamiento.
* Nivel de lactato en sangre.
* Porcentaje de hidratación corporal estimado.

Cada indicador se compara con su rango recomendado. Sin embargo, en lugar de clasificar cada uno de forma aislada, el sistema asigna un puntaje de recuperación según el comportamiento de cada parámetro.

Si la frecuencia cardiaca se encuentra dentro del rango recomendado, se asignan 2 puntos; si se encuentra ligeramente elevada, se asigna 1 punto; si supera significativamente el límite, no se asignan puntos.

El nivel de lactato aporta 2 puntos cuando está dentro del rango óptimo, 1 punto cuando se encuentra en nivel intermedio y 0 puntos cuando supera el límite máximo recomendado.

El porcentaje de hidratación aporta 2 puntos si es adecuado, 1 punto si está levemente por debajo del valor recomendado y 0 puntos si indica deshidratación marcada.

Al finalizar la evaluación, se calcula el puntaje total de recuperación.

* Si el puntaje total es 6, la recuperación se considera óptima.
* Si el puntaje está entre 3 y 5 inclusive, la recuperación se considera parcial.
* Si el puntaje es inferior a 3, la recuperación se considera insuficiente.

Además, si cualquiera de los tres indicadores se encuentra en nivel crítico (es decir, en su peor estado), el sistema debe emitir una advertencia médica independiente del puntaje total.

El algoritmo debe:

* Evaluar cada indicador.
* Asignar los puntos correspondientes.
* Calcular el puntaje total.
* Determinar el nivel de recuperación.
* Emitir advertencia cuando corresponda.


### Ejemplos de prueba

---

**Ejemplo 1**

Frecuencia cardiaca: Dentro de rango

Lactato: Óptimo

Hidratación: Adecuada

**Resultado esperado:**

Puntaje total: 6

Nivel de recuperación: Óptima

Sin advertencias

---

**Ejemplo 2**

Frecuencia cardiaca: Ligeramente elevada

Lactato: Intermedio

Hidratación: Adecuada

**Resultado esperado:**

Puntaje total: 4

Nivel de recuperación: Parcial

Sin advertencias

---

**Ejemplo 3**

Frecuencia cardiaca: Crítica

Lactato: Intermedio

Hidratación: Baja

**Resultado esperado:**

Puntaje total: 1

Nivel de recuperación: Insuficiente

Advertencia médica

