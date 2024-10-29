## **Problema 213: Simulador de Lanzamiento**

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
      - **1: L (Left)** - Pasa una ficha al jugador a la izquierda.
      - **2: C (Center)** - Coloca una ficha en el centro.
      - **3: R (Right)** - Pasa una ficha al jugador a la derecha.
      - **4: 1 (Punto)** - Acción neutra.
      - **5: 2 (Punto)** - Acción neutra.
      - **6: 3 (Punto)** - Acción neutra.

3. **Turnos**:
   - El número de turnos (`N`) se solicita al inicio de la simulación.
   - El valor de `N` debe estar entre 1 y 10; si el usuario ingresa un valor fuera de este rango, se debe mostrar un mensaje de error y solicitar nuevamente el número de turnos hasta que sea válido.
   - Durante cada turno, cada usuario lanza sus tres dados, y el sistema muestra el resultado específico de cada dado.

**Ejemplo de desarrollo del juego**:  
1. La simulación solicita el número de turnos (`N`) para la simulación. Supongamos que `N = 3`.
2. En el primer turno:
   - Computadora 1 lanza tres dados y obtiene `L`, `C`, y `R`.
   - Computadora 2 lanza tres dados y obtiene `1 (Punto)`, `R`, y `C`.
   - Computadora 3 lanza tres dados y obtiene `2 (Punto)`, `L`, y `R`.
   - Computadora 4 lanza tres dados y obtiene `C`, `1 (Punto)`, y `L`.
   - El sistema muestra los resultados de los lanzamientos de cada dado para cada usuario en el primer turno.
3. Este proceso se repite para los 3 turnos, mostrando únicamente los resultados de los dados en cada turno para cada usuario.

---

### **Requerimientos**  
- El algoritmo debe solicitar el número de turnos (`N`) al inicio de la simulación y validar que `N` esté entre 1 y 10. Si se ingresa un valor fuera de este rango, se debe mostrar un mensaje de error y solicitar nuevamente el número de turnos.
- Durante cada turno, cada usuario debe lanzar tres dados de 6 caras, y el sistema debe mostrar el resultado de cada dado para cada usuario.
- El algoritmo debe utilizar estructuras de control iterativas del tipo **"Hacer... Repetir"** para gestionar los turnos.
- No se deben usar instrucciones rompedoras (como `romper`, `continuar` u otra similar) para finalizar el ciclo.

---

### **Etapas de Desarrollo**

Para facilitar la implementación y prueba del proyecto, se recomienda avanzar en las siguientes etapas:

1. **Etapa 1: Solicitar el Número de Turnos y Validación de `N`**
   - Implementar la solicitud de `N`, el número de turnos, validando que esté en el rango de 1 a 10.
   - Probar la validación mostrando un mensaje de confirmación si `N` está en el rango correcto o un mensaje de error si no lo está.

2. **Etapa 2: Simular el Lanzamiento de un Dado para un Usuario**
   - Crear una función o procedimiento que simule el lanzamiento de un dado de 6 caras y muestre el resultado.
   - Probar la función lanzando el dado varias veces y verificando que los resultados estén dentro del rango de 1 a 6 y que se muestren correctamente.

3. **Etapa 3: Simular el Lanzamiento de Tres Dados para un Usuario**
   - Ampliar la función de la Etapa 2 para lanzar tres dados y mostrar el resultado de cada uno en un turno.
   - Probar el lanzamiento de tres dados varias veces para asegurarse de que cada resultado se muestra correctamente.

4. **Etapa 4: Agregar los Cuatro Usuarios Controlados por la Computadora**
   - Crear una estructura que represente a los cuatro usuarios y adapte el código para que cada usuario lance sus tres dados en cada turno.
   - Probar el algoritmo simulando un solo turno para los cuatro usuarios, mostrando el resultado de cada dado para cada usuario.

5. **Etapa 5: Implementar el Ciclo de Turnos**
   - Utilizar una estructura de control **"Hacer... Repetir"** para ejecutar los lanzamientos de dados en múltiples turnos según el valor de `N`.
   - Probar la simulación con diferentes valores de `N` dentro del rango permitido (1 a 10), asegurándose de que todos los turnos se ejecuten y muestren los resultados.

6. **Etapa 6: Revisión Final y Ajustes**
   - Revisar que el algoritmo muestre correctamente los resultados de cada dado en cada turno y de cada usuario.
   - Realizar ajustes finales en la presentación de los resultados para mejorar la claridad y la legibilidad.
   - Hacer pruebas adicionales con diferentes valores de `N` para asegurar la robustez y el correcto funcionamiento del programa.
