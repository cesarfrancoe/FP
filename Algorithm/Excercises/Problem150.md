## Problema 150 – Evaluación de contrato de proveedor

Una institución pública analiza la aprobación de contratos con proveedores teniendo en cuenta varios criterios administrativos y financieros. La aprobación no depende únicamente del valor ofertado, sino también del cumplimiento de requisitos legales y del comportamiento histórico del proveedor.

Para que un contrato pueda considerarse viable, el proveedor debe tener una antigüedad mínima de un año y no debe presentar incumplimientos activos. Además, el valor ofertado debe encontrarse dentro del presupuesto máximo asignado al proyecto. Si el valor supera el presupuesto, el contrato no puede ser aprobado.

Cuando se cumplen las condiciones anteriores, el nivel de aprobación depende del porcentaje de cumplimiento en evaluaciones previas. Si dicho porcentaje es igual o superior al 90%, el contrato se clasifica como aprobación directa. Si el porcentaje está entre 75% y 89% inclusive, se clasifica como aprobación condicionada. Si el porcentaje es inferior a 75%, el contrato debe ser rechazado.

Existe una condición adicional: si el proveedor tiene menos de tres años de antigüedad, incluso cumpliendo los demás requisitos, la aprobación solo puede ser condicionada.

El algoritmo debe determinar si el contrato es rechazado, aprobado directamente o aprobado de manera condicionada.

### Ejemplos de prueba

---

**Ejemplo 1**

Años de antigüedad: 5

Incumplimientos activos: 0

Valor ofertado: 80.000.000

Presupuesto máximo: 95.000.000

Porcentaje de cumplimiento previo: 92

**Resultado esperado:**

Aprobación directa

---

**Ejemplo 2**

Años de antigüedad: 2

Incumplimientos activos: 0

Valor ofertado: 70.000.000

Presupuesto máximo: 85.000.000

Porcentaje de cumplimiento previo: 95

**Resultado esperado:**

Aprobación condicionada

---

**Ejemplo 3**

Años de antigüedad: 6

Incumplimientos activos: 1

Valor ofertado: 60.000.000

Presupuesto máximo: 75.000.000

Porcentaje de cumplimiento previo: 88

**Resultado esperado:**

Rechazado


