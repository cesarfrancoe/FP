## **Problema 213: Simulador de Temporizador (Cuenta Progresiva)**

### **Descripción**  
Este problema consiste en simular un temporizador que comienza en `0 horas, 0 minutos y 0 segundos` y avanza segundo a segundo hasta alcanzar una cantidad específica de horas, minutos y segundos ingresada por el usuario. Durante el proceso, el sistema muestra en pantalla el tiempo transcurrido en cada segundo.

---

### **Análisis**  
Para implementar el simulador de temporizador en cuenta progresiva, se deben considerar los siguientes elementos y reglas:

1. **Ingreso de Datos**:
   - El usuario ingresa la cantidad final de horas, minutos y segundos a la que desea que el temporizador llegue.
   - Los valores ingresados deben estar dentro de los rangos aceptables:
     - Horas: entre 0 y 23.
     - Minutos: entre 0 y 59.
     - Segundos: entre 0 y 59.
   - Si alguno de los valores está fuera de su rango, se debe mostrar un mensaje de error y solicitar nuevamente el valor.

2. **Cuenta Progresiva**:
   - Una vez ingresados los valores finales, el temporizador comienza en `0h 0m 0s` y cuenta hacia adelante, segundo a segundo, hasta alcanzar los valores de horas, minutos y segundos ingresados por el usuario.
   - Cada vez que los segundos alcanzan 60, se restablecen a 0 y se incrementa un minuto.
   - Cada vez que los minutos alcanzan 60, se restablecen a 0 y se incrementa una hora.
   - La cuenta progresiva se detiene automáticamente cuando se alcanzan los valores finales de horas, minutos y segundos.

3. **Visualización**:
   - En cada segundo de la cuenta progresiva, el sistema muestra el tiempo transcurrido en el formato `HH:MM:SS`.
   - Al alcanzar el tiempo final especificado por el usuario, el sistema muestra el mensaje **"Tiempo alcanzado"** y detiene la simulación.

---

### **Ejemplo de Desarrollo del Temporizador**:

1. El sistema solicita al usuario ingresar las horas, minutos y segundos que desea alcanzar.
   - Ejemplo: el usuario ingresa 0 horas, 1 minuto y 5 segundos.

2. El temporizador inicia la cuenta progresiva desde `00:00:00`, mostrando cada segundo en pantalla:
   ```
   00:00:00
   00:00:01
   00:00:02
   ...
   00:01:05
   Tiempo alcanzado
   ```

---

### **Requerimientos**  

1. El algoritmo debe solicitar al usuario ingresar una cantidad final de horas, minutos y segundos.
2. Debe validar que las horas estén entre 0 y 23, y que tanto los minutos como los segundos estén entre 0 y 59. Si el usuario ingresa un valor fuera de estos rangos, el sistema debe mostrar un mensaje de error y solicitar el valor nuevamente hasta que sea correcto.
3. La cuenta progresiva debe iniciar en `0h 0m 0s` y aumentar en intervalos de un segundo, ajustando minutos y horas según corresponda, hasta alcanzar el tiempo especificado por el usuario.
4. En cada segundo, el sistema debe mostrar en pantalla el tiempo transcurrido en el formato `HH:MM:SS`.
5. El temporizador debe detenerse automáticamente cuando el tiempo transcurrido alcance los valores finales de horas, minutos y segundos.
6. El temporizador debe utilizar una estructura de control iterativa del tipo **"Hacer... Repetir"** para avanzar el tiempo, y debe detenerse al llegar al valor final especificado.
7. No se deben usar instrucciones rompedoras (como `romper`, `continuar` u otra similar) para finalizar el ciclo.
