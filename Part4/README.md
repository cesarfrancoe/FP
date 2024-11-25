### **Subrutinas**

Las subrutinas, también conocidas como **funciones** o **procedimientos** (o **métodos** en el paradigma orientado a objetos), son bloques de código que realizan una tarea específica y pueden ser llamados desde distintas partes de un programa. Las subrutinas permiten la reutilización del código, la organización y la modularización de los programas, lo que mejora la claridad y el mantenimiento del código.

#### **Tipos de Subrutinas**

1. **Subrutinas sin parámetros y sin retorno de valores**: Son aquellas que no reciben parámetros al ser invocadas, y no devuelven ningún valor. Se utilizan para realizar tareas simples que no dependen de valores externos ni necesitan retornar un resultado.

   **Ejemplo de pseudocódigo**:
   ```
   Subrutina Saludar()
       Imprimir "¡Hola, Mundo!"
   FinSubrutina

   Llamar Saludar()
   ```

   - **Explicación**: La subrutina `Saludar` no recibe parámetros ni devuelve un valor. Solo imprime un mensaje cuando es llamada.

---

2. **Subrutinas sin parámetros y con retorno de valores**: Estas subrutinas no reciben parámetros, pero sí devuelven un valor como resultado. Son útiles cuando la tarea realizada por la subrutina produce un resultado que debe ser utilizado en otro lugar del programa.

   **Ejemplo de pseudocódigo**:
   ```
   Subrutina ObtenerValor()
       Retornar 42
   FinSubrutina

   Resultado = Llamar ObtenerValor()
   Imprimir Resultado
   ```

   - **Explicación**: La subrutina `ObtenerValor` no recibe parámetros, pero devuelve el valor 42, que luego es impreso.

---

3. **Subrutinas con parámetros y sin retorno de valores**: Son subrutinas que reciben uno o más parámetros al ser invocadas, pero no devuelven ningún valor. Se utilizan cuando se necesita realizar una operación que depende de los parámetros, pero no es necesario devolver un resultado.

   **Ejemplo de pseudocódigo**:
   ```
   Subrutina ImprimirSuma(A, B)
       Resultado = A + B
       Imprimir Resultado
   FinSubrutina

   Llamar ImprimirSuma(5, 10)
   ```

   - **Explicación**: La subrutina `ImprimirSuma` recibe dos parámetros, `A` y `B`, los suma y luego imprime el resultado sin devolver ningún valor.

---

4. **Subrutinas con parámetros y con retorno de valores**: Estas subrutinas reciben uno o más parámetros y, además, devuelven un valor como resultado. Son útiles cuando la operación realizada depende de los parámetros y el resultado debe ser utilizado en otra parte del programa.

   **Ejemplo de pseudocódigo**:
   ```
   Subrutina Multiplicar(A, B)
       Retornar A * B
   FinSubrutina

   Resultado = Llamar Multiplicar(4, 3)
   Imprimir Resultado
   ```

   - **Explicación**: La subrutina `Multiplicar` recibe dos parámetros, los multiplica y devuelve el resultado, que luego se imprime.

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

Las subrutinas (o **métodos** en el paradigma orientado a objetos) son una herramienta fundamental para la organización, reutilización y modularización del código. Existen diferentes tipos, como las que no reciben parámetros y no retornan valores, las que no reciben parámetros pero retornan valores, las que reciben parámetros pero no retornan valores, y las que reciben parámetros y retornan valores. Utilizar subrutinas correctamente permite escribir programas más eficientes, legibles y fáciles de mantener.
