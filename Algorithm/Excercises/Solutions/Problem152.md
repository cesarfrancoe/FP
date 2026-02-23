ALGORITMO

VARIABLES
    tipoSistema COMO CADENA
    energiaUtil COMO REAL
    energiaConsumida COMO REAL
    consumoCriticoReferencia COMO REAL
    indiceEficiencia COMO REAL
    minimoAceptable COMO REAL
    margenMejora COMO REAL
    clasificacion COMO CADENA
    estadoConsumo COMO CADENA

INICIO

    ESCRIBIR "Ingrese el tipo de sistema (Eléctrico, Térmico o Híbrido): "
    LEER tipoSistema

    ESCRIBIR "Ingrese la energía útil generada: "
    LEER energiaUtil

    ESCRIBIR "Ingrese la energía total consumida: "
    LEER energiaConsumida

    ESCRIBIR "Ingrese el consumo crítico de referencia: "
    LEER consumoCriticoReferencia

    indiceEficiencia ← (energiaUtil / energiaConsumida) × 100
    margenMejora ← 100 − indiceEficiencia

    SI (tipoSistema = "Eléctrico") ENTONCES
        minimoAceptable ← 85
    SINO SI (tipoSistema = "Térmico") ENTONCES
        minimoAceptable ← 75
    SINO SI (tipoSistema = "Híbrido") ENTONCES
        minimoAceptable ← 80
    FIN SI

    SI (indiceEficiencia < minimoAceptable) ENTONCES
        clasificacion ← "Ineficiente"
    SINO SI (margenMejora < 5) ENTONCES
        clasificacion ← "Optimizado"
    SINO
        clasificacion ← "Eficiente estándar"
    FIN SI

    SI (tipoSistema = "Híbrido" Y energiaConsumida > consumoCriticoReferencia Y clasificacion = "Optimizado") ENTONCES
        clasificacion ← "Eficiente estándar"
    FIN SI

    SI (energiaConsumida > consumoCriticoReferencia) ENTONCES
        estadoConsumo ← "Consumo en nivel crítico"
    SINO
        estadoConsumo ← "Consumo dentro de rango normal"
    FIN SI

    ESCRIBIR "Índice de eficiencia: ", indiceEficiencia
    ESCRIBIR "Margen de mejora: ", margenMejora
    ESCRIBIR "Clasificación: ", clasificacion
    ESCRIBIR estadoConsumo

FIN
