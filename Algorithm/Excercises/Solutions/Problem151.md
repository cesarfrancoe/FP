```text
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

1     ESCRIBIR "Ingrese el ingreso mensual: "
2     LEER ingresoMensual

3     ESCRIBIR "Ingrese el valor de la cuota estimada: "
4     LEER cuotaEstimada

5     ESCRIBIR "Ingrese el total de deudas actuales: "
6     LEER deudasActuales

7     ESCRIBIR "Ingrese el puntaje crediticio: "
8     LEER puntajeCrediticio

9     indiceCarga ← (cuotaEstimada + deudasActuales) / ingresoMensual

10    SI (indiceCarga ≤ 0.40) ENTONCES
11        estadoCarga ← "Adecuada"
12    SINO
13        estadoCarga ← "Excesiva"
14    FIN SI

15    SI (puntajeCrediticio ≥ 800) ENTONCES
16        estadoHistorial ← "Excelente"
17    SINO SI (puntajeCrediticio ≥ 650 Y puntajeCrediticio ≤ 799) ENTONCES
18        estadoHistorial ← "Aceptable"
19    SINO
20        estadoHistorial ← "Deficiente"
21    FIN SI

22    SI (estadoCarga = "Excesiva") ENTONCES
23        ESCRIBIR "Sobreendeudamiento"
24    FIN SI

25    SI (estadoHistorial = "Deficiente") ENTONCES
26        ESCRIBIR "Riesgo crediticio alto"
27    FIN SI

28    SI (estadoCarga = "Adecuada" Y (estadoHistorial = "Excelente" O estadoHistorial = "Aceptable")) ENTONCES
29        perfilFinanciero ← "Estable"
30    SINO
31        perfilFinanciero ← "Con riesgo"
32    FIN SI

33    ESCRIBIR "Índice de carga financiera: ", indiceCarga
34    ESCRIBIR "Carga financiera: ", estadoCarga
35    ESCRIBIR "Historial crediticio: ", estadoHistorial
36    ESCRIBIR "Perfil financiero: ", perfilFinanciero

FIN
```
