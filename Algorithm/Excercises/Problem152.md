## Problema 152 – Evaluación de eficiencia energética en sistemas industriales

Una empresa de ingeniería evalúa el desempeño energético de distintos sistemas industriales instalados en plantas de producción. La evaluación no es uniforme para todos los sistemas, ya que los criterios dependen del tipo de tecnología implementada.

Inicialmente se debe identificar el tipo de sistema, el cual puede ser “Eléctrico”, “Térmico” o “Híbrido”. Dependiendo del tipo, se consideran distintos parámetros para el análisis.

Para todos los sistemas se debe calcular el índice de eficiencia energética, definido como la relación entre la energía útil generada y la energía total consumida durante el periodo de medición.

Índice de eficiencia = (Energía útil generada / Energía total consumida) × 100

En los sistemas eléctricos, el índice mínimo aceptable es del 85%.

En los sistemas térmicos, el índice mínimo aceptable es del 75%.

En los sistemas híbridos, el índice mínimo aceptable es del 80%.

Adicionalmente, se define que todos los sistemas tienen como eficiencia técnica máxima teórica el 100%.

El margen de mejora potencial se calcula como:

Margen de mejora potencial = 100 − Índice de eficiencia

Este margen se expresa en porcentaje y representa cuánto podría incrementarse la eficiencia hasta alcanzar el máximo teórico.

Si el índice calculado se encuentra por debajo del mínimo correspondiente al tipo de sistema, el sistema se clasifica como "ineficiente".

Cuando el índice cumple el mínimo exigido, el sistema puede clasificarse como "eficiente estándar" o "eficiente optimizado". Para ello, se evalúa el margen de mejora potencial estimado por el equipo técnico.

* Si el margen de mejora potencial es inferior al 5%, el sistema se considera optimizado.

* Si el margen es igual o superior al 5%, el sistema se clasifica como eficiente estándar.

Existe una condición adicional para sistemas híbridos:
Si el consumo energético total supera un umbral crítico definido por la planta (es decir, Energía consumida > Consumo crítico de referencia), el sistema no puede clasificarse como “Eficiente optimizado”, incluso si su margen de mejora es menor que 5%. En ese caso se clasifica como “Eficiente estándar”.

Además, el algoritmo debe indicar de forma independiente si el consumo energético se encuentra en nivel crítico, lo cual ocurre cuando:
Energía consumida > Consumo crítico de referencia.

El algoritmo debe:

* Calcular el índice de eficiencia.
* Calcular el margen de mejora potencial.
* Determinar si el sistema es ineficiente, eficiente estándar u optimizado.
* Indicar adicionalmente si el consumo energético se encuentra en nivel crítico.

### Ejemplos de prueba

---

**Ejemplo 1**

Tipo de sistema: Eléctrico

Energía útil: 900

Energía consumida: 1000

Consumo crítico de referencia: 1200

**Resultado esperado:**

Eficiencia: Optimizado

Consumo dentro de rango normal

---

**Ejemplo 2**

Tipo de sistema: Térmico

Energía útil: 700

Energía consumida: 1000

Consumo crítico de referencia: 1200

**Resultado esperado:**

Eficiencia: Ineficiente

Consumo dentro de rango normal

---

**Ejemplo 3**

Tipo de sistema: Híbrido

Energía útil: 850

Energía consumida: 1000

Consumo crítico de referencia: 900

**Resultado esperado:**

Eficiencia: Eficiente estándar

Consumo en nivel crítico
