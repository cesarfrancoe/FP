ALGORITMO

VARIABLES
    ingresoMensual COMO REAL
    cuotaEstimada COMO REAL
    deudasActuales COMO REAL
    puntajeCrediticio COMO ENTERO
    indiceCarga COMO REAL
    estadoCarga COMO CADENA
    estadoHistorial COMO CADENA
    perfilFinanciero COMO CADENA

INICIO

    ESCRIBIR "Ingrese el ingreso mensual: "
    LEER ingresoMensual

    ESCRIBIR "Ingrese el valor de la cuota estimada: "
    LEER cuotaEstimada

    ESCRIBIR "Ingrese el total de deudas actuales: "
    LEER deudasActuales

    ESCRIBIR "Ingrese el puntaje crediticio: "
    LEER puntajeCrediticio

    indiceCarga ← (cuotaEstimada + deudasActuales) / ingresoMensual

    SI (indiceCarga ≤ 0.40) ENTONCES
        estadoCarga ← "Adecuada"
    SINO
        estadoCarga ← "Excesiva"
    FIN SI

    SI (puntajeCrediticio ≥ 800) ENTONCES
        estadoHistorial ← "Excelente"
    SINO SI (puntajeCrediticio ≥ 650 Y puntajeCrediticio ≤ 799) ENTONCES
        estadoHistorial ← "Aceptable"
    SINO
        estadoHistorial ← "Deficiente"
    FIN SI

    SI (estadoCarga = "Excesiva") ENTONCES
        ESCRIBIR "Sobreendeudamiento"
    FIN SI

    SI (estadoHistorial = "Deficiente") ENTONCES
        ESCRIBIR "Riesgo crediticio alto"
    FIN SI

    SI (estadoCarga = "Adecuada" Y (estadoHistorial = "Excelente" O estadoHistorial = "Aceptable")) ENTONCES
        perfilFinanciero ← "Estable"
    SINO
        perfilFinanciero ← "Con riesgo"
    FIN SI

    ESCRIBIR "Índice de carga financiera: ", indiceCarga
    ESCRIBIR "Carga financiera: ", estadoCarga
    ESCRIBIR "Historial crediticio: ", estadoHistorial
    ESCRIBIR "Perfil financiero: ", perfilFinanciero

FIN
