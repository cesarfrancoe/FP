### Problema 152 – Determinación de categoría tributaria empresarial

Una entidad de control fiscal debe clasificar a las empresas en una categoría tributaria anual teniendo en cuenta varios factores económicos y administrativos. La clasificación no depende únicamente del nivel de ingresos, sino también del número de empleados, del sector económico al que pertenece la empresa y de su cumplimiento en obligaciones anteriores.

Para que una empresa pueda permanecer en el régimen simplificado, sus ingresos anuales no deben superar un umbral establecido y el número de empleados no debe exceder el límite permitido por la normativa vigente. Si cualquiera de estas dos condiciones se incumple, la empresa debe pasar automáticamente al régimen ordinario.

Cuando la empresa cumple las condiciones básicas del régimen simplificado, la clasificación final depende del sector económico. Las empresas del sector industrial deben realizar una contribución adicional si sus ingresos superan cierto valor intermedio, mientras que las del sector comercial solo están obligadas a dicha contribución si además superan un número específico de empleados.

Existe una condición adicional relacionada con el historial de cumplimiento. Si la empresa registra sanciones tributarias en el último año, no puede permanecer en el régimen simplificado, independientemente de sus ingresos o número de empleados.

El algoritmo debe determinar si la empresa pertenece al régimen simplificado o al régimen ordinario y, en caso de permanecer en el régimen simplificado, indicar si debe realizar contribución adicional.

### Ejemplos de prueba

**Ejemplo 1**

Ingresos anuales: 400.000.000
Número de empleados: 8
Sector económico: Industrial
Sanciones registradas: 0

Resultado esperado:
Régimen simplificado – Sin contribución adicional

**Ejemplo 2**

Ingresos anuales: 600.000.000
Número de empleados: 12
Sector económico: Comercial
Sanciones registradas: 0

Resultado esperado:
Régimen ordinario

**Ejemplo 3**

Ingresos anuales: 450.000.000
Número de empleados: 6
Sector económico: Industrial
Sanciones registradas: 1

Resultado esperado:
Régimen ordinario
