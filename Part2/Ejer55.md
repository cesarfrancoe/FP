### Problema 55: El computador adivina un número

**Descripción del problema:**

Escribe un algoritmo en el que el computador trate de adivinar un número entre 1 y 15 que el usuario haya pensado. El computador tendrá un máximo de **3 intentos** para adivinar el número, y el usuario debe darle pistas indicando si el número que propone el computador es mayor o menor que el que ha pensado.

#### Reglas del juego:

1. El usuario debe pensar en un número entre 1 y 15 (sin decírselo al programa).
   
2. El computador intentará adivinar el número que el usuario pensó, haciendo una propuesta de número en cada intento.

3. Después de cada intento del computador, el usuario debe responder si el número es "mayor", "menor" o si "adivinó" correctamente.

4. El computador tendrá un máximo de 3 intentos para adivinar el número.

5. Si el computador adivina el número en cualquiera de los intentos, el programa debe mostrar un mensaje de felicitación.
   
6. Si el computador no acierta después de 3 intentos, el programa debe mostrar un mensaje indicando que no logró adivinar.

#### Entrada:

- El usuario pensará en un número y luego deberá ingresar una pista en cada intento del computador: "mayor", "menor" o "adivinaste".

#### Salida:

- El programa debe mostrar la propuesta de número del computador y luego esperar la pista del usuario.
- Si el computador adivina el número, el programa debe mostrar: "¡El computador adivinó correctamente!"
- Si el computador no adivina en 3 intentos, el programa debe mostrar: "El computador no logró adivinar tu número."

#### Ejemplo:

```
Piensa en un número entre 1 y 15. El computador intentará adivinarlo.

Intento 1: ¿Es el número 8?
No
¿El número es mayor (S/N)? S

Intento 2: ¿Es el número 12?
No
¿El número es mayor (S/N)? N

Intento 3: ¿Es el número 10?
Si ¡adivinaste!

¡El computador adivinó correctamente!
```

Si el computador no adivina después de 3 intentos:

```
Piensa en un número entre 1 y 15. El computador intentará adivinarlo.

Intento 1: ¿Es el número 7?
No
¿El número es mayor (S/N)? S

Intento 2: ¿Es el número 11?
No
¿El número es mayor (S/N)? N

Intento 3: ¿Es el número 9?
No

El computador no logró adivinar tu número.
```
