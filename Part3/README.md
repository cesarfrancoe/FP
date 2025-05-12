### **Subrutinas**

Las subrutinas, también conocidas como **funciones** o **procedimientos** (o **métodos** en el paradigma orientado a objetos), son bloques de código que realizan una tarea específica y pueden ser llamados desde distintas partes de un programa. Las subrutinas permiten la reutilización del código, la organización y la modularización de los programas, lo que mejora la claridad y el mantenimiento del código.

#### **Tipos de Subrutinas**

1. **Subrutinas sin parámetros y sin retorno de valores**: Son aquellas que no reciben parámetros al ser invocadas, y no devuelven ningún valor. Se utilizan para realizar tareas simples que no dependen de valores externos ni necesitan retornar un resultado.

   **Declaración de la subrutina**:
   ```
   Subrutina Saludar()
       Imprimir "¡Hola, Mundo!"
   FinSubrutina
   ```

   **Llamado a la subrutina**:
   ```
   Llamar Saludar()
   ```

   - **Explicación**: La subrutina `Saludar` no recibe parámetros ni devuelve un valor. Solo imprime un mensaje cuando es llamada.

---

2. **Subrutinas sin parámetros y con retorno de valores**: Estas subrutinas no reciben parámetros, pero sí devuelven un valor como resultado. Son útiles cuando la tarea realizada por la subrutina produce un resultado que debe ser utilizado en otro lugar del programa.

   **Declaración de la subrutina**:
   ```
   Subrutina ObtenerValor()
       Retornar 42
   FinSubrutina
   ```

   **Llamado a la subrutina**:
   ```
   Resultado = Llamar ObtenerValor()
   Imprimir Resultado
   ```

   - **Explicación**: La subrutina `ObtenerValor` no recibe parámetros, pero devuelve el valor 42, que luego es impreso.

---

3. **Subrutinas con parámetros y sin retorno de valores**: Son subrutinas que reciben uno o más **parámetros** al ser invocadas, pero no devuelven ningún valor. Los **argumentos** son los valores que se pasan a estos parámetros al momento de llamar a la subrutina. Se utilizan cuando se necesita realizar una operación que depende de los parámetros, pero no es necesario devolver un resultado.

   **Declaración de la subrutina**:
   ```
   Subrutina ImprimirSuma(A, B)
       Resultado = A + B
       Imprimir Resultado
   FinSubrutina
   ```

   **Llamado a la subrutina**:
   ```
   Llamar ImprimirSuma(5, 10)
   ```

   - **Explicación**: La subrutina `ImprimirSuma` recibe dos **parámetros**, **A** y **B**, que son asignados a los **argumentos** 5 y 10 cuando se llama a la subrutina. Luego, se suma el valor de los parámetros y se imprime el resultado.

---

4. **Subrutinas con parámetros y con retorno de valores**: Estas subrutinas reciben uno o más **parámetros** y, además, devuelven un valor como resultado. Los **argumentos** son los valores que se pasan a esos parámetros al invocar la subrutina. Son útiles cuando la operación realizada depende de los parámetros y el resultado debe ser utilizado en otra parte del programa.

   **Declaración de la subrutina**:
   ```
   Subrutina Multiplicar(A, B)
       Retornar A * B
   FinSubrutina
   ```

   **Llamado a la subrutina**:
   ```
   Resultado = Llamar Multiplicar(4, 3)
   Imprimir Resultado
   ```

   - **Explicación**: La subrutina `Multiplicar` recibe dos **parámetros**, **A** y **B**, que corresponden a los **argumentos** 4 y 3 cuando se llama a la subrutina. La subrutina realiza la multiplicación y devuelve el resultado, que luego se imprime.

---

#### **Ventajas del uso de Subrutinas**

1. **Reutilización de código**: Las subrutinas permiten escribir un código que puede ser reutilizado en varias partes del programa, evitando duplicaciones y haciendo el código más eficiente.
   
2. **Modularidad**: Facilitan la organización del código, ya que dividen el programa en partes más pequeñas y manejables.
   
3. **Mantenimiento más sencillo**: Al estar agrupadas las tareas en subrutinas, los cambios y ajustes en una funcionalidad específica se pueden realizar de manera más sencilla sin afectar otras partes del código.
   
4. **Legibilidad**: El uso de subrutinas permite que el programa sea más claro y fácil de entender, ya que cada subrutina tiene una responsabilidad bien definida.

---

#### **Consideraciones**

- Es importante nombrar las subrutinas de manera clara, para que su propósito sea comprensible con solo ver su nombre.
- En algunos lenguajes, las subrutinas pueden tener un **valor de retorno**. Si una subrutina no devuelve un valor, se denomina **procedimiento**.

---

### **Resumen**

Las subrutinas (o **métodos** en el paradigma orientado a objetos) son bloques de código reutilizables que permiten modularizar y organizar programas de manera más eficiente. Existen cuatro tipos principales de subrutinas:

1. **Sin parámetros y sin retorno de valores**
2. **Sin parámetros y con retorno de valores**
3. **Con parámetros y sin retorno de valores**
4. **Con parámetros y con retorno de valores**

El uso adecuado de las subrutinas facilita la reutilización del código, mejora la legibilidad del programa y facilita su mantenimiento.

### **Tabla Resumen de Tipos de Subrutinas**

| Tipo | ¿Recibe Parámetros? | ¿Devuelve Valor? | Ejemplo              | Comentario                                        |
| ---- | ------------------- | ---------------- | -------------------- | ------------------------------------------------- |
| 1    | ❌ No                | ❌ No             | `Saludar()`          | Solo ejecuta una acción (ej. imprimir un mensaje) |
| 2    | ❌ No                | ✅ Sí             | `ObtenerValor()`     | Devuelve un valor fijo o calculado                |
| 3    | ✅ Sí                | ❌ No             | `ImprimirSuma(A, B)` | Usa parámetros para operar, pero no retorna valor |
| 4    | ✅ Sí                | ✅ Sí             | `Multiplicar(A, B)`  | Usa parámetros y retorna un valor                 |


