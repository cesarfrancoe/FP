```
ALGORITMO
VARIABLES
    documento COMO Entero
    edad COMO Entero
    tieneBoleta COMO Entero
    esEstudiante COMO Entero

    residuoGrupo COMO Entero
    residuoTurno COMO Entero

    grupoIngreso COMO Cadena
    turnoIngreso COMO Cadena
    categoriaEdad COMO Cadena
    tipoPersona COMO Cadena
    puedeIngresar COMO Cadena

    precioEntrada COMO Entero

INICIO
1   ESCRIBIR "Ingrese el número de documento:"
2   LEER documento

3   ESCRIBIR "Ingrese la edad:"
4   LEER edad

5   ESCRIBIR "¿Tiene boleta? (1 = Sí, 0 = No):"
6   LEER tieneBoleta

7   ESCRIBIR "¿Es estudiante? (1 = Sí, 0 = No):"
8   LEER esEstudiante

9   residuoGrupo ← documento mod 3
10  residuoTurno ← documento mod 2

11  grupoIngreso ← "Sin asignar"
12  turnoIngreso ← "Sin asignar"
13  categoriaEdad ← "Sin clasificar"
14  tipoPersona ← "Sin clasificar"
15  puedeIngresar ← "No autorizado"
16  precioEntrada ← 0

17  SI (residuoGrupo = 0) ENTONCES
18      grupoIngreso ← "Grupo A"
19  FIN SI

20  SI (residuoGrupo = 1) ENTONCES
21      grupoIngreso ← "Grupo B"
22  FIN SI

23  SI (residuoGrupo = 2) ENTONCES
24      grupoIngreso ← "Grupo C"
25  FIN SI

26  SI (residuoTurno = 0) ENTONCES
27      turnoIngreso ← "Turno Mañana"
28  SINO
29      turnoIngreso ← "Turno Tarde"
30  FIN SI

31  SI (edad < 13) ENTONCES
32      categoriaEdad ← "Niño"
33  SINO SI (edad < 18) ENTONCES
34      categoriaEdad ← "Adolescente"
35  SINO SI (edad < 60) ENTONCES
36      categoriaEdad ← "Adulto"
37  SINO
38      categoriaEdad ← "Adulto mayor"
39  FIN SI

40  SI (esEstudiante = 1) ENTONCES
41      tipoPersona ← "Estudiante"
42  FIN SI

43  SI (edad ≥ 18) ENTONCES
44      SI (tieneBoleta = 1) ENTONCES
45          puedeIngresar ← "Autorizado"
46      SINO
47          puedeIngresar ← "No autorizado"
48      FIN SI
49  SINO
50      puedeIngresar ← "No autorizado"
51  FIN SI

52  SI (categoriaEdad = "Niño") ENTONCES
53      precioEntrada ← 3000
54  SINO SI (categoriaEdad = "Adolescente") ENTONCES
55      precioEntrada ← 5000
56  SINO SI (categoriaEdad = "Adulto") ENTONCES
57      precioEntrada ← 10000
58  SINO
59      precioEntrada ← 4000
60  FIN SI

61  SI (tipoPersona = "Estudiante") ENTONCES
62      precioEntrada ← precioEntrada - 2000
63  FIN SI

64  ESCRIBIR "Grupo de ingreso:"
65  ESCRIBIR grupoIngreso

66  ESCRIBIR "Turno asignado:"
67  ESCRIBIR turnoIngreso

68  ESCRIBIR "Categoría de edad:"
69  ESCRIBIR categoriaEdad

70  ESCRIBIR "Tipo de persona:"
71  ESCRIBIR tipoPersona

72  ESCRIBIR "Estado de ingreso:"
73  ESCRIBIR puedeIngresar

74  ESCRIBIR "Precio de entrada:"
75  ESCRIBIR precioEntrada
FIN
```
