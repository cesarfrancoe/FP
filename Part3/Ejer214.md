## **Problema 214: Simulador de Temporizador (Cuenta Regresiva)**

### **Descripción**  
Este problema consiste en simular un temporizador que comienza en una cantidad específica de horas, minutos y segundos ingresada por el usuario y cuenta hacia atrás, segundo a segundo, hasta llegar a cero.

---

### **Análisis**  
Para implementar el simulador de temporizador en cuenta regresiva, se deben considerar los siguientes elementos y reglas:

1. **Ingreso de Datos**:
   - El usuario ingresa la cantidad inicial de horas, minutos y segundos desde la cual desea iniciar el temporizador.
   - Los valores ingresados deben estar dentro de los rangos aceptables:
     - Horas: entre 0 y 23.
     - Minutos: entre 0 y 59.
     - Segundos: entre 0 y 59.
   - Si alguno de los valores está fuera de su rango, se debe mostrar un mensaje de error y solicitar nuevamente el valor.

2. **Cuenta Regresiva**:
   - Una vez ingresados los valores iniciales, el temporizador comienza a contar hacia atrás desde la cantidad especificada, disminuyendo un segundo a la vez.
   - Cada vez que los segundos llegan a cero, se restablecen a 59 y se reduce un minuto.
   - Cada vez que los minutos llegan a cero, se restablecen a 59 y se reduce una hora.
   - La cuenta regresiva se detiene automáticamente cuando se alcanza `0h 0m 0s`.

3. **Visualización**:
   - En cada segundo de la cuenta regresiva, el sistema muestra el tiempo restante en el formato `HH:MM:SS`.
   - Al alcanzar `00:00:00`, el sistema muestra el mensaje **"Tiempo terminado"** y finaliza la simulación.

---

### **Ejemplo de Desarrollo del Temporizador**:

1. El sistema solicita al usuario ingresar las horas, minutos y segundos desde los cuales desea iniciar la cuenta regresiva.
   - Ejemplo: el usuario ingresa 0 horas, 1 minuto y 5 segundos.

2. El temporizador inicia la cuenta regresiva, mostrando cada segundo en pantalla:
   ```
   00:01:05
   00:01:04
   00:01:03
   ...
   00:00:01
   00:00:00
   Tiempo terminado
   ```

---

### **Requerimientos**  

1. El algoritmo debe solicitar al usuario ingresar una cantidad inicial de horas, minutos y segundos.
2. Debe validar que las horas estén entre 0 y 23, y que tanto los minutos como los segundos estén entre 0 y 59. Si el usuario ingresa un valor fuera de estos rangos, el sistema debe mostrar un mensaje de error y solicitar el valor nuevamente hasta que sea correcto.
3. La cuenta regresiva debe iniciar desde el tiempo especificado y reducirse en intervalos de un segundo, ajustando minutos y horas según corresponda, hasta alcanzar `0h 0m 0s`.
4. En cada segundo, el sistema debe mostrar en pantalla el tiempo restante en el formato `HH:MM:SS`.
5. Al llegar a `00:00:00`, el sistema debe detenerse y mostrar el mensaje **"Tiempo terminado"**.
6. El temporizador debe utilizar una estructura de control iterativa del tipo **"Hacer... Repetir"** para disminuir el tiempo hasta alcanzar el valor final de cero.
7. No se deben usar instrucciones rompedoras (como `romper`, `continuar` u otra similar) para finalizar el ciclo.
