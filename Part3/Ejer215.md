## **Problema 215: Simulador de Lanzamiento de dados (LCR)**

### **Descripción**  
Este problema consiste en simular el lanzamiento de 3 dados de 6 caras para cuatro usuarios controlados por la computadora. La simulación debe repetirse por un número `N` de turnos, ingresado al inicio. El valor de `N` debe estar entre 1 y 10. En cada turno, se debe mostrar el resultado de cada lanzamiento de cada dado para cada usuario.

---

### **Análisis**  
Para implementar la simulación, se deben considerar los siguientes elementos y reglas:

1. **Usuarios Controlados por la Computadora**:
   - La simulación es para cuatro usuarios controlados por la computadora, identificados como "Computadora 1", "Computadora 2", "Computadora 3", y "Computadora 4".

2. **Dados y Caras**:
   - Cada usuario lanza tres dados de 6 caras en cada turno.
   - Las caras de los dados pueden tener los siguientes efectos, que serán mostrados en los resultados:

     | **Valor del Dado** | **Símbolo** | **Acción**                             |
     |--------------------|-------------|----------------------------------------|
     | 1                  | L (Left)    | Pasa una ficha al jugador a la izquierda |
     | 2                  | C (Center)  | Coloca una ficha en el centro            |
     | 3                  | R (Right)   | Pasa una ficha al jugador a la derecha   |
     | 4                  | * (Punto)   | Acción neutra                            |
     | 5                  | * (Punto)   | Acción neutra                            |
     | 6                  | * (Punto)   | Acción neutra                            |

3. **Turnos**:
   - El número de turnos (`N`) se solicita al inicio de la simulación.
   - El valor de `N` debe estar entre 1 y 10; si el usuario ingresa un valor fuera de este rango, se debe mostrar un mensaje de error y solicitar nuevamente el número de turnos hasta que sea válido.
   - Durante cada turno, cada usuario lanza sus tres dados, y el sistema muestra el resultado específico de cada dado.

**Ejemplo de desarrollo del juego**:  
1. La simulación solicita el número de turnos (`N`) para la simulación. Supongamos que `N = 3`.
2. En el primer turno:
   - Computadora 1 lanza tres dados y obtiene `L`, `C`, y `R`.
   - Computadora 2 lanza tres dados y obtiene `* (Punto)`, `R`, y `C`.
   - Computadora 3 lanza tres dados y obtiene `* (Punto)`, `L`, y `R`.
   - Computadora 4 lanza tres dados y obtiene `C`, `* (Punto)`, y `L`.
   - El sistema muestra los resultados de los lanzamientos de cada dado para cada usuario en el primer turno.
3. Este proceso se repite para los 3 turnos, mostrando únicamente los resultados de los dados en cada turno para cada usuario.

---

### **Requerimientos**  
- El algoritmo debe solicitar el número de turnos (`N`) al inicio de la simulación y validar que `N` esté entre 1 y 10. Si se ingresa cualquier valor fuera de este rango, se debe mostrar un mensaje de error y solicitar nuevamente la entrada hasta que sea correcta.
- Durante cada turno, cada usuario debe lanzar tres dados de 6 caras, y el sistema debe mostrar el resultado de cada dado para cada usuario.
- El algoritmo debe utilizar estructuras de control iterativas del tipo **"Hacer... Repetir"** para gestionar los turnos.
- No se deben usar instrucciones rompedoras (como `romper`, `continuar` u otra similar) para finalizar el ciclo.

---

### **Etapas de Desarrollo**

1. **Etapa 1: Solicitar la cantidad de turnos**
   - Solicitar al usuario el número de turnos `N` que se va a simular.
   - Validar que el valor ingresado esté entre 1 y 10; si no es así, mostrar un mensaje de error y solicitar nuevamente la entrada.

2. **Etapa 2: Simulación de N turnos**
   - Establecer una estructura iterativa para ejecutar la simulación durante los `N` turnos especificados.
   - Mostrar en pantalla el número del turno actual.

3. **Etapa 3: Simulación de 4 usuarios por turno**
   - Dentro de cada turno, simular el comportamiento de cuatro usuarios controlados por la computadora.
   - Mostrar en pantalla el número del usuario actual (por ejemplo, "Usuario 1", "Usuario 2", etc.).

4. **Etapa 4: Simulación de 3 lanzamientos por usuario**
   - Para cada usuario, realizar tres lanzamientos de un dado en cada turno.
   - Mostrar en pantalla el número del lanzamiento actual (por ejemplo, "Lanzamiento 1", "Lanzamiento 2", etc.).

5. **Etapa 5: Simulación del lanzamiento del dado de 6 caras**
   - Implementar la lógica que simula el lanzamiento de un dado de 6 caras, generando un valor aleatorio entre 1 y 6.

6. **Etapa 6: Mostrar el símbolo correspondiente al valor del dado**
   - Dependiendo del resultado del dado, mostrar el símbolo que corresponde a cada valor según la siguiente tabla:

     | **Valor del Dado** | **Símbolo** | **Acción**                             |
     |--------------------|-------------|----------------------------------------|
     | 1                  | L (Left)    | Pasa una ficha al jugador a la izquierda |
     | 2                  | C (Center)  | Coloca una ficha en el centro            |
     | 3                  | R (Right)   | Pasa una ficha al jugador a la derecha   |
     | 4                  | * (Punto)   | Acción neutra                            |
     | 5                  | * (Punto)   | Acción neutra                            |
     | 6                  | * (Punto)   | Acción neutra                            |

7. **Etapa 7: Revisión Final y Ajustes**
   - Verificar que todos los resultados se muestren de forma clara y precisa para cada turno, cada usuario, y cada lanzamiento.
   - Realizar ajustes finales en la presentación de los resultados y hacer pruebas adicionales para asegurar el correcto funcionamiento del programa.
