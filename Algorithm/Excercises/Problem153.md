## Problema 153 – Evaluación de estado fisiológico en medicina deportiva

Un centro de medicina deportiva evalúa el estado fisiológico de un atleta inmediatamente después de una sesión de entrenamiento intensivo. El propósito es determinar su nivel de recuperación a partir de tres indicadores cuantitativos medidos en el mismo momento: frecuencia cardiaca en reposo posterior al entrenamiento (en latidos por minuto), nivel de lactato en sangre (en mmol/L) y porcentaje de hidratación corporal estimado (en porcentaje).

Todos los valores registrados se consideran números reales no negativos.

Cada indicador se clasifica en uno de tres niveles mutuamente excluyentes y exhaustivos. A cada nivel se le asigna un puntaje. El puntaje total de recuperación corresponde a la suma de los puntos obtenidos en los tres indicadores.

**1. Frecuencia cardiaca (lpm)**

* Si 0 ≤ frecuencia ≤ 80, se considera dentro del rango recomendado y aporta 2 puntos.
* Si 80 < frecuencia ≤ 95, se considera ligeramente elevada y aporta 1 punto.
* Si frecuencia > 95, se considera en nivel crítico y aporta 0 puntos.

**2. Nivel de lactato (mmol/L)**

* Si 0 ≤ lactato ≤ 2, se considera óptimo y aporta 2 puntos.
* Si 2 < lactato ≤ 4, se considera intermedio y aporta 1 punto.
* Si lactato > 4, se considera en nivel crítico y aporta 0 puntos.

**3. Porcentaje de hidratación (%)**

* Si hidratación ≥ 55, se considera adecuada y aporta 2 puntos.
* Si 50 ≤ hidratación < 55, se considera leve déficit y aporta 1 punto.
* Si 0 ≤ hidratación < 50, se considera deshidratación marcada y aporta 0 puntos.

Los intervalos definidos no se superponen y cubren completamente todos los valores posibles dentro del dominio válido (valores reales no negativos).

El puntaje total posible está entre 0 y 6 inclusive.

El nivel global de recuperación se determina así:

* Si puntaje total = 6, la recuperación es óptima.
* Si 3 ≤ puntaje total ≤ 5, la recuperación es parcial.
* Si puntaje total < 3, la recuperación es insuficiente.

Adicionalmente, se debe emitir una advertencia médica si al menos uno de los tres indicadores se encuentra en nivel crítico. Un indicador está en nivel crítico si y solo si:

* frecuencia > 95, o
* lactato > 4, o
* hidratación < 50.

La advertencia médica es independiente del nivel global de recuperación y debe mostrarse incluso si el puntaje total corresponde a recuperación parcial o insuficiente.

El algoritmo debe:

* Evaluar cada indicador según los intervalos definidos.
* Calcular el puntaje individual de cada indicador.
* Calcular el puntaje total.
* Determinar el nivel de recuperación.
* Determinar si corresponde emitir advertencia médica.

---

**Ejemplos de prueba**

**Ejemplo 1**

Frecuencia cardiaca: 80 lpm

Lactato: 2 mmol/L

Hidratación: 55%

Puntajes: 2 + 2 + 2 = 6

**Resultado esperado:** 
Recuperación óptima. 

Sin advertencia médica.

**Ejemplo 2**

Frecuencia cardiaca: 95 lpm

Lactato: 3.5 mmol/L

Hidratación: 52%

Puntajes: 1 + 1 + 1 = 3

**Resultado esperado:** 
Recuperación parcial. 

Sin advertencia médica.

Ejemplo 3

Frecuencia cardiaca: 102 lpm

Lactato: 4.2 mmol/L

Hidratación: 49%

Puntajes: 0 + 0 + 0 = 0

**Resultado esperado:** 

Recuperación insuficiente. 

Con advertencia médica.
