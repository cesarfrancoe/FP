### Problema 155 – Evaluación de observación astronómica

Un observatorio astronómico analiza los datos registrados durante una sesión de observación nocturna para determinar la calidad de los registros obtenidos y la viabilidad de continuar con el estudio del objeto celeste.

El sistema recibe como datos de entrada suministrados por el usuario:

* Tipo de objeto observado: “Planeta”, “Estrella” o “Galaxia”.
* Magnitud aparente (valor real).
* Interferencia lumínica: “Baja”, “Media” o “Alta”.
* Estabilidad atmosférica: “Alta”, “Media” o “Baja” (solo si el objeto es Planeta).
* Variabilidad luminosa: “Baja”, “Media” o “Alta” (solo si el objeto es Estrella).
* Tiempo efectivo de exposición en segundos (valor real).

Todos los valores son ingresados directamente por el usuario.

### Sistema de puntaje

Magnitud aparente:

* 0 ≤ magnitud ≤ 6 → 2 puntos.
* 6 < magnitud ≤ 8 → 1 punto.
* magnitud > 8 → 0 puntos.

Interferencia lumínica:

* Baja → 2 puntos.
* Media → 1 punto.
* Alta → 0 puntos.

Parámetro específico según el tipo de objeto:

Planeta (se evalúa estabilidad atmosférica):

* Alta → 2 puntos.
* Media → 1 punto.
* Baja → 0 puntos.

Estrella (se evalúa variabilidad luminosa):

* Baja → 2 puntos.
* Media → 1 punto.
* Alta → 0 puntos.

Galaxia (se evalúa tiempo de exposición como parámetro principal):

* Tiempo ≥ 120 segundos → 2 puntos.
* 80 ≤ tiempo < 120 → 1 punto.
* Tiempo < 80 → 0 puntos.

---

### Clasificación final

El puntaje total es la suma de:

* Puntaje por magnitud.
* Puntaje por interferencia.
* Puntaje del parámetro específico según el tipo.

Puntaje máximo posible: 6.

* 5 o 6 → “Observación de alta calidad”.
* 3 o 4 → “Observación de calidad media”.
* 0, 1 o 2 → “Observación inválida”.

### Advertencia adicional por tiempo insuficiente

Independientemente de la clasificación anterior, el sistema debe emitir una advertencia si el tiempo de exposición es inferior al mínimo recomendado para el tipo:

* Planeta: tiempo < 90 segundos.
* Estrella: tiempo < 100 segundos.
* Galaxia: tiempo < 80 segundos.

La advertencia no modifica la clasificación.

### Ejemplos de prueba

**Ejemplo 1**

Tipo de objeto: Estrella

Magnitud aparente: 3.5

Variabilidad luminosa: Baja

Interferencia lumínica: Baja

Tiempo de exposición: 120

Cálculo:

* Magnitud 3.5 → 2 puntos
* Interferencia baja → 2 puntos
* Variabilidad baja → 2 puntos
  Puntaje total = 6

**Resultado esperado:**

Observación de alta calidad

**Ejemplo 2**

Tipo de objeto: Galaxia

Magnitud aparente: 7.0

Interferencia lumínica: Media

Tiempo de exposición: 85

Cálculo:

* Magnitud 7.0 → 1 punto
* Interferencia media → 1 punto
* Tiempo 70 → 0 puntos
  Puntaje total = 2

**Resultado esperado:**

Observación inválida

Advertencia: tiempo de exposición insuficiente

**Ejemplo 3**

Tipo de objeto: Planeta

Magnitud aparente: 8.5

Estabilidad atmosférica: Baja

Interferencia lumínica: Alta

Tiempo de exposición: 100

Cálculo:

* Magnitud 8.5 → 0 puntos
* Interferencia alta → 0 puntos
* Estabilidad baja → 0 puntos
  Puntaje total = 0

**Resultado esperado:**

Observación inválida
