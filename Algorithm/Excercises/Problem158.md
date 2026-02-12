### Problema 158 – Evaluación técnica de diseño estructural en ingeniería civil

Una firma de ingeniería civil analiza la viabilidad preliminar de un diseño estructural propuesto para una edificación. La evaluación no depende únicamente del material seleccionado, sino también de la carga estimada, el factor de seguridad calculado y el tipo de zona sísmica en la que se construirá la estructura.

El proceso inicia identificando el material estructural principal, que puede ser “Concreto”, “Acero” o “Madera”. Dependiendo del material, ciertos parámetros adquieren mayor relevancia. Por ejemplo, para estructuras en concreto y acero es obligatorio verificar que el factor de seguridad sea superior al mínimo normativo establecido. En el caso de la madera, además del factor de seguridad, debe verificarse que la carga estimada no supere un límite recomendado para ese tipo de material.

Independientemente del material, si la carga estimada supera la capacidad máxima permitida por el diseño preliminar, la propuesta debe clasificarse como no viable.

Cuando la carga y el factor de seguridad cumplen los mínimos requeridos, la clasificación final depende de la zona sísmica. En zonas de alta sismicidad, el diseño solo puede considerarse completamente aprobado si el factor de seguridad supera un valor adicional de refuerzo. Si no alcanza ese valor, aunque cumpla el mínimo normativo, el diseño se clasifica como viable con ajustes.

Además, si el material seleccionado es madera y la zona sísmica es alta, el sistema debe emitir una advertencia adicional indicando que se recomienda una revisión estructural especializada.

El algoritmo debe:

* Determinar si el diseño es no viable, viable con ajustes o aprobado.
* Emitir advertencia adicional cuando corresponda.

### Ejemplos de prueba

**Ejemplo 1**

Material: Concreto
Carga estimada: 800
Capacidad máxima permitida: 1000
Factor de seguridad: 2.5
Factor mínimo normativo: 2.0
Zona sísmica: Media

Resultado esperado:
Aprobado

**Ejemplo 2**

Material: Acero
Carga estimada: 900
Capacidad máxima permitida: 1000
Factor de seguridad: 2.1
Factor mínimo normativo: 2.0
Zona sísmica: Alta
Factor adicional requerido: 2.5

Resultado esperado:
Viable con ajustes

**Ejemplo 3**

Material: Madera
Carga estimada: 1100
Capacidad máxima permitida: 1000
Factor de seguridad: 1.8
Factor mínimo normativo: 2.0
Zona sísmica: Alta

Resultado esperado:
No viable
Advertencia: revisión estructural especializada recomendada
