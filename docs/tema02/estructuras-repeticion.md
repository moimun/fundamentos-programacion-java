
# 3. Estructuras de repetición

Las estructuras de repetición permiten ejecutar varias veces un mismo conjunto de instrucciones mientras se cumpla una determinada condición.

También se conocen como estructuras iterativas y se utilizan cuando necesitamos repetir una operación varias veces sin tener que escribir las mismas instrucciones continuamente.

En Java disponemos de tres estructuras principales de repetición: `while`, `do/while` y `for`.

---

## 3.1. Control de las estructuras de repetición

Antes de estudiar los diferentes tipos de bucles, debemos conocer algunos conceptos relacionados con su funcionamiento.

### Bucle o ciclo

Un **bucle** es un conjunto de instrucciones que se ejecuta varias veces.

La repetición continúa mientras se cumpla una determinada condición.

### Iteración

Una **iteración** es cada una de las ejecuciones individuales que realiza un bucle.

Por ejemplo, si un bucle muestra diez veces un mensaje, habrá realizado diez iteraciones.

### Funcionamiento de un bucle

El funcionamiento general de una estructura de repetición es el siguiente:

1. Se comprueba una condición lógica.
2. Si la condición es verdadera (`true`), se ejecutan las instrucciones del bucle.
3. Se vuelve a comprobar la condición.
4. El proceso continúa mientras la condición sea verdadera.
5. Cuando la condición es falsa (`false`), el bucle termina y el programa continúa con las instrucciones siguientes.

### Bucles infinitos

Un **bucle infinito** es una secuencia de instrucciones que se repite indefinidamente porque nunca llega a cumplirse la condición necesaria para terminarlo.

Por ejemplo:

```java
int i = 0;

while (true) {
    System.out.println("Este bucle no termina");
    i++;
}
```

En este ejemplo, la condición siempre es verdadera porque hemos escrito `true` directamente.

Por tanto, el bucle no termina por sí solo.

Los bucles infinitos pueden consumir recursos del ordenador, especialmente tiempo de procesador (CPU).

Si un programa deja de responder debido a un bucle infinito, podemos detenerlo desde el entorno de desarrollo o desde el sistema operativo.

En Windows también podemos utilizar el comando:

```powershell
taskkill /f /PID numero_proceso
```

### Variables de control

Las variables de control permiten controlar cuántas veces se ejecuta un bucle o cuándo debe terminar.

Podemos encontrar tres tipos principales:

**Contador**

Es una variable, normalmente de tipo entero, que aumenta o disminuye su valor para controlar el número de iteraciones.

Ejemplo:

```java
int contador = 0;

contador++;
```

El operador `++` aumenta el valor de la variable en una unidad.

**Acumulador**

Es una variable que permite ir acumulando diferentes valores o resultados de operaciones.

Ejemplo:

```java
int resultado = 0;

resultado = resultado + 5;
resultado = resultado + 10;
```

Al finalizar, la variable `resultado` tendrá el valor 15.

**Semáforo booleano**

Es una variable de tipo `boolean` que permite indicar si debemos continuar repitiendo las instrucciones o terminar el bucle.

Ejemplo:

```java
boolean continuar = true;
```

Cuando ya no queremos continuar, cambiamos su valor a `false`.

---

## 3.2. Estructura `while`: repetir si se cumple una condición

La estructura `while` permite repetir un conjunto de instrucciones mientras se cumpla una condición lógica.

La condición se comprueba al principio de cada iteración.

Esto significa que, si la condición es falsa desde el primer momento, las instrucciones del bucle no se ejecutarán ninguna vez.

### Sintaxis

```java
// Instrucciones anteriores

while (condicion) {

    // Instrucciones que se repiten

}

// Instrucciones posteriores
```

### Ejemplo 01: mostrar 100 veces Hola Mundo

Vamos a utilizar un contador para mostrar el mensaje Hola Mundo cien veces.

```java
int i = 0;

while (i < 100) {

    System.out.println("Hola Mundo");

    i = i + 1;

}
```

En este ejemplo:

1. Declaramos el contador `i` y le asignamos el valor 0.
2. Comprobamos si `i` es inferior a 100.
3. Si se cumple la condición, mostramos el mensaje.
4. Aumentamos el contador en una unidad.
5. Volvemos a comprobar la condición.

Cuando el contador llega a 100, la condición deja de cumplirse y el bucle termina.

**Modificaciones propuestas por el profesor:**

- Mostrar también el valor del contador en cada línea.
- Pedir al usuario cuántas repeticiones quiere realizar.
- Comprobar que el usuario introduce un número entero válido.

### Utilización del contador

El nombre del contador puede ser cualquiera, aunque es habitual utilizar letras como `i`, `j` o `k`.

También es habitual inicializar el contador a 0 en lugar de 1.

Para comprobar cómo evoluciona el valor de una variable podemos utilizar el modo de depuración (*Debug*) de Eclipse.

Algunas de las opciones disponibles son:

| Acción | Atajo |
|---|---|
| Step Over | F6 |
| Step Into | F5 |
| Step Return | F7 |
| Resume | F8 |
| Stop | Ctrl + F2 |

Estas opciones permiten ejecutar el programa paso a paso y observar cómo cambian los valores de las variables.

### Ejemplo 02: tabla de multiplicar

Podemos aprovechar el contador para realizar operaciones matemáticas dentro del bucle.

En este ejemplo vamos a mostrar la tabla de multiplicar de un número introducido por el usuario.

```java
import java.util.Scanner;

public class TablaMultiplicar {

    public static void main(String[] args) {

        Scanner entrada = new Scanner(System.in);

        int numeroTabla = 0;
        int resultado = 0;
        int i = 1;

        System.out.print("¿Qué tabla de multiplicar quieres? ");
        numeroTabla = entrada.nextInt();

        System.out.println("Esta es la tabla del " + numeroTabla);

        while (i <= 10) {

            resultado = numeroTabla * i;

            System.out.println(numeroTabla + " * " + i + " = " + resultado);

            i = i + 1;
        }
    }
}
```

El contador comienza en 1 y aumenta hasta llegar a 10.

En cada iteración se multiplica el número elegido por el valor del contador.

**Modificación propuesta por el profesor:**

Comprobar que el usuario realmente introduce un número entero.

### Ejemplo 03: acumulador

En este ejemplo vamos a sumar los múltiplos de 3 desde 0 hasta un valor indicado por el usuario.

A diferencia del ejemplo anterior, el contador no aumenta de uno en uno, sino de tres en tres.

```java
import java.util.Scanner;

public class MultiplosTres {

    public static void main(String[] args) {

        int resultado = 0;
        int i = 0;
        int limite = 20;

        Scanner entrada = new Scanner(System.in);

        System.out.print("¿Hasta qué valor quieres sumar los múltiplos de 3? ");
        limite = entrada.nextInt();

        while (i <= limite) {

            System.out.println("Añadimos " + i);

            resultado = resultado + i;

            i = i + 3;
        }

        System.out.println("El resultado final es " + resultado + ".");
    }
}
```

En este programa utilizamos:

- `i` como contador para controlar el bucle.
- `resultado` como acumulador para guardar la suma.
- `limite` para indicar hasta qué valor queremos realizar la operación.

Si el límite es 20, se sumarán los siguientes valores:

```text
0 + 3 + 6 + 9 + 12 + 15 + 18 = 63
```

**Modificaciones propuestas por el profesor:**

- Comprobar que el usuario introduce un número entero.
- Pedir también de qué número quiere sumar los múltiplos, en lugar de utilizar siempre el 3.

### Semáforos booleanos

Los semáforos booleanos permiten controlar cuándo debemos dejar de repetir un bucle.

Se utilizan cuando no podemos calcular previamente cuántas iteraciones serán necesarias y necesitamos repetir las instrucciones hasta que se produzca una situación concreta.

Por ejemplo, podemos utilizar una variable booleana para indicar si el usuario ha acertado un número secreto.

### Ejemplo 04: adivinar un número utilizando un semáforo

Vamos a modificar el ejercicio del número secreto para que el usuario pueda seguir intentándolo hasta acertar.

Utilizaremos una variable booleana llamada `acertado`.

```java
boolean acertado = false;

while (!acertado) {

    // Pedir un número al usuario

    // Comprobar si ha acertado

    // Si acierta:
    // acertado = true;

}
```

Al principio, `acertado` tiene el valor `false`, por lo que el bucle continúa ejecutándose.

Cuando el usuario acierta, cambiamos el valor de la variable a `true`.

En ese momento, la condición `!acertado` pasa a ser falsa y el bucle termina.

**Modificaciones propuestas por el profesor:**

- Comprobar que el usuario introduce un número entero entre 0 y 10.
- Continuar pidiendo el número hasta que sea válido.
- Mostrar un mensaje cuando no acierte para que vuelva a intentarlo.
- Mostrar un mensaje indicando que ha acertado cuando termine el bucle.
- Generar el número secreto de forma aleatoria.
- Permitir que el usuario abandone el juego introduciendo el valor `-1`.
- Mostrar un mensaje cuando el usuario decida retirarse.

---

## 3.3. Estructura `do/while`: repetir al menos una vez

La estructura `do/while` permite repetir un conjunto de instrucciones mientras se cumpla una condición lógica.

Su principal diferencia respecto a `while` es que la condición se comprueba al final de cada iteración.

Por este motivo, las instrucciones del bucle se ejecutan siempre al menos una vez, aunque la condición sea falsa desde el principio.

### Sintaxis

```java
// Instrucciones anteriores

do {

    // Instrucciones que se repiten

} while (condicion);

// Instrucciones posteriores
```

Observa que, a diferencia de `while`, en `do/while` se escribe un punto y coma después de la condición final.

### Ejemplo 05: pedir un número entre 1 y 10

Vamos a pedir al usuario que introduzca un número entre 1 y 10.

Si el valor no es correcto, volveremos a solicitarlo hasta que introduzca uno válido.

```java
import java.util.Scanner;

public class NumeroValido {

    public static void main(String[] args) {

        Scanner entrada = new Scanner(System.in);

        int numero;

        do {

            System.out.print("Introduce un número entre 1 y 10: ");

            numero = entrada.nextInt();

        } while (numero < 1 || numero > 10);

        System.out.println("El número introducido es correcto: " + numero);
    }
}
```

En este ejemplo:

1. Primero solicitamos un número.
2. Después comprobamos si es inferior a 1 o superior a 10.
3. Si alguna de estas condiciones se cumple, volvemos a pedir el número.
4. Cuando el valor está entre 1 y 10, el bucle termina.

Este ejemplo utiliza `do/while` porque necesitamos pedir el dato al menos una vez antes de poder comprobar si es correcto.

Si el ejercicio está bien planteado, también podemos conseguir el mismo resultado utilizando `while`.

### Ejemplo 06: comprobar la primera letra de una palabra

El profesor propone pedir al usuario una palabra que comience por alguna de las siguientes letras:

- b
- m
- s
- t

Utilizaremos `do/while` para continuar solicitando palabras hasta que se introduzca una que cumpla la condición.

Para obtener el primer carácter de una cadena podemos utilizar:

```java
palabra.charAt(0)
```

Antes de comprobar la primera letra debemos asegurarnos de que la palabra no está vacía.

También debemos tener en cuenta que el usuario puede escribir las letras en mayúsculas o minúsculas.

**Modificaciones propuestas por el profesor:**

- Aceptar también las palabras que terminen por las letras indicadas.
- Utilizar `palabra.charAt(palabra.length()-1)` para obtener el último carácter.
- Ignorar los espacios que pueda haber al principio de la palabra utilizando `palabra.trim()`.

---

## 3.4. Estructura `for`: repetir un número determinado de veces

La estructura `for` permite repetir un conjunto de instrucciones un número determinado de veces.

Se utiliza especialmente cuando conocemos el número de repeticiones que queremos realizar o podemos establecerlo mediante un contador.

### Sintaxis

```java
// Instrucciones anteriores

for (inicializacion; condicion; incremento) {

    // Instrucciones que se repiten

}

// Instrucciones posteriores
```

La estructura `for` tiene tres partes principales:

**Inicialización del contador**

Se establece el valor inicial de una variable numérica que utilizaremos como contador.

También podemos declarar la variable directamente dentro del `for`.

**Condición**

Es una expresión booleana que indica si se debe realizar una nueva iteración.

Mientras sea verdadera, el bucle continuará ejecutándose.

**Incremento o decremento**

Es la instrucción que modifica el valor del contador al finalizar cada iteración.

Puede aumentar o disminuir su valor.

### Ejemplo

```java
for (int i = 0; i < 5; i++) {

    System.out.println("Hola Mundo");

}
```

En este caso:

- Inicializamos el contador `i` a 0.
- Comprobamos si `i` es inferior a 5.
- Mostramos el mensaje.
- Incrementamos el contador en una unidad.

El resultado será que el mensaje aparecerá cinco veces.

### Equivalencia entre `for` y `while`

Una estructura `for` puede realizarse también utilizando `while`.

Por ejemplo, estas dos estructuras son equivalentes:

```java
for (int i = 0; i < 5; i++) {

    System.out.println("Hola Mundo");

}
```

Utilizando `while`:

```java
int i = 0;

while (i < 5) {

    System.out.println("Hola Mundo");

    i++;
}
```

La diferencia está en que `for` reúne la inicialización, la condición y el incremento en una misma línea, mientras que `while` los distribuye entre diferentes instrucciones.

### Operadores de incremento y decremento

En Java podemos utilizar operadores que permiten aumentar o disminuir el valor de una variable.

| Operador | Funcionamiento | Equivalencia |
|---|---|---|
| `i++` | Aumenta 1 | `i = i + 1` |
| `i--` | Disminuye 1 | `i = i - 1` |
| `i += 1` | Aumenta 1 | `i = i + 1` |

### Ejemplo 07: tabla de multiplicar ascendente y descendente

El profesor propone mostrar la tabla de multiplicar de un número indicado por el usuario.

Primero se mostrará de forma ascendente, desde 1 hasta 10, y después de forma descendente, desde 10 hasta 1.

Para ello podemos utilizar dos bucles `for`:

```java
import java.util.Scanner;

public class TablaMultiplicar {

    public static void main(String[] args) {

        Scanner entrada = new Scanner(System.in);

        System.out.print("Introduce un número: ");

        int numero = entrada.nextInt();

        System.out.println("Tabla ascendente:");

        for (int i = 1; i <= 10; i++) {

            System.out.println(numero + " * " + i + " = " + (numero * i));
        }

        System.out.println("Tabla descendente:");

        for (int i = 10; i >= 1; i--) {

            System.out.println(numero + " * " + i + " = " + (numero * i));
        }
    }
}
```

### Ejemplo 08: potencias de un número

En este ejercicio se propone mostrar las potencias de 2 hasta alcanzar un límite entero indicado por el usuario.

Por ejemplo, si el límite es 2000, se mostrarán:

```text
2
4
8
16
32
64
128
256
512
1024
```

La siguiente potencia sería 2048, pero ya supera el límite establecido.

Para realizar este ejercicio podemos utilizar el contador del bucle para ir calculando las siguientes potencias.

**Modificación propuesta por el profesor:**

Permitir que el usuario indique también de qué número quiere calcular las potencias.

Por ejemplo, si introduce el número 3 y el límite 1000, el resultado será:

```text
3
9
27
81
243
729
```

---

## 3.5. Combinación con estructuras de selección

Las estructuras de repetición también se pueden combinar con estructuras de selección como `if`, `if/else` y `switch`.

Esto permite realizar comprobaciones y tomar decisiones dentro de un bucle.

De esta manera podemos repetir instrucciones, comprobar diferentes condiciones y decidir qué hacer en cada iteración.

### Ejemplo 09: adivinar un número con tres intentos

Vamos a modificar el ejercicio del número secreto para permitir que el usuario tenga solamente tres intentos.

El programa debe cumplir las siguientes condiciones:

- El usuario dispone de tres intentos para adivinar el número.
- Se debe mostrar cuántos intentos quedan disponibles.
- Si se agotan los intentos, se debe mostrar el número secreto.
- Solamente se descuentan intentos cuando se introduce un número entero válido entre 0 y 10.
- El usuario puede abandonar el juego introduciendo el valor `-1`.

En este ejercicio se combinan las estructuras de repetición con las estructuras de selección para controlar los intentos y comprobar las respuestas.

### Ejemplo 10: mostrar un cuadrado de asteriscos

En este ejercicio se propone crear un programa que muestre un cuadrado formado por asteriscos.

El usuario debe indicar la longitud del lado, que tendrá que estar comprendida entre 2 y 10.

Por ejemplo, si introduce el valor 6, el resultado será:

```text
******
******
******
******
******
******
```

Para realizarlo debemos utilizar dos bucles `for`:

- Un bucle exterior para controlar las filas.
- Un bucle interior para mostrar los asteriscos de cada fila.

Esta estructura se conoce como **bucle anidado**, porque contiene un bucle dentro de otro.

**Modificación propuesta por el profesor:**

Mostrar todos los cuadrados anteriores, comenzando por el lado de longitud 2 hasta llegar al tamaño indicado por el usuario.

Por ejemplo, si el usuario introduce 4, se mostrarán los cuadrados de lados 2, 3 y 4.

### Ejemplo 11: mostrar un triángulo de asteriscos

El último ejercicio del documento propone mostrar un triángulo formado por asteriscos.

El usuario indica la longitud del lado y el programa muestra tantas filas como indique ese valor.

Por ejemplo, para un triángulo de lado 5:

```text
*
**
***
****
*****
```

Para realizar este ejercicio también podemos utilizar bucles `for` anidados.

El bucle exterior controla el número de filas y el interior controla cuántos asteriscos se muestran en cada una.

---

## Resumen del tema

En este apartado hemos aprendido los diferentes tipos de estructuras de repetición que podemos utilizar en Java.

| Estructura | Funcionamiento |
|---|---|
| `while` | Repite las instrucciones mientras se cumpla una condición. |
| `do/while` | Ejecuta las instrucciones al menos una vez y después comprueba la condición. |
| `for` | Repite las instrucciones utilizando un contador y una condición. |

También hemos estudiado:

- Qué es un bucle y qué es una iteración.
- Cómo funcionan los contadores y los acumuladores.
- Cómo utilizar semáforos booleanos.
- Qué es un bucle infinito y cómo evitarlo.
- Cómo utilizar la depuración para observar la ejecución de un bucle.
- Cómo combinar estructuras de repetición y selección.
- Cómo utilizar bucles anidados.

Estas estructuras permiten repetir operaciones y desarrollar programas capaces de realizar tareas de forma automática.

---

[Volver al Tema 02](index.md)

[Volver a la página principal](../index.md)
