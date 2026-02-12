### Problema 156 – Evaluación clínica preventiva en medicina general

En una consulta de medicina preventiva se desea evaluar el estado general de un paciente considerando su presión arterial sistólica, su índice de masa corporal (IMC) y su nivel de glucosa en ayunas. La evaluación no tiene como objetivo emitir un único diagnóstico, sino determinar diferentes indicadores de riesgo que pueden presentarse simultáneamente.

La presión arterial se considera elevada si supera el valor recomendado para adultos. El índice de masa corporal permite clasificar al paciente en bajo peso, rango normal o sobrepeso según los límites establecidos. Por su parte, el nivel de glucosa en ayunas puede encontrarse dentro del rango normal, en nivel de alerta o en nivel alto.

Un paciente puede presentar simultáneamente presión elevada y sobrepeso, o glucosa alta con IMC normal, entre otras combinaciones. Por tanto, el algoritmo no debe producir una única clasificación global, sino evaluar cada indicador de manera independiente y emitir un mensaje para cada uno de ellos.

Además, si dos o más indicadores se encuentran fuera del rango normal, el sistema debe emitir una advertencia adicional indicando riesgo metabólico elevado.

El algoritmo debe analizar los valores ingresados y mostrar todos los mensajes correspondientes según las condiciones detectadas.

---

### Ejemplos de prueba

**Ejemplo 1**

Presión sistólica: 150
IMC: 29
Glucosa en ayunas: 110

Resultado esperado:
Presión elevada
Sobrepeso
Nivel de glucosa en alerta
Advertencia: riesgo metabólico elevado

---

**Ejemplo 2**

Presión sistólica: 120
IMC: 22
Glucosa en ayunas: 90

Resultado esperado:
Presión normal
IMC en rango normal
Glucosa normal

---

**Ejemplo 3**

Presión sistólica: 135
IMC: 31
Glucosa en ayunas: 140

Resultado esperado:
Presión elevada
Sobrepeso
Glucosa alta
Advertencia: riesgo metabólico elevado
