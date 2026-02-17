## Problema 151 – Evaluación de capacidad financiera integral

Una entidad bancaria analiza la situación financiera de un solicitante antes de aprobar un crédito. En lugar de emitir únicamente una aprobación o rechazo, el sistema debe evaluar de manera independiente la capacidad de pago y el nivel de exposición financiera.

El análisis comienza calculando el índice de carga financiera, el cual corresponde a la proporción entre la suma de la cuota estimada del nuevo crédito y las deudas actuales respecto al ingreso mensual. Este índice permite determinar si la persona mantiene una carga financiera adecuada o excesiva.

De manera paralela, se evalúa el historial crediticio del solicitante, el cual se clasifica en excelente, aceptable o deficiente según el puntaje registrado.

Si el índice de carga financiera supera el límite permitido, el sistema debe indicar que existe sobreendeudamiento, independientemente del historial crediticio. Si el historial es deficiente, el sistema debe indicar riesgo crediticio alto, incluso cuando el índice de carga financiera sea adecuado.

Solo cuando ambos indicadores se encuentran dentro de los límites aceptables, el sistema puede indicar que el perfil financiero es estable.

El algoritmo debe:

* Calcular el índice de carga financiera.
* Clasificar dicho índice como adecuado o excesivo.
* Clasificar el historial crediticio.
* Emitir los mensajes correspondientes a cada indicador.
* Indicar finalmente si el perfil es estable o presenta riesgo.


### Ejemplos de prueba

---

**Ejemplo 1**

Ingreso mensual: 5.000.000

Cuota estimada: 800.000

Deudas actuales: 700.000

Puntaje crediticio: 820

**Resultado esperado:**

Carga financiera adecuada

Historial excelente

Perfil financiero estable

---

**Ejemplo 2**

Ingreso mensual: 4.000.000

Cuota estimada: 1.200.000

Deudas actuales: 900.000

Puntaje crediticio: 780

**Resultado esperado:**

Carga financiera excesiva

Historial aceptable

Perfil con riesgo

---

**Ejemplo 3**

Ingreso mensual: 4.000.000

Cuota estimada: 700.000

Deudas actuales: 600.000

Puntaje crediticio: 600

**Resultado esperado:**

Carga financiera adecuada

Historial deficiente

Perfil con riesgo
