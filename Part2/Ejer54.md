### Problema 54: Adivina el Número

**Descripción del problema:**

Escribe un programa que permita al usuario adivinar un número entre 1 y 15 que es generado aleatoriamente por el computador. El usuario tendrá un máximo de **3 intentos** para adivinar el número.

#### Reglas del juego:

1. El programa generará un número aleatorio entre 1 y 15 (ambos inclusive).
   
2. El usuario tendrá 3 intentos para adivinar correctamente el número.
   
3. Después de cada intento, el programa debe indicar si el número ingresado por el usuario es mayor, menor o igual al número generado por el computador.

4. Si el usuario adivina el número correctamente dentro de los 3 intentos, el programa debe mostrar un mensaje felicitando al usuario.
   
5. Si el usuario no adivina el número después de 3 intentos, el programa debe mostrar el número correcto.

#### Entrada:

- El usuario introducirá un número entre 1 y 15 en cada intento.

#### Salida:

- El programa debe dar pistas al usuario después de cada intento: "El número es mayor", "El número es menor", o "¡Adivinaste!"
- Si el usuario no acierta después de 3 intentos, el programa debe mostrar el mensaje: "No adivinaste, el número correcto era X", donde X es el número generado.

#### Ejemplo:

```
El computador ha generado un número entre 1 y 15. Adivina cuál es:

Intento 1: 10
El número es menor.

Intento 2: 6
El número es mayor.

Intento 3: 8
¡Adivinaste!
```

Si el usuario no adivina después de 3 intentos:

```
El computador ha generado un número entre 1 y 15. Adivina cuál es:

Intento 1: 5
El número es mayor.

Intento 2: 12
El número es menor.

Intento 3: 8
No adivinaste, el número correcto era 7.
```
