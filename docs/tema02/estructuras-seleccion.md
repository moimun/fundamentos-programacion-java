# 2. Estructuras de selección

Las estructuras de selección permiten que un programa pueda tomar decisiones y ejecutar unas instrucciones u otras dependiendo de si se cumple una condición.

Para ello, se utilizan expresiones que devuelven un resultado booleano, es decir, pueden ser `true` (verdadero) o `false` (falso).

El código que se ejecutará dependerá del resultado de esa condición.

## 2.1. Estructura `if`

La estructura `if` permite ejecutar un conjunto de instrucciones solamente cuando se cumple una condición.

Si la condición es verdadera (`true`), se ejecutan las instrucciones que están dentro del bloque `if`. Si es falsa (`false`), se salta ese bloque y el programa continúa con las siguientes instrucciones.

### Sintaxis

```java
if (condicion) {
    // Instrucciones que se ejecutan si la condición es verdadera
}
```

- `if`: indica que vamos a comprobar una condición.
- `condicion`: expresión que devuelve `true` o `false`.
- `{ }`: delimitan el bloque de instrucciones que se ejecutará si se cumple la condición.

### Ejemplo

Vamos a comprobar si una persona es mayor de edad.

```java
int edad = 20;

if (edad >= 18) {
    System.out.println("Eres mayor de edad");
}
```

En este ejemplo, la variable `edad` tiene el valor 20.

Como 20 es mayor o igual que 18, la condición se cumple y aparece el mensaje:

```text
Eres mayor de edad
```

Si la edad fuera inferior a 18, no se ejecutaría el bloque `if` y no aparecería ningún mensaje.

### Cosas que debemos tener en cuenta

- La condición siempre debe escribirse entre paréntesis.
- Si la condición es verdadera, se ejecutan las instrucciones que están entre las llaves.
- Si el bloque `if` solamente tiene una instrucción, las llaves son opcionales.
- La línea que contiene la condición o las llaves no termina en punto y coma (`;`).
- Las instrucciones que están dentro del bloque sí terminan en punto y coma.
- Es recomendable utilizar sangría para que el código sea más fácil de leer.

### Errores habituales

Algunos errores que podemos cometer al utilizar `if` son:

- No poner los paréntesis de la condición.
- Olvidar alguna llave del bloque.
- Poner un punto y coma después de la condición `if`, haciendo que el bloque se ejecute independientemente del resultado.
- No utilizar las llaves cuando tenemos varias instrucciones dentro del bloque.

### Ejercicio: calcular un descuento

El profesor propone crear un programa que aplique un descuento del 8 % cuando el precio de una compra sea igual o superior a 200 €.

El programa debe:

- Pedir al usuario el precio de la compra.
- Comprobar si el precio es igual o superior a 200 €.
- Aplicar el descuento del 8 % cuando se cumpla la condición.
- Mostrar el precio introducido, el descuento aplicado y el precio final.
- Utilizar constantes para definir el precio mínimo y el porcentaje de descuento.

También se propone modificar el ejercicio para aplicar una penalización de 2 € cuando el precio sea inferior a 30 €, teniendo en cuenta que el valor introducido no puede ser negativo.

## 2.2. Estructura `if/else`

La estructura `if/else` permite elegir entre dos posibilidades.

Primero comprueba una condición. Si es verdadera (`true`), ejecuta las instrucciones del bloque `if`. Si es falsa (`false`), ejecuta las instrucciones del bloque `else`.

A diferencia de `if`, aquí siempre se ejecuta uno de los dos bloques.

### Sintaxis

```java
if (condicion) {
    // Instrucciones si la condición es verdadera
} else {
    // Instrucciones si la condición es falsa
}
```

### Ejemplo

Vamos a comprobar si una persona es mayor de edad o menor de edad.

```java
int edad = 16;

if (edad >= 18) {
    System.out.println("Eres mayor de edad");
} else {
    System.out.println("Eres menor de edad");
}
```

En este caso, la variable `edad` tiene el valor 16.

Como la condición `edad >= 18` es falsa, se ejecuta el bloque `else` y aparece:

```text
Eres menor de edad
```

Si la edad fuera 20, se ejecutaría el bloque `if` y aparecería el mensaje de mayor de edad.

### Ejercicio: adivinar un número secreto

El profesor propone crear un programa que permita adivinar un número secreto.

El programa debe:

- Definir un número secreto mediante una constante, con un valor entre 0 y 10.
- Pedir al usuario que introduzca un número entero entre 0 y 10.
- Comprobar que el usuario ha introducido realmente un número entero.
- Mostrar un mensaje de error si el valor introducido no es un número.
- Mostrar un mensaje diferente dependiendo de si el usuario ha acertado o no.
- Mostrar un mensaje indicando que el programa ha terminado.

Como modificación, se propone ampliar el ejercicio:

- Comprobar que el número introducido está entre 0 y 10.
- Utilizar dos números secretos en lugar de uno.
- Generar los números secretos de forma aleatoria.
- Permitir ganar si se acierta al menos uno de los dos números.
- Mostrar un mensaje de aviso y terminar el programa si el usuario no introduce un número.

## 2.3. Estructura `if/else if/else`

La estructura `if/else if/else` permite comprobar varias condiciones diferentes y ejecutar el bloque de instrucciones correspondiente a la primera condición que se cumpla.

Se utiliza cuando tenemos varias posibilidades y necesitamos elegir entre ellas.

Solamente se ejecutará un bloque de todos los disponibles.

Si varias condiciones se cumplen, se ejecutará únicamente la primera, siguiendo el orden en el que aparecen en el código.

El bloque `else` es opcional. Si ninguna condición se cumple y no hemos utilizado `else`, no se ejecutará ninguna de las instrucciones de esa estructura.

### Sintaxis

```java
if (condicion1) {
    // Instrucciones si se cumple la primera condición
} else if (condicion2) {
    // Instrucciones si se cumple la segunda condición
} else if (condicion3) {
    // Instrucciones si se cumple la tercera condición
} else {
    // Instrucciones si no se cumple ninguna condición
}
```

Podemos añadir tantos bloques `else if` como necesitemos.

### Ejemplo: clasificar una nota

Vamos a utilizar esta estructura para indicar el resultado de una nota numérica.

```java
float nota = 8.5f;

if (nota < 5) {
    System.out.println("SUSPENSO");
} else if (nota < 6) {
    System.out.println("SUFICIENTE");
} else if (nota < 7) {
    System.out.println("BIEN");
} else if (nota < 9) {
    System.out.println("NOTABLE");
} else {
    System.out.println("EXCELENTE");
}
```

En este ejemplo, la nota es 8.5.

El programa comprueba las condiciones en orden:

- ¿La nota es inferior a 5? No.
- ¿La nota es inferior a 6? No.
- ¿La nota es inferior a 7? No.
- ¿La nota es inferior a 9? Sí.

Por tanto, aparece:

```text
NOTABLE
```

### Ejercicio: clasificar las notas

El profesor propone crear un programa que pida una nota al usuario y muestre el resultado correspondiente:

- SUSPENSO.
- SUFICIENTE.
- BIEN.
- NOTABLE.
- EXCELENTE.

También debe:

- Comprobar que la nota está dentro del intervalo de 0 a 10.
- Mostrar un mensaje de error si la nota no es correcta.
- Mostrar un mensaje si el usuario introduce un valor que no es un número.

### Ejercicio: aplicar un descuento máximo

Se propone modificar el ejercicio anterior del descuento del 8 %.

El programa debe controlar que:

- El precio introducido no sea negativo.
- El valor introducido sea un número.
- El descuento aplicado no supere los 200 €.
- Si el descuento calculado supera los 200 €, se aplique solamente el descuento máximo.
- Se muestre un mensaje indicando cuándo se aplica ese límite.

## 2.4. Estructura `switch`

La estructura `switch` permite seleccionar qué instrucciones ejecutar dependiendo del valor de una expresión.

A diferencia de `if`, no se basa en comprobar una condición booleana, sino en comparar el resultado de una expresión con diferentes valores concretos.

Puede utilizar expresiones de los siguientes tipos:

- `byte`
- `short`
- `int`
- `long`
- `enum`
- `String`
- `char`

No se pueden utilizar valores reales como `float` o `double`.

### Sintaxis

```java
switch (variable) {
    case valor1:
        // Instrucciones
        break;

    case valor2:
        // Instrucciones
        break;

    case valor3:
        // Instrucciones
        break;

    default:
        // Instrucciones si no coincide ningún valor
}
```

- `switch`: indica la expresión que vamos a comprobar.
- `case`: indica uno de los posibles valores.
- `break`: permite salir del `switch` cuando termina el caso correspondiente.
- `default`: contiene las