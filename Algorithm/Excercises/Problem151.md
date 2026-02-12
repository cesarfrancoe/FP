### Problema 151 – Clasificación de riesgo crediticio personal

Una entidad bancaria analiza solicitudes de crédito personal evaluando múltiples factores relacionados con la capacidad de pago y el comportamiento financiero del solicitante. La decisión no se basa únicamente en el ingreso mensual, sino también en el nivel de endeudamiento actual, el historial de pagos y la estabilidad laboral.

Para que una solicitud pueda considerarse viable, el ingreso mensual debe ser suficiente en relación con el valor de la cuota estimada del crédito. Además, el nivel total de deudas no debe superar un porcentaje determinado del ingreso mensual. Si cualquiera de estas condiciones básicas no se cumple, la solicitud debe ser rechazada.

Cuando se cumplen las condiciones mínimas, la clasificación del riesgo depende del puntaje de historial crediticio. Si el puntaje es igual o superior a 800, el riesgo se considera bajo. Si el puntaje está entre 650 y 799 inclusive, el riesgo se considera medio. Si el puntaje es inferior a 650, el riesgo se considera alto y la solicitud debe ser rechazada.

Existe una condición adicional relacionada con la estabilidad laboral. Si el solicitante ha permanecido menos de un año en su empleo actual, la clasificación no puede ser de riesgo bajo, incluso si el puntaje crediticio es alto; en ese caso, la clasificación final debe ajustarse a riesgo medio.

El algoritmo debe determinar si la solicitud es rechazada o aprobada y, en caso de aprobación, indicar si el riesgo es bajo o medio.

### Ejemplos de prueba

**Ejemplo 1**

Ingreso mensual: 4.000.000
Cuota estimada: 800.000
Total de deudas: 1.000.000
Puntaje crediticio: 820
Años en empleo actual: 3

Resultado esperado:
Aprobada – Riesgo bajo

**Ejemplo 2**

Ingreso mensual: 4.000.000
Cuota estimada: 800.000
Total de deudas: 1.000.000
Puntaje crediticio: 820
Años en empleo actual: 0

Resultado esperado:
Aprobada – Riesgo medio

**Ejemplo 3**

Ingreso mensual: 3.000.000
Cuota estimada: 1.200.000
Total de deudas: 2.000.000
Puntaje crediticio: 700
Años en empleo actual: 5

Resultado esperado:
Rechazada
