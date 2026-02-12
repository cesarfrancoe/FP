### Problema 157 – Evaluación de observación astronómica

Un observatorio astronómico analiza datos registrados durante una sesión de observación nocturna para determinar la calidad de los registros obtenidos y la viabilidad de continuar con el estudio del objeto celeste.

El análisis comienza identificando el tipo de objeto observado, el cual puede ser “Planeta”, “Estrella” o “Galaxia”. Dependiendo del tipo de objeto, se consideran diferentes parámetros como relevantes.

Si el objeto observado es un Planeta, se evalúa principalmente la magnitud aparente y la estabilidad atmosférica registrada durante la observación. Si el objeto es una Estrella, además de la magnitud aparente se analiza su variabilidad luminosa. En el caso de una Galaxia, el parámetro más relevante es el nivel de interferencia lumínica y el tiempo efectivo de exposición.

La magnitud aparente debe encontrarse dentro de un rango observable por el telescopio utilizado; si no lo está, la observación se considera inválida independientemente de los demás parámetros.

Para que la sesión sea considerada de alta calidad, deben cumplirse las condiciones específicas del tipo de objeto y no debe existir interferencia significativa. Si algunas condiciones se cumplen pero otras no, la sesión se clasifica como calidad media. Si no se cumplen las condiciones mínimas, la observación se clasifica como inválida.

Además, si el tiempo efectivo de exposición es inferior al mínimo recomendado para el tipo de objeto, el sistema debe emitir una advertencia adicional indicando que los datos pueden ser insuficientes para análisis posterior.

El algoritmo debe:

* Determinar si la observación es inválida, de calidad media o de alta calidad.
* Emitir advertencia adicional cuando corresponda.

### Ejemplos de prueba

**Ejemplo 1**

Tipo de objeto: Estrella
Magnitud aparente: 3.5
Variabilidad luminosa: Baja
Interferencia lumínica: Baja
Tiempo de exposición: 120

Resultado esperado:
Observación de alta calidad

**Ejemplo 2**

Tipo de objeto: Galaxia
Magnitud aparente: 4.0
Interferencia lumínica: Media
Tiempo de exposición: 40

Resultado esperado:
Observación de calidad media
Advertencia: tiempo de exposición insuficiente

**Ejemplo 3**

Tipo de objeto: Planeta
Magnitud aparente: 9.5
Estabilidad atmosférica: Baja
Tiempo de exposición: 100

Resultado esperado:
Observación inválida


Si quieres, el siguiente puede ser en ingeniería o computación, incorporando dependencias aún más estrictas entre entradas.
