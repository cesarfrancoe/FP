## Problema 152 – Evaluación de eficiencia energética en sistemas industriales

Una empresa de ingeniería evalúa el desempeño energético de distintos sistemas industriales instalados en plantas de producción. La evaluación no es uniforme para todos los sistemas, ya que los criterios dependen del tipo de tecnología implementada.

Inicialmente se debe identificar el tipo de sistema, el cual puede ser “Eléctrico”, “Térmico” o “Híbrido”. Dependiendo del tipo, se consideran distintos parámetros para el análisis.

Para todos los sistemas se debe calcular el índice de eficiencia energética, definido como la relación entre la energía útil generada y la energía total consumida durante el periodo de medición.

En los sistemas eléctricos, el índice mínimo aceptable es del 85%.

En los sistemas térmicos, el índice mínimo aceptable es del 75%.

En los sistemas híbridos, el índice mínimo aceptable es del 80%.

Si el índice calculado se encuentra por debajo del mínimo correspondiente al tipo de sistema, el sistema se clasifica como ineficiente.

Cuando el índice cumple el mínimo exigido, el sistema puede clasificarse como eficiente estándar o eficiente optimizado. Para ello, se evalúa el margen de mejora potencial estimado por el equipo técnico.

Si el margen de mejora potencial es inferior al 5%, el sistema se considera optimizado.

Si el margen es igual o superior al 5%, el sistema se clasifica como eficiente estándar.

Existe una condición adicional:
En sistemas híbridos, si el consumo energético total supera un umbral crítico definido por la planta, el sistema no puede clasificarse como optimizado, incluso si el margen de mejora es bajo.

El algoritmo debe:

* Calcular el índice de eficiencia.
* Determinar si el sistema es ineficiente, eficiente estándar u optimizado.
* Indicar adicionalmente si el consumo energético se encuentra en nivel crítico.

### Ejemplos de prueba

---

**Ejemplo 1**

Tipo de sistema: Eléctrico
Energía útil: 900
Energía consumida: 1000
Margen de mejora potencial: 3
Consumo crítico de referencia: 1200

**Resultado esperado:**

Eficiencia: Optimizado
Consumo dentro de rango normal

---

**Ejemplo 2**

Tipo de sistema: Térmico
Energía útil: 700
Energía consumida: 1000
Margen de mejora potencial: 10
Consumo crítico de referencia: 1200

**Resultado esperado:**

Eficiencia: Ineficiente
Consumo dentro de rango normal

---

**Ejemplo 3**

Tipo de sistema: Híbrido
Energía útil: 850
Energía consumida: 1000
Margen de mejora potencial: 2
Consumo crítico de referencia: 900

**Resultado esperado:**

Eficiencia: Eficiente estándar
Consumo en nivel crítico
