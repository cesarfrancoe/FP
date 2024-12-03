### **Arreglos Estáticos Unidimensionales**

Un **arreglo estático unidimensional** es una estructura de datos que almacena una colección de elementos del mismo tipo, donde el número de elementos es fijo y conocido en tiempo de compilación. Los arreglos son útiles para almacenar colecciones de datos cuando el tamaño de la colección no cambia durante la ejecución del programa.

#### **Declaración de un Arreglo Unidimensional**

La declaración de un arreglo unidimensional se hace especificando el tipo de los elementos y el tamaño del arreglo. El tamaño debe ser conocido de antemano, ya que los arreglos estáticos tienen una longitud fija.

**Ejemplo de declaración**:
```
Arreglo A[10]  // Declara un arreglo de 10 elementos
```

- **Explicación**: El arreglo `A` tiene 10 elementos, con índices que van de 0 a 9.

---

#### **Inicialización de un Arreglo**

Un arreglo puede ser inicializado de manera manual, asignando valores a cada uno de sus elementos, o de manera automática, utilizando un valor predeterminado.

**Ejemplo de inicialización manual**:
```
Arreglo A[5] = {1, 2, 3, 4, 5}  // Inicializa un arreglo con 5 elementos
```

- **Explicación**: El arreglo `A` contiene los valores 1, 2, 3, 4 y 5 en las posiciones de índice 0 a 4.

**Ejemplo de inicialización automática**:
```
Arreglo A[5] = {0}  // Inicializa todos los elementos con el valor 0
```

- **Explicación**: Todos los elementos del arreglo `A` son inicializados con el valor 0.

---

#### **Acceso a los Elementos de un Arreglo**

Para acceder a los elementos de un arreglo, se utiliza su índice. Los índices comienzan desde 0 y van hasta el tamaño del arreglo menos uno.

**Ejemplo de acceso a elementos**:
```
Valor = A[2]  // Accede al tercer elemento del arreglo A
```

- **Explicación**: El valor almacenado en la posición de índice 2 de `A` es asignado a la variable `Valor`.

---

#### **Modificación de Elementos en un Arreglo**

Los elementos de un arreglo pueden ser modificados directamente utilizando su índice.

**Ejemplo de modificación**:
```
A[4] = 10  // Asigna el valor 10 al quinto elemento de A
```

- **Explicación**: El valor del quinto elemento del arreglo `A` (en la posición de índice 4) es cambiado a 10.

---

#### **Recorrido de un Arreglo**

Para recorrer un arreglo y realizar una operación con cada uno de sus elementos, se utiliza un ciclo (como un ciclo `Para` o `Mientras`).

**Ejemplo de recorrido utilizando ciclo `Para`**:
```
Para i = 0 Hasta 4 Hacer
    Imprimir A[i]
FinPara
```

- **Explicación**: Este ciclo recorre el arreglo `A` desde el índice 0 hasta el índice 4, imprimiendo cada uno de los elementos del arreglo.

---

#### **Búsqueda en un Arreglo**

La búsqueda de un elemento en un arreglo implica recorrer el arreglo y comparar cada elemento con el valor buscado. 

**Ejemplo de búsqueda lineal**:
```
Subrutina BuscarElemento(Arreglo A, ValorBuscado)
    Para i = 0 Hasta 4 Hacer
        Si A[i] == ValorBuscado Entonces
            Retornar i  // Retorna el índice del elemento encontrado
        FinSi
    FinPara
    Retornar -1  // Retorna -1 si el valor no se encuentra
FinSubrutina
```

- **Explicación**: La subrutina `BuscarElemento` recorre el arreglo `A` buscando el valor `ValorBuscado`. Si lo encuentra, retorna el índice del elemento; de lo contrario, retorna -1 indicando que no se encontró el valor.

---

#### **Ventajas de los Arreglos Estáticos Unidimensionales**

1. **Acceso rápido**: Los elementos de un arreglo se pueden acceder rápidamente mediante su índice, lo que hace que la búsqueda y modificación de elementos sean eficientes.
   
2. **Simplicidad**: Los arreglos son fáciles de entender y usar, lo que los hace una estructura ideal para muchas aplicaciones sencillas.

3. **Eficiencia de memoria**: Los arreglos estáticos ocupan un bloque contiguo de memoria, lo que permite un uso eficiente del espacio.

---

#### **Consideraciones**

- El tamaño de los arreglos estáticos debe ser conocido en tiempo de compilación. Si se necesita cambiar el tamaño del arreglo en tiempo de ejecución, se debe considerar el uso de estructuras dinámicas, como listas o vectores.
- Los índices en un arreglo están limitados por el tamaño declarado. Acceder a un índice fuera de los límites del arreglo puede causar errores de ejecución.

---

### **Resumen**

Los **arreglos estáticos unidimensionales** son estructuras de datos sencillas pero poderosas que permiten almacenar colecciones de elementos del mismo tipo en un bloque de memoria contigua. Son útiles cuando el número de elementos es fijo y conocido, y permiten un acceso rápido a los elementos mediante índices. Existen diversas operaciones que se pueden realizar sobre arreglos, como la inicialización, el acceso, la modificación, el recorrido y la búsqueda.
