### Problema 156 – Construcción de un Bowl personalizado

En un restaurante de comida saludable los clientes pueden construir un bowl personalizado seleccionando una base y un conjunto limitado de complementos. El sistema debe calcular el contenido calórico total del bowl y evaluar ciertas condiciones nutricionales a partir de las decisiones tomadas por el usuario.

El proceso inicia solicitando la base del bowl, la cual debe corresponder a una de las siguientes opciones: arroz, quinoa o lechuga. En caso de seleccionar arroz, el sistema debe solicitar el tipo de arroz, que puede ser blanco, verde o amarillo, aportando 200, 180 y 190 calorías respectivamente. Si la base es quinoa, se debe solicitar el tipo, que puede ser tradicional o roja, con un aporte de 180 y 190 calorías respectivamente. Si la base seleccionada es lechuga, esta aporta directamente 50 calorías y no requiere información adicional.

Posteriormente, el sistema debe consultar de forma secuencial si el usuario desea agregar cada uno de los siguientes complementos: pollo, tofu, aguacate, maíz y tomate. Para cada complemento, el usuario debe responder "si" o "no". Cada vez que el usuario responda afirmativamente, se considera que ha seleccionado un complemento. El número máximo de complementos permitidos es tres, por lo tanto, una vez se hayan seleccionado tres complementos, el sistema no debe continuar realizando preguntas sobre los restantes.

En el caso de seleccionar pollo, el sistema debe solicitar el tipo de preparación, que puede ser a la plancha o teriyaki, aportando 150 y 180 calorías respectivamente. Si se selecciona tofu, se debe solicitar su tipo, que puede ser natural o marinado, con un aporte de 120 y 140 calorías respectivamente. Los demás complementos no requieren información adicional y aportan las siguientes calorías: aguacate 100, maíz 80 y tomate 30. Si el usuario responde "no" a un complemento, este no se incluye en el cálculo.

Las calorías totales del bowl corresponden a la suma de las calorías de la base y de todos los complementos seleccionados. Con base en este valor, el bowl se clasifica como Bowl ligero si las calorías son menores o iguales a 300, Bowl balanceado si se encuentran entre 301 y 500 inclusive, o Bowl energético si superan las 500 calorías.

Adicionalmente, si el bowl incluye pollo o tofu, se considera que contiene proteína principal. En caso contrario, el sistema debe mostrar una advertencia indicando que el bowl no contiene proteína principal. De igual forma, si la base seleccionada es arroz blanco y las calorías totales superan las 550 unidades, el sistema debe mostrar una recomendación nutricional sugiriendo cambiar la base por quinoa o lechuga. Esta recomendación no afecta la clasificación del bowl.

Finalmente, si el usuario selecciona menos de tres complementos, el bowl se considera no válido y el sistema debe mostrar el siguiente mensaje: “Bowl no válido: debe seleccionar exactamente 3 complementos para construir el bowl”. En este caso, no se deben mostrar ni las calorías totales ni la clasificación nutricional ni mensajes adicionales.

El algoritmo debe mostrar los resultados correspondientes según la validez del bowl y las condiciones descritas.

---

### Ejemplos de prueba

**Ejemplo 1**

Base: arroz  
Tipo de arroz: verde  

Pollo: si (plancha)  
Tofu: no  
Aguacate: si  
Maíz: si  
→ Ya se han seleccionado 3 complementos, no se pregunta por tomate

Cálculo:
180 + 150 + 100 + 80 = 510

Resultado esperado:
Calorías totales: 510
Clasificación: Bowl energético
Proteína principal: Sí

---

**Ejemplo 2**

Base: quinoa
Tipo de quinoa: tradicional

Pollo: no
Tofu: no
Aguacate: si
Maíz: si
Tomate: si

Cálculo:
180 + 100 + 80 + 30 = 390

Resultado esperado:
Calorías totales: 390
Clasificación: Bowl balanceado
Proteína principal: No
Advertencia: el bowl no contiene proteína principal

---

**Ejemplo 3**

Base: lechuga

Pollo: no
Tofu: si (natural)
Aguacate: no
Maíz: no
Tomate: no

→ Solo se seleccionó 1 complemento

Resultado esperado:
Bowl no válido: debe seleccionar exactamente 3 complementos para construir el bowl
