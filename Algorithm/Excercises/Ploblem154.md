### Problema 153 – Evaluación de viabilidad de lote agrícola

Un ingeniero agrónomo debe determinar si un lote de terreno es apto para la siembra de un cultivo específico. La decisión no depende únicamente del tipo de suelo, sino también del nivel de acidez, la disponibilidad de agua y la altitud sobre el nivel del mar.

Para que el lote pueda considerarse viable, el nivel de pH del suelo debe encontrarse dentro de un rango adecuado para el cultivo y la altitud debe estar dentro de los límites recomendados. Si alguno de estos dos factores se encuentra fuera del rango permitido, el lote se clasifica como no apto.

Cuando el lote cumple las condiciones básicas de pH y altitud, la clasificación final depende del nivel de humedad disponible. Si la disponibilidad de agua es alta, el lote se clasifica como óptimo. Si la disponibilidad es media, se clasifica como viable con manejo técnico adicional. Si la disponibilidad es baja, el lote no puede considerarse apto, aun cuando los demás factores sean adecuados.

Existe una condición adicional relacionada con el contenido de materia orgánica del suelo. Si este valor es inferior a un porcentaje mínimo recomendado, la clasificación no puede ser óptima, aunque las demás condiciones sean favorables.

El algoritmo debe determinar si el lote es no apto, viable con manejo técnico adicional u óptimo para la siembra.

### Ejemplos de prueba

**Ejemplo 1**

pH del suelo: 6.5
Altitud: 1.800
Disponibilidad de agua: Alta
Materia orgánica: 4

Resultado esperado:
Óptimo para la siembra

**Ejemplo 2**

pH del suelo: 6.8
Altitud: 1.750
Disponibilidad de agua: Alta
Materia orgánica: 2

Resultado esperado:
Viable con manejo técnico adicional

**Ejemplo 3**

pH del suelo: 5.0
Altitud: 2.100
Disponibilidad de agua: Media
Materia orgánica: 5

Resultado esperado:
No apto for la siembra
