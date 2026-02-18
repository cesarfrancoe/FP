## Problema 151 – Evaluación de capacidad financiera integral

Una entidad bancaria analiza la situación financiera de un solicitante antes de aprobar un crédito. En lugar de emitir únicamente una aprobación o rechazo, el sistema debe evaluar de manera independiente la capacidad de pago y el nivel de exposición financiera.

El análisis comienza calculando el índice de carga financiera, el cual corresponde a la proporción entre la suma de la cuota estimada del nuevo crédito y las deudas actuales respecto al ingreso mensual. Este índice se calcula como:

(cuota estimada + deudas actuales) / ingreso mensual

El índice de carga financiera se considera adecuado cuando no supera el 40% del ingreso mensual. Si el índice es superior al 40%, se clasifica como excesivo.

De manera paralela, se evalúa el historial crediticio del solicitante. El historial se clasifica según el puntaje registrado de la siguiente forma:

- Puntaje igual o superior a 800: Historial excelente.

- Puntaje entre 650 y 799 inclusive: Historial aceptable.

- Puntaje inferior a 650: Historial deficiente.

Si el índice de carga financiera es excesivo, el sistema debe emitir el mensaje "sobreendeudamiento". Si el historial es deficiente, el sistema debe emitir el mensaje "riesgo crediticio alto". Ambos mensajes pueden emitirse de manera simultánea si se cumplen las dos condiciones.
El perfil financiero se considera estable únicamente cuando el índice de carga financiera es adecuado y el historial crediticio es excelente o aceptable. En cualquier otro caso, el perfil debe clasificarse como perfil con riesgo.

El algoritmo debe:

- Calcular el índice de carga financiera.

- Clasificar dicho índice como adecuado o excesivo.

- Clasificar el historial crediticio.

- Emitir los mensajes correspondientes a cada indicador.

- Determinar si el perfil financiero es estable o presenta riesgo.


### Ejemplos de prueba

---

**Ejemplo 1**

Ingreso mensual: 5.000.000

Cuota estimada: 800.000

Deudas actuales: 700.000

Puntaje crediticio: 820

**Resultado esperado:**

Carga financiera: adecuada

Historial: excelente

Perfil financiero: estable

---

**Ejemplo 2**

Ingreso mensual: 4.000.000

Cuota estimada: 1.200.000

Deudas actuales: 900.000

Puntaje crediticio: 780

**Resultado esperado:**

Carga financiera: excesiva

Historial: aceptable

Sobreendeudamiento

Perfil financiero: con riesgo

---

**Ejemplo 3**

Ingreso mensual: 4.000.000

Cuota estimada: 700.000

Deudas actuales: 600.000

Puntaje crediticio: 600

**Resultado esperado:**

Carga financiera: adecuada

Historial: deficiente

Riego crediticio: alto

Perfil financiero: con riesgo
