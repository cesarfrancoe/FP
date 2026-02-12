### Problema 155 – Clasificación de rendimiento deportivo en competencia atlética

En una competencia atlética universitaria se desea clasificar el desempeño de los participantes en una prueba de resistencia, considerando no solo el tiempo registrado, sino también la categoría de edad y la frecuencia cardiaca promedio durante la prueba.

Para que un atleta pueda considerarse apto en la evaluación, su tiempo debe estar por debajo de un límite máximo establecido para su categoría de edad. Si supera dicho límite, su desempeño se clasifica automáticamente como insuficiente, independientemente de los demás indicadores.

Cuando el tiempo cumple con el requisito establecido, la clasificación final depende de la frecuencia cardiaca promedio. Si la frecuencia cardiaca se mantiene dentro del rango recomendado para su edad, el desempeño puede clasificarse como destacado si además el tiempo se encuentra dentro del 10% mejor respecto al límite permitido. Si la frecuencia cardiaca se encuentra ligeramente por encima del rango recomendado, el desempeño se clasifica como aceptable. Si la frecuencia cardiaca supera ampliamente el rango seguro, el resultado debe clasificarse como insuficiente por riesgo fisiológico.

Existe una condición adicional: si el atleta pertenece a la categoría juvenil, los límites de frecuencia cardiaca permitidos deben ajustarse con un margen superior adicional, sin que esto modifique el criterio del tiempo máximo permitido.

El algoritmo debe determinar si el desempeño es insuficiente, aceptable o destacado.

### Ejemplos de prueba

**Ejemplo 1**

Edad: 22
Categoría: Adulto
Tiempo registrado: 38
Tiempo máximo permitido: 45
Frecuencia cardiaca promedio: 155
Frecuencia máxima recomendada: 170

Resultado esperado:
Desempeño destacado

**Ejemplo 2**

Edad: 17
Categoría: Juvenil
Tiempo registrado: 42
Tiempo máximo permitido: 45
Frecuencia cardiaca promedio: 182
Frecuencia máxima recomendada: 175

Resultado esperado:
Desempeño aceptable

**Ejemplo 3**

Edad: 30
Categoría: Adulto
Tiempo registrado: 50
Tiempo máximo permitido: 45
Frecuencia cardiaca promedio: 160
Frecuencia máxima recomendada: 170

Resultado esperado:
Desempeño insuficiente
