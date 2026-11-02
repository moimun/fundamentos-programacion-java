
# Arrays

## 1. Declaración e inicialización de arrays

Un **array** es una estructura que permite almacenar varios valores del mismo tipo de dato utilizando un único identificador.

Cada valor se guarda en una posición diferente y estas posiciones siguen un orden numérico.

A efectos prácticos, cada posición individual de un array se comporta como una variable del tipo de dato elegido.

Con un array podemos:

- Consultar el valor almacenado en una posición.
- Guardar nuevos datos en sus diferentes posiciones.
- Acceder a cada elemento utilizando su índice.

### 1.1. Declaración de un array

Para utilizar un array en Java, primero debemos declararlo e inicializarlo.

La declaración indica qué tipo de datos vamos a almacenar y qué nombre tendrá el array.

Por ejemplo:

```java
int[] arrayEnters;
```

En este caso hemos declarado un array llamado `arrayEnters` que podrá almacenar números enteros (`int`).

También podemos declarar arrays de otros tipos de datos:

```java
int[] arrayEnters;
double[] arrayReals;
float[] arrayDecimals;
char[] arrayCaracters;
String[] arrayCadenes;
```

### 1.2. Inicialización de un array

Antes de utilizar un array es obligatorio inicializarlo.

En Java, cuando inicializamos un array, su tamaño debe ser conocido. Una vez creado con un número determinado de posiciones, su tamaño ya no puede cambiar.

Existen diferentes formas de inicializar un array.

**Inicialización con valores concretos**

Podemos crear un array indicando directamente los valores que queremos almacenar.

Sintaxis:

```java
tipoDato[] nombreArray = {valor1, valor2, valor3};
```

Ejemplo:

```java
int[] arrayEnters = {10, 20, 30, 40, 50};
```

En este caso hemos creado un array de números enteros con cinco posiciones.

Cada posición contiene uno de los valores indicados.

**Inicialización con valores por defecto**

También podemos crear un array indicando únicamente el número de posiciones que queremos reservar.

Sintaxis:

```java
tipoDato[] nombreArray = new tipoDato[tamaño];
```

Ejemplo:

```java
double[] arrayReals = new double[10];
```

En este caso hemos creado un array de tipo `double` con diez posiciones.

Java inicializa automáticamente sus elementos con el valor por defecto correspondiente al tipo de dato.

Los valores por defecto son:

| Tipo de dato | Valor por defecto |
|---|---|
| `byte`, `short`, `int`, `long` | `0` |
| `double`, `float` | `0.0` |
| `boolean` | `false` |
| `char` | `0` |
| `String` | `null` |
| Objetos en general | `null` |

Por ejemplo, las siguientes instrucciones son equivalentes:

```java
double[] arrayReals = new double[10];
```

```java
double[] arrayReals = {
    0.0, 0.0, 0.0, 0.0, 0.0,
    0.0, 0.0, 0.0, 0.0, 0.0
};
```

### 1.3. Inicialización de todos los elementos con un mismo valor

También podemos inicializar un array asignando el mismo valor a todas sus posiciones mediante un bucle `for`.

Por ejemplo, vamos a crear un array de 30 números enteros y asignar el valor 7 a todos sus elementos.

```java
int[] arrayEnters2 = new int[30];

for (int i = 0; i < arrayEnters2.length; i++) {
    arrayEnters2[i] = 7;
}
```

En este ejemplo:

- Creamos un array de 30 posiciones.
- Utilizamos un bucle `for` para recorrer todas sus posiciones.
- Asignamos el valor 7 a cada posición.

Para mostrar su contenido podemos utilizar otro bucle:

```java
for (int i = 0; i < arrayEnters2.length; i++) {
    System.out.println(i + ": " + arrayEnters2[i]);
}
```

El resultado mostrará las posiciones del array y el valor almacenado en cada una.

### 1.4. Consideraciones sobre la inicialización

Debemos tener en cuenta algunas características de los arrays en Java:

- Antes de utilizar un array es obligatorio inicializarlo.
- Cuando se crea un array, su tamaño debe estar definido.
- Una vez inicializado, el tamaño del array no puede cambiar.
- Cada posición almacena un valor del tipo de dato declarado.
- Si utilizamos `new`, Java asigna automáticamente los valores por defecto.

---

[Siguiente apartado: Manipulación de datos dentro de arrays](#2-manipulacion-de-datos-dentro-de-arrays)



## 2. Manipulación de datos dentro de arrays

Los arrays tienen algunas particularidades a la hora de trabajar con ellos. A diferencia de las variables normales, no podemos realizar operaciones directamente sobre un array completo.

Por ejemplo, en Java no podemos sumar dos arrays utilizando directamente el operador `+`.

```java
int[] arrayA = {10, 20, 30, 40, 50};
int[] arrayB = {50, 60, 70, 80, 100};

// Esta operación no es válida:
int[] arrayC = arrayA + arrayB;
```

Esta operación produce un error de compilación.

Para trabajar con los datos almacenados en un array debemos manipularlos individualmente, posición por posición.

Cada posición se comporta como una variable del tipo de dato elegido, por lo que podemos consultar su valor y almacenar nuevos datos.

### 2.1. Acceder a las posiciones de un array: índices

Para acceder a un elemento de un array utilizamos un número entero llamado **índice**.

El índice indica la posición que ocupa un elemento dentro del array.

La sintaxis es:

```java
nombreArray[indice]
```

En Java, los índices comienzan siempre en 0:

- Primera posición: índice 0.
- Segunda posición: índice 1.
- Tercera posición: índice 2.
- Última posición: tamaño del array menos 1.

Por ejemplo, tenemos el siguiente array:

```java
int[] arrayA = {10, 20, 30, 40, 50};
```

Su distribución sería:

| Índice | Valor almacenado |
|---:|---:|
| 0 | 10 |
| 1 | 20 |
| 2 | 30 |
| 3 | 40 |
| 4 | 50 |

Para consultar un elemento podemos escribir:

```java
System.out.println(arrayA[0]);
System.out.println(arrayA[2]);
System.out.println(arrayA[4]);
```

El resultado será:

```text
10
30
50
```

### 2.2. Modificar los elementos de un array

También podemos cambiar el valor almacenado en una posición concreta utilizando el operador de asignación `=`.

Por ejemplo:

```java
int[] arrayA = {10, 20, 30, 40, 50};

// Modificamos el valor de la posición 2
arrayA[2] = 100;

System.out.println(arrayA[2]);
```

Resultado:

```text
100
```

El valor anterior, que era 30, ha sido sustituido por 100.

### 2.3. Realizar operaciones con elementos de diferentes arrays

Podemos consultar elementos de distintos arrays y realizar operaciones con ellos.

Para ello debemos indicar las posiciones concretas que queremos utilizar.

Ejemplo:

```java
int[] arrayA = {10, 20, 30, 40, 50};
int[] arrayB = {50, 60, 70, 80, 100};
int[] arrayC = new int[5];

// La variable r tendrá el valor 140
int r = arrayA[3] + arrayB[4];

// Guardamos el resultado en la segunda posición de arrayC
arrayC[1] = r + arrayA[0];
```

En este ejemplo:

- `arrayA[3]` contiene el valor 40.
- `arrayB[4]` contiene el valor 100.
- La variable `r` almacena el resultado de sumar 40 + 100, que es 140.
- `arrayA[0]` contiene el valor 10.
- `arrayC[1]` almacena el resultado de sumar 140 + 10, que es 150.

Por tanto, el valor de la segunda posición de `arrayC` será 150.

### 2.4. Errores al acceder a las posiciones

Debemos tener cuidado al consultar o modificar las posiciones de un array.

No podemos utilizar índices negativos ni índices iguales o superiores al tamaño del array.

Por ejemplo:

```java
int[] arrayA = {10, 20, 30, 40, 50};

// El array tiene 5 posiciones.
// Los índices válidos van de 0 a 4.

// Esta asignación es incorrecta:
arrayA[5] = 60;

// Esta consulta también es incorrecta:
int r = arrayA[2] + arrayA[4] + arrayA[6];
```

En ambos casos se intenta acceder a posiciones que no existen.

Al ejecutar estas instrucciones se puede producir una excepción llamada:

`IndexOutOfBoundsException`

Este error aparece cuando intentamos acceder a una posición que está fuera de los límites permitidos.

### 2.5. Atributo `length`

Para evitar errores al recorrer un array o acceder a sus posiciones, podemos utilizar el atributo `length`.

Este atributo permite conocer el número total de elementos que contiene un array.

La sintaxis es:

```java
nombreArray.length
```

Hay que recordar que `length` no lleva paréntesis.

Por ejemplo:

```java
int[] arrayA = {10, 20, 30, 40, 50};

System.out.println(arrayA.length);
```

Resultado:

```text
5
```

Aunque el tamaño del array es 5, su último índice es 4, porque las posiciones comienzan en 0.

Podemos utilizar `length` para comprobar si una posición existe antes de acceder a ella.

Ejemplo:

```java
int[] arrayA = {10, 20, 30, 40, 50};

int index = 6;

if (index < arrayA.length) {

    System.out.println("La posición " + index + " vale " + arrayA[index]);

} else {

    System.out.println("Este array no tiene tantas posiciones!");

}
```

Resultado:

```text
Este array no tiene tantas posiciones!
```

En este caso, el índice 6 no es válido porque el array solamente tiene cinco posiciones.

### 2.6. Recorrer un array

Para consultar todos los elementos de un array podemos utilizar un bucle `for`.

El contador del bucle nos permite acceder a cada posición siguiendo el orden de sus índices.

Ejemplo:

```java
int[] arrayA = {10, 20, 30, 40, 50};

for (int i = 0; i < arrayA.length; i++) {

    System.out.println(arrayA[i]);

}
```

Resultado:

```text
10
20
30
40
50
```

En este ejemplo:

- El contador `i` comienza en 0.
- La condición comprueba que `i` sea inferior al tamaño del array.
- En cada repetición mostramos el elemento situado en la posición `i`.
- El contador aumenta una unidad.
- Cuando `i` alcanza el valor 5, el bucle termina.

Utilizar `arrayA.length` permite adaptar el recorrido al tamaño del array sin tener que escribir manualmente el número de posiciones.

---

[Volver al apartado anterior](#1-declaracion-e-inicializacion-de-arrays)

[Siguiente apartado: Almacenamiento de la entrada de datos en un array](#3-almacenamiento-de-la-entrada-de-datos-en-un-array)



## 3. Almacenamiento de la entrada de datos en un array

En muchas ocasiones necesitamos almacenar varios datos introducidos por el usuario dentro de un array.

Para realizar esta operación utilizamos la clase `Scanner` junto con un bucle que permita leer los diferentes valores y guardarlos en las posiciones correspondientes.

Antes de empezar debemos tener en cuenta que el tamaño de un array se establece cuando lo creamos y no puede modificarse posteriormente.

### 3.1. Leer varios valores utilizando Scanner

Cuando utilizamos una instrucción como `nextInt()`, `nextDouble()` o `nextLong()`, el programa se detiene esperando que el usuario introduzca datos por teclado.

Sin embargo, el usuario puede introducir varios valores antes de pulsar la tecla Enter.

Por ejemplo:

```text
10 20 30 40 50
```

En este caso, los valores están separados por espacios y `Scanner` puede identificarlos individualmente.

Cuando introducimos varios valores en una misma línea, estos quedan pendientes de lectura.

Las siguientes llamadas a los métodos `next...()` irán recogiendo los valores pendientes sin necesidad de volver a esperar una nueva entrada del usuario.

Cuando se han leído todos los valores introducidos, el programa volverá a esperar una nueva entrada por teclado.

### 3.2. Comprobar el tipo de dato introducido

Cuando leemos varios valores por teclado, debemos tener en cuenta que el usuario puede introducir datos de diferentes tipos.

Esto puede ocurrir por un error al escribir o porque el programa realmente espera una secuencia de valores de distintos tipos.

Antes de realizar una lectura podemos comprobar si el siguiente dato es del tipo que necesitamos.

Para ello utilizamos los métodos `hasNext...()` de la clase `Scanner`.

Algunos ejemplos son:

| Método | Tipo de dato |
|---|---|
| `hasNextInt()` | Número entero |
| `hasNextDouble()` | Número real |
| `hasNextLong()` | Número entero de tipo long |

Ejemplo:

```java
if (entrada.hasNextInt()) {
    int numero = entrada.nextInt();
} else {
    System.out.println("El dato introducido no es un entero");
}
```

De esta manera podemos comprobar el tipo de dato antes de intentar leerlo.

### 3.3. Leer una cantidad conocida de datos

Cuando conocemos previamente cuántos valores vamos a almacenar, podemos utilizar un array de tamaño fijo y un bucle con contador.

El tamaño del array debe establecerse antes de comenzar a guardar los datos.

Por ejemplo, si queremos almacenar cinco números enteros:

```java
import java.util.Scanner;

public class EntradaValoresConocidos {

    public static void main(String[] args) {

        Scanner entrada = new Scanner(System.in);

        int[] numeros = new int[5];

        for (int i = 0; i < numeros.length; i++) {

            System.out.print("Introduce un número: ");

            numeros[i] = entrada.nextInt();
        }

        System.out.println("Los números introducidos son:");

        for (int i = 0; i < numeros.length; i++) {

            System.out.println(numeros[i]);
        }
    }
}
```

En este ejemplo:

1. Creamos un array de cinco posiciones.
2. Utilizamos un bucle `for` para recorrer todas las posiciones.
3. Pedimos un número al usuario en cada repetición.
4. Guardamos el número directamente en la posición correspondiente.
5. Al terminar, recorremos el array para mostrar todos los valores.

De esta manera, cada número queda almacenado en una posición diferente.

### 3.4. Leer una cantidad desconocida de datos

En otras ocasiones no conocemos previamente cuántos valores va a introducir el usuario.

En estos casos podemos utilizar dos posibilidades:

- Hacer que el primer dato introducido indique cuántos valores se van a guardar.
- Utilizar un valor especial para indicar que hemos terminado de introducir datos.

**Primera opción: indicar la cantidad de datos**

El usuario introduce primero un número que indica cuántos valores quiere almacenar.

Por ejemplo, si introduce el valor 4, el programa reservará cuatro posiciones y solicitará cuatro números.

```java
import java.util.Scanner;

public class EntradaCantidadDatos {

    public static void main(String[] args) {

        Scanner entrada = new Scanner(System.in);

        System.out.print("¿Cuántos números quieres introducir? ");

        int cantidad = entrada.nextInt();

        int[] numeros = new int[cantidad];

        for (int i = 0; i < numeros.length; i++) {

            System.out.print("Introduce un número: ");

            numeros[i] = entrada.nextInt();
        }

        System.out.println("Valores introducidos:");

        for (int i = 0; i < numeros.length; i++) {

            System.out.println(numeros[i]);
        }
    }
}
```

En este ejemplo, el tamaño del array depende de la cantidad indicada por el usuario.

**Segunda opción: utilizar una marca de final de secuencia**

Otra posibilidad consiste en permitir que el usuario introduzca valores hasta que escriba un número especial que indique que ha terminado.

Este valor se conoce como **marca de final de secuencia**.

La marca debe cumplir dos condiciones:

- Debe ser un valor único.
- No puede aparecer entre los valores que queremos almacenar.

Para controlar cuándo termina la entrada podemos utilizar un semáforo booleano.

Por ejemplo, podemos utilizar el valor `-1` como marca de final, siempre que no necesitemos almacenar números negativos.

La variable booleana indicará si se ha encontrado la marca de final de secuencia.

### 3.5. Almacenar datos en arrays parcialmente ocupados

Cuando no conocemos cuántos datos va a introducir el usuario, podemos encontrarnos con un problema: el tamaño de los arrays no puede cambiar una vez creados.

Una solución consiste en elegir previamente un tamaño máximo para el array.

Por ejemplo, podemos crear un array de 100 posiciones aunque el usuario solamente introduzca 20 valores.

En ese caso tendremos un array parcialmente ocupado.

Esto significa que algunas posiciones contienen datos introducidos por el usuario y otras todavía no se han utilizado.

Debemos tener en cuenta que:

- No podemos conocer siempre la cantidad total de datos que se introducirán.
- Si se introducen más datos de los que permite el array, los datos adicionales se ignoran.
- Debemos elegir un tamaño que permita almacenar suficientes valores.
- Tampoco debemos reservar una cantidad excesiva de memoria sin necesidad.

Por tanto, debemos buscar un equilibrio entre disponer de suficientes posiciones y no desperdiciar memoria.

---

[Siguiente apartado: Esquemas fundamentales en la utilización de arrays](#4-esquemas-fundamentales-en-la-utilizacion-de-arrays)




## 4. Esquemas fundamentales en la utilización de arrays

Para trabajar con arrays existen diferentes estrategias que nos permiten organizar las operaciones y resolver problemas habituales de programación.

Estas estrategias utilizan principalmente bucles, índices y contadores para recorrer, consultar, modificar y ordenar los elementos almacenados.

El profesor presenta siete estrategias fundamentales:

- Iniciación procedural.
- Recorrido.
- Búsqueda.
- Arrays auxiliares.
- Copia.
- Cambio de tamaño.
- Ordenación.

### 4.1. Iniciación procedural

La **generación procedural** consiste en generar el contenido de un array mediante instrucciones y operaciones, en lugar de introducir manualmente todos sus valores.

Esta técnica permite crear arrays cuyos elementos siguen un patrón determinado.

Se utiliza especialmente en el diseño de videojuegos, aunque también podemos aplicarla en otros programas.

**Ejemplo 01: generar un array con el doble del valor anterior**

El ejercicio consiste en inicializar un array de 15 elementos de manera que cada posición tenga el doble del valor de la posición anterior.

El primer elemento tendrá el valor 1.

El resultado esperado es:

```text
[1, 2, 4, 8, 16, 32, 64, 128, 256, 512, 1024, 2048, 4096, 8192, 16384]
```

Podemos resolverlo utilizando un bucle `for`:

```java
int[] arrayNumeros = new int[15];

arrayNumeros[0] = 1;

for (int i = 1; i < arrayNumeros.length; i++) {

    arrayNumeros[i] = arrayNumeros[i - 1] * 2;

}

System.out.println("Elementos del array:");

for (int i = 0; i < arrayNumeros.length; i++) {

    System.out.println(arrayNumeros[i]);

}
```

En este ejemplo:

1. Creamos un array de 15 posiciones.
2. Asignamos el valor 1 a la primera posición.
3. Recorremos el resto de posiciones mediante un bucle.
4. Multiplicamos por 2 el valor de la posición anterior.
5. Guardamos el resultado en la posición actual.

De esta manera generamos todos los valores automáticamente.

### 4.2. Recorrido

El **recorrido de un array** consiste en visitar sus posiciones de forma secuencial para realizar operaciones con todos o parte de los valores almacenados.

Normalmente utilizamos un bucle `for` para recorrer los elementos y realizar los cálculos necesarios.

Entre las operaciones que podemos realizar encontramos:

- Sumar todos los elementos.
- Calcular una media.
- Contar determinados valores.
- Buscar el valor mayor o menor.
- Comprobar si se cumple una condición.

**Ejemplo 02: calcular la nota media**

Partimos del siguiente array de notas:

```java
float[] arrayNotas = {
    4.9f, 5.5f, 9f, 10f, 6.7f, 8.2f,
    7.5f, 5f, 8.3f, 5.1f, 9f, 7f
};
```

El ejercicio consiste en calcular la nota media de todos los alumnos y mostrar el resultado.

Para hacerlo debemos sumar todas las notas y dividir el resultado entre la cantidad de elementos del array.

```java
float[] arrayNotas = {
    4.9f, 5.5f, 9f, 10f, 6.7f, 8.2f,
    7.5f, 5f, 8.3f, 5.1f, 9f, 7f
};

float suma = 0;

for (int i = 0; i < arrayNotas.length; i++) {

    suma = suma + arrayNotas[i];

}

float media = suma / arrayNotas.length;

System.out.println("La nota media es: " + media);
```

En este ejemplo:

- `suma` es un acumulador que guarda la suma de las notas.
- El bucle `for` recorre todas las posiciones.
- `arrayNotas[i]` permite consultar cada nota.
- `arrayNotas.length` indica cuántas notas tenemos.
- Finalmente dividimos la suma entre el número de notas.

**Modificación propuesta por el profesor:**

En lugar de utilizar un array con notas inicializadas previamente, debemos pedir las notas al usuario y almacenarlas en el array antes de calcular la media.

### 4.3. Búsqueda

La **búsqueda** consiste en localizar un valor concreto dentro de un array.

Para realizarla debemos recorrer las posiciones hasta encontrar el elemento que estamos buscando.

El funcionamiento general es:

1. Comenzamos a recorrer el array.
2. Comparamos cada elemento con el valor que queremos encontrar.
3. Cuando encontramos el valor, detenemos el recorrido.
4. Si llegamos al final del array sin encontrarlo, significa que el elemento no existe.

Podemos utilizar una variable booleana para indicar si hemos encontrado el valor.

**Ejemplo 03: buscar una nota de 10**

El profesor propone trabajar con los siguientes arrays de notas:

```java
float[] arrayNotas = {
    2f, 5.5f, 9f, 10f, 4.9f, 8f,
    8.5f, 7f, 6.6f, 5f, 9f, 7f
};
```

El objetivo es comprobar si algún alumno ha obtenido un 10 y mostrar un mensaje indicando si se ha encontrado alguna nota con ese valor.

```java
float[] arrayNotas = {
    2f, 5.5f, 9f, 10f, 4.9f, 8f,
    8.5f, 7f, 6.6f, 5f, 9f, 7f
};

boolean encontrado = false;

for (int i = 0; i < arrayNotas.length && !encontrado; i++) {

    if (arrayNotas[i] == 10f) {

        encontrado = true;

    }

}

if (encontrado) {

    System.out.println("Se ha encontrado una nota de 10");

} else {

    System.out.println("No se ha encontrado ninguna nota de 10");

}
```

En este ejemplo:

- Inicializamos la variable `encontrado` con el valor `false`.
- Recorremos el array mientras no hayamos encontrado el valor.
- Comparamos cada nota con 10.
- Si encontramos una nota igual a 10, cambiamos `encontrado` a `true`.
- Al terminar, mostramos el mensaje correspondiente.

**Modificaciones propuestas por el profesor:**

Comprobar también si algún alumno ha suspendido.

Para probar diferentes situaciones se proponen otros arrays:

```java
float[] arrayNotas = {
    2f, 5.5f, 9f, 8f, 7f, 8f,
    8.5f, 7f, 6.6f, 5f, 9f, 7f
};
```

```java
float[] arrayNotas = {
    6f, 5.5f, 9f, 8f, 7f, 8f,
    10f, 7f, 6.6f, 5f, 9f, 7f
};
```

**Ejemplo 04: buscar un carácter**

En este ejercicio debemos crear un array de 10 caracteres:

```java
char[] arrayCaracteres = {
    'a', '0', 'g', ';', 'w',
    'o', 'h', '+', 'x', 's'
};
```

El programa debe solicitar al usuario un carácter que quiera buscar dentro del array.

También debe comprobar que el usuario introduce exactamente un carácter.

Si introduce más de uno o deja la entrada vacía, deberá volver a solicitarlo.

Una vez obtenido el carácter correcto, el programa recorrerá el array y mostrará:

- Si el carácter se ha encontrado.
- La posición en la que se encuentra.

**Modificación propuesta por el profesor:**

Permitir que el usuario introduzca un carácter hasta que sea válido y mostrar todas las posiciones en las que aparece si está repetido.

### 4.4. Arrays auxiliares

Podemos utilizar arrays auxiliares para almacenar diferentes valores relacionados con los datos de otro array.

De esta manera podemos guardar muchos valores diferentes utilizando un único identificador para cada conjunto de datos.

**Ejemplo 05: contar alumnos según sus notas**

Partimos del siguiente array:

```java
float[] arrayNotas = {
    4.9f, 5.5f, 9f, 10f, 6.7f, 8.2f,
    7.5f, 5f, 8.3f, 5.1f, 9f, 7f
};
```

El ejercicio consiste en crear un gráfico que muestre cuántos alumnos hay en cada categoría:

- Suspenso.
- Aprobado.
- Bien.
- Notable.
- Excelente.

Para resolverlo utilizaremos un array auxiliar que almacenará los contadores de cada categoría.

Por ejemplo:

```java
int[] contadores = new int[5];
```

Cada posición del array auxiliar representará una categoría:

| Posición | Categoría |
|---:|---|
| 0 | Suspenso |
| 1 | Aprobado |
| 2 | Bien |
| 3 | Notable |
| 4 | Excelente |

Después recorreremos el array de notas y aumentaremos el contador correspondiente según la nota de cada alumno.

**Modificación propuesta por el profesor:**

Crear un array de 100 elementos e introducir valores de notas aleatoriamente para realizar el mismo ejercicio.

### 4.5. Copia de arrays

En Java podemos asignar una variable de tipo array a otra variable del mismo tipo.

Sin embargo, debemos tener cuidado porque esta operación no crea una copia independiente de los datos.

**Asignación de un array a otro**

Observa el siguiente ejemplo:

```java
int[] arrayA = {10, 20, 30, 40, 50};

System.out.println("Array A: " + arrayA);

int[] arrayB = {60, 70, 80, 90, 100};

System.out.println("Array B: " + arrayB);

// Asignamos arrayB a arrayA
arrayA = arrayB;

System.out.println("Array A: " + arrayA);
System.out.println("Array B: " + arrayB);
```

Cuando hacemos:

```java
arrayA = arrayB;
```

No estamos copiando los elementos de `arrayB` dentro de `arrayA`.

Lo que sucede es que las dos variables pasan a hacer referencia al mismo array en memoria.

Por tanto, si modificamos un elemento utilizando cualquiera de las dos variables, el cambio se verá reflejado en ambas.

```java
arrayA[1] = 200;

System.out.println(arrayB[1]);
```

Resultado:

```text
200
```

Además, el array original al que hacía referencia `arrayA` deja de estar accesible mediante esa variable.

Java podrá liberar posteriormente esa memoria mediante el recolector de basura (*Garbage Collector*), si ya no existen otras referencias a ese array.

**Crear una copia independiente**

Si queremos tener dos arrays diferentes con los mismos valores, debemos copiar sus elementos individualmente.

**Ejemplo 06: copiar un array de números enteros**

Partimos del siguiente array:

```java
int[] enters = {45, 3, 74, -34, 12, 20, 66, 43, -101};
```

El ejercicio consiste en crear otro array llamado `copiaEnters` que tenga exactamente el mismo contenido, pero que sea independiente del original.

Podemos hacerlo utilizando un bucle `for`:

```java
int[] enters = {45, 3, 74, -34, 12, 20, 66, 43, -101};

int[] copiaEnters = new int[enters.length];

for (int i = 0; i < enters.length; i++) {

    copiaEnters[i] = enters[i];

}
```

En este caso:

1. Creamos un nuevo array con el mismo tamaño que el original.
2. Recorremos todas las posiciones del array original.
3. Copiamos cada elemento en la misma posición del nuevo array.

Ahora tenemos dos arrays independientes.

Si modificamos un elemento de uno de ellos, el otro no cambiará.

### 4.6. Cambio de tamaño de un array

Una vez creado un array, su tamaño no puede modificarse directamente.

Sin embargo, en algunas situaciones podemos necesitar más espacio para almacenar nuevos datos.

Para solucionar este problema podemos crear otro array de mayor tamaño y copiar los elementos del array original.

El procedimiento es el siguiente:

1. Crear un nuevo array con un tamaño superior al original.
2. Copiar los datos del array original manteniendo el mismo orden.
3. Asignar el nuevo array a la variable que utilizábamos anteriormente.
4. Añadir los nuevos valores en las posiciones disponibles.

**Ejemplo: ampliar el tamaño de un array**

Supongamos que tenemos un array de notas y queremos reservar espacio para 10 valores adicionales.

```java
int MAX_VALORES = 10;

float[] arrayNotas = {5.5f, 7f, 8.5f, 6f};

// PASO 1: crear un array nuevo de mayor tamaño

float[] arrayNuevo = new float[arrayNotas.length + MAX_VALORES];

// PASO 2: copiar los datos del array original

for (int i = 0; i < arrayNotas.length; i++) {

    arrayNuevo[i] = arrayNotas[i];

}

// Las posiciones adicionales tienen el valor 0.0

// PASO 3: asignar el nuevo array a la variable original

arrayNotas = arrayNuevo;

// PASO 4: ahora podemos añadir nuevos valores

arrayNotas[4] = 9f;
arrayNotas[5] = 7.5f;
```

En este ejemplo:

- El array original tenía cuatro posiciones.
- Creamos otro array con catorce posiciones.
- Copiamos los cuatro valores originales.
- Las diez posiciones adicionales quedan disponibles.
- Asignamos el nuevo array a `arrayNotas`.

Debemos tener en cuenta que cambiar el tamaño de un array de esta manera supone crear otro array y copiar todos sus elementos.

Esta operación puede afectar al rendimiento del programa.

Por eso, es recomendable elegir un tamaño inicial adecuado y evitar tener que ampliar el array constantemente.

### 4.7. Ordenación de arrays

La **ordenación** consiste en reorganizar los elementos de un array siguiendo un orden determinado.

Podemos ordenar los valores de forma:

- Ascendente: de menor a mayor.
- Descendente: de mayor a menor.

La ordenación puede resultar útil para mostrar los datos de forma organizada y facilitar determinadas operaciones de búsqueda.

Existen diferentes algoritmos de ordenación:

- QuickSort.
- BucketSort.
- SelectionSort (selección).
- BubbleSort (burbuja).

En los apuntes del profesor se estudian especialmente los algoritmos de selección y burbuja.

**Algoritmo de selección (SelectionSort)**

Este algoritmo utiliza dos bucles `for` para recorrer el array.

En cada iteración:

1. Se mantiene una posición fija, identificada mediante el índice `i`.
2. Se comparan los valores de las siguientes posiciones utilizando el índice `j`.
3. Se localiza el índice del valor menor.
4. Al terminar la búsqueda, se intercambia el valor menor con el de la posición fija.

De esta manera, el menor valor se coloca en la posición más baja disponible.

Ejemplo:

```java
int[] numeros = {45, 12, 30, 5, 20};

for (int i = 0; i < numeros.length - 1; i++) {

    int indiceMenor = i;

    for (int j = i + 1; j < numeros.length; j++) {

        if (numeros[j] < numeros[indiceMenor]) {

            indiceMenor = j;

        }
    }

    int auxiliar = numeros[i];

    numeros[i] = numeros[indiceMenor];

    numeros[indiceMenor] = auxiliar;
}
```

Al finalizar, el array estará ordenado de menor a mayor:

```text
[5, 12, 20, 30, 45]
```

**Algoritmo de la burbuja (BubbleSort)**

Este algoritmo ordena los elementos comparando parejas de valores que están uno al lado del otro.

Cuando encuentra dos valores que están en el orden incorrecto, intercambia sus posiciones.

El funcionamiento es el siguiente:

1. Se recorre todo el array comparando parejas de elementos consecutivos.
2. Si el primer valor es mayor que el segundo, se intercambian.
3. Al terminar el primer recorrido, el valor más alto queda en la última posición.
4. En el siguiente recorrido ya no es necesario comprobar esa última posición.
5. Se repite el proceso hasta ordenar todos los elementos.

Ejemplo:

```java
int[] numeros = {45, 12, 30, 5, 20};

for (int i = 0; i < numeros.length - 1; i++) {

    for (int j = 0; j < numeros.length - 1 - i; j++) {

        if (numeros[j] > numeros[j + 1]) {

            int auxiliar = numeros[j];

            numeros[j] = numeros[j + 1];

            numeros[j + 1] = auxiliar;

        }
    }
}
```

El resultado será:

```text
[5, 12, 20, 30, 45]
```

**Ejemplo 07: ordenar números enteros**

El profesor propone crear un programa que solicite al usuario 10 números enteros y los almacene en un array.

Después deberá mostrar:

- El array inicial.
- El array ordenado utilizando el algoritmo de selección.
- El array ordenado utilizando el algoritmo de la burbuja.

**Ejemplo 08: ordenar cadenas de texto**

En este ejercicio debemos solicitar al usuario cinco cadenas de texto e introducirlas en un array.

Después debemos:

1. Mostrar el array inicial.
2. Ordenar las cadenas alfabéticamente utilizando el algoritmo de la burbuja.
3. Mostrar el array resultante.

Para comparar dos cadenas de texto alfabéticamente podemos utilizar el método:

```java
cadena1.compareToIgnoreCase(cadena2)
```

Este método compara las cadenas sin distinguir entre mayúsculas y minúsculas.

El resultado de la comparación será:

- Un número negativo si la primera cadena precede alfabéticamente a la segunda.
- `0` si las cadenas son iguales.
- Un número positivo si la primera cadena aparece después de la segunda.

Ejemplo:

```java
String cadena1 = "Manzana";
String cadena2 = "Naranja";

int resultado = cadena1.compareToIgnoreCase(cadena2);

System.out.println(resultado);
```

En este caso, `Manzana` aparece antes que `Naranja` al ordenarlas alfabéticamente.

---

## Resumen del apartado

En este apartado hemos estudiado siete estrategias para trabajar con arrays:

| Estrategia | Utilidad |
|---|---|
| Iniciación procedural | Generar valores automáticamente siguiendo un patrón. |
| Recorrido | Procesar todos o parte de los elementos. |
| Búsqueda | Localizar un valor dentro del array. |
| Arrays auxiliares | Almacenar contadores y otros datos relacionados. |
| Copia | Crear otro array independiente con los mismos valores. |
| Cambio de tamaño | Crear un array mayor y copiar los datos originales. |
| Ordenación | Organizar los elementos de menor a mayor o alfabéticamente. |

Estas estrategias nos permiten resolver muchos problemas habituales utilizando arrays y estructuras de repetición.

---

[Volver al apartado anterior](#3-almacenamiento-de-la-entrada-de-datos-en-un-array)

[Siguiente apartado: Arrays multidimensionales](#5-arrays-multidimensionales)




## 5. Arrays multidimensionales

Hasta ahora hemos trabajado con arrays que almacenan sus elementos en una única dimensión.

Sin embargo, Java también permite crear arrays con varias dimensiones para organizar los datos de una forma más compleja.

El array bidimensional es el más habitual y permite organizar la información como si fuera una tabla o una hoja de cálculo.

### 5.1. Arrays bidimensionales

Un **array bidimensional** es una estructura que contiene filas y columnas.

Para acceder a un elemento necesitamos utilizar dos índices:

- Primer índice: indica la fila.
- Segundo índice: indica la columna.

Por ejemplo, podemos representar una matriz de tres filas y tres columnas:

| | Columna 0 | Columna 1 | Columna 2 |
|---|---:|---:|---:|
| Fila 0 | 1 | 2 | 3 |
| Fila 1 | 4 | 5 | 6 |
| Fila 2 | 7 | 8 | 9 |

Para acceder a cada elemento utilizamos la siguiente sintaxis:

```java
nombreArray[indiceFila][indiceColumna]
```

Por ejemplo:

```java
matriz[0][2] // Devuelve 3
matriz[1][1] // Devuelve 5
matriz[2][2] // Devuelve 9
```

### 5.2. Declaración e inicialización de arrays bidimensionales

Para declarar un array bidimensional utilizamos dos pares de corchetes `[][]`.

Existen diferentes formas de inicializarlo.

**Inicialización con valores por defecto**

Podemos crear una matriz indicando el número de filas y columnas.

Sintaxis:

```java
tipoDato[][] nombreArray = new tipoDato[filas][columnas];
```

Ejemplo:

```java
int[][] matriz = new int[5][5];
```

En este caso hemos creado una matriz de cinco filas y cinco columnas.

Como utilizamos el tipo `int`, todas las posiciones se inicializan automáticamente con el valor 0.

**Inicialización con valores concretos**

También podemos inicializar una matriz indicando directamente los valores de cada fila.

Cada fila se representa mediante otro array unidimensional y las diferentes filas se separan mediante comas.

Ejemplo:

```java
int[][] matriz = {
    {1, 2, 3, 4, 5},
    {6, 7, 8, 9, 10},
    {11, 12, 13, 14, 15}
};
```

En este caso tenemos una matriz de tres filas y cinco columnas.

Se trata de una matriz rectangular porque todas sus filas tienen la misma longitud.

**Arrays bidimensionales con filas de diferentes tamaños**

Java también permite crear arrays bidimensionales cuyas filas tengan diferentes cantidades de elementos.

Por ejemplo:

```java
int[][] arrayBidimensional = {
    {1},
    {1, 2, 3},
    {1, 2},
    {1, 2, 3, 4, 5, 6}
};
```

En este caso ya no tenemos una matriz rectangular, porque cada fila tiene una longitud diferente.

### 5.3. Mostrar el contenido de una matriz

Para mostrar todos los elementos de un array bidimensional necesitamos utilizar dos bucles `for` anidados.

El primer bucle recorre las filas y el segundo recorre las columnas de cada fila.

Ejemplo:

```java
int[][] matriz = {
    {1, 2, 3, 4, 5},
    {6, 7, 8, 9, 10},
    {11, 12, 13, 14, 15}
};

for (int i = 0; i < matriz.length; i++) {

    for (int j = 0; j < matriz[i].length; j++) {

        System.out.print(matriz[i][j] + "\t");

    }

    System.out.println("");
}
```

El resultado será:

```text
1    2    3    4    5
6    7    8    9    10
11   12   13   14   15
```

En este ejemplo:

- `matriz.length` indica el número de filas.
- `matriz[i].length` indica el número de columnas de la fila actual.
- `matriz[i][j]` permite acceder al elemento correspondiente a una fila y una columna.
- `System.out.print()` muestra los valores en la misma línea.
- `System.out.println()` permite pasar a la siguiente fila.

### 5.4. Acceder a las posiciones de una matriz

Para acceder a un elemento concreto de una matriz necesitamos indicar sus dos índices.

La sintaxis es:

```java
nombreArray[fila][columna]
```

Por ejemplo:

```java
int[][] matriz = {
    {1, 2, 3, 4, 5},
    {6, 7, 8, 9, 10},
    {11, 12, 13, 14, 15},
    {16, 17, 18, 19, 20}
};
```

Podemos consultar diferentes posiciones:

```java
System.out.println(matriz[0][2]);
System.out.println(matriz[1][1]);
System.out.println(matriz[2][2]);
```

Resultado:

```text
3
7
13
```

También podemos modificar directamente el valor de una posición:

```java
matriz[0][2] = 100;
```

De esta manera sustituimos el valor que había en la primera fila y tercera columna por 100.

### 5.5. Recorrer arrays bidimensionales

Para trabajar con matrices necesitamos utilizar dos estructuras de repetición anidadas:

- Un bucle para recorrer cada fila.
- Otro bucle para recorrer los elementos de cada fila.

La estructura general es:

```java
// Matriz de m filas y n columnas

int[][] a = new int[m][n];

for (int i = 0; i < a.length; i++) {

    for (int j = 0; j < a[i].length; j++) {

        // Procesamiento de la matriz

    }
}
```

Este esquema permite recorrer todos los elementos de la matriz siguiendo el orden de sus filas y columnas.

### 5.6. Iniciación procedural de matrices

Al igual que ocurre con los arrays unidimensionales, podemos inicializar una matriz mediante instrucciones y bucles.

**Ejemplo 09: inicializar una matriz con el valor 1**

El ejercicio consiste en crear una matriz de números enteros de cinco filas y diez columnas, asignando el valor 1 a todas sus posiciones.

Después debemos mostrar su contenido.

```java
int[][] matriz = new int[5][10];

for (int i = 0; i < matriz.length; i++) {

    for (int j = 0; j < matriz[i].length; j++) {

        matriz[i][j] = 1;

    }
}

// Mostrar la matriz

for (int i = 0; i < matriz.length; i++) {

    for (int j = 0; j < matriz[i].length; j++) {

        System.out.print(matriz[i][j] + "\t");

    }

    System.out.println("");
}
```

**Modificación propuesta por el profesor:**

- Pedir al usuario las dimensiones de la matriz (filas y columnas).
- Establecer un tamaño máximo de 20 filas y 20 columnas.
- Inicializar todos los elementos con números enteros aleatorios entre 0 y 10.

### 5.7. Recorrido de matrices

Podemos utilizar los arrays bidimensionales para almacenar información organizada por filas.

**Ejemplo 10: calcular la media de las notas de cada alumno**

En este ejercicio cada fila de la matriz representa las notas de un alumno.

La última posición de cada fila está inicialmente a 0 y debemos utilizarla para almacenar la media de las notas de ese alumno.

Partimos de la siguiente matriz:

```java
float[][] matrizNotas = {
    {4.5f, 6f, 5f, 8f, 0f},
    {10f, 8f, 7.5f, 9.5f, 0f},
    {3f, 2.5f, 4.5f, 6f, 0f},
    {6f, 8.5f, 6f, 4f, 0f},
    {9f, 7.5f, 7f, 8f, 0f}
};
```

Para resolverlo debemos recorrer cada fila, sumar las cuatro primeras notas y dividir el resultado entre cuatro.

La media se guardará en la última posición de cada fila.

```java
for (int i = 0; i < matrizNotas.length; i++) {

    float suma = 0;

    for (int j = 0; j < matrizNotas[i].length - 1; j++) {

        suma = suma + matrizNotas[i][j];

    }

    float media = suma / (matrizNotas[i].length - 1);

    matrizNotas[i][matrizNotas[i].length - 1] = media;

}
```

**Modificación propuesta por el profesor:**

Mostrar al final la nota media global de todos los estudiantes.

### 5.8. Búsqueda en matrices

También podemos buscar un valor concreto dentro de una matriz bidimensional.

Para realizar esta operación debemos recorrer las diferentes filas y columnas y comprobar si alguno de los elementos coincide con el valor que buscamos.

En este caso podemos utilizar variables booleanas, también llamadas semáforos, para indicar si hemos encontrado el elemento.

**Ejemplo 11: buscar una nota igual a 0**

En este ejercicio cada fila representa las notas de un alumno.

Debemos mostrar un mensaje si algún alumno ha obtenido un 0 en alguna actividad.

La matriz inicial es:

```java
float[][] matrizNotas = {
    {4.5f, 6f, 5f, 8f},
    {10f, 8f, 7.5f, 9.5f},
    {3f, 2.5f, 0f, 6f},
    {6f, 8.5f, 6f, 4f},
    {9f, 7.5f, 7f, 8f}
};
```

Para realizar la búsqueda utilizaremos dos bucles `while` y una variable booleana.

```java
boolean encontrado = false;

int i = 0;

while (i < matrizNotas.length && !encontrado) {

    int j = 0;

    while (j < matrizNotas[i].length && !encontrado) {

        if (matrizNotas[i][j] == 0f) {

            encontrado = true;

        }

        j++;

    }

    i++;

}

if (encontrado) {

    System.out.println("Se ha encontrado un alumno con un 0");

} else {

    System.out.println("No se ha encontrado ningún 0");

}
```

En este ejemplo:

- `encontrado` indica si hemos localizado el valor buscado.
- El primer `while` recorre las filas.
- El segundo `while` recorre las columnas de cada fila.
- Cuando encontramos un 0, cambiamos el valor de `encontrado` a `true`.
- Los bucles terminan cuando encontramos el valor o llegamos al final de la matriz.

**Modificación propuesta por el profesor:**

Cambiar la matriz inicial por otra que no contenga ningún 0 y comprobar que el programa muestra el mensaje correspondiente.

### 5.9. Arrays de más de dos dimensiones

Java también permite crear arrays con más de dos dimensiones.

En estos casos necesitamos utilizar más de dos índices para acceder a una posición concreta.

Un array de tres dimensiones se puede imaginar como una estructura tridimensional en forma de cubo.

Cuando utilizamos dimensiones superiores, la representación visual resulta más complicada y necesitamos un mayor nivel de abstracción.

Cada índice permite seleccionar una posición dentro de una dimensión determinada.

El conjunto de índices identifica el elemento concreto al que queremos acceder.

**Ejemplo: declarar un array de cuatro dimensiones**

Podemos crear un array de cuatro dimensiones utilizando la siguiente sintaxis:

```java
int[][][][] arrayCuatroDimensiones =
    new int[5][10][4][20];
```

En este caso tenemos:

- Primera dimensión: tamaño 5.
- Segunda dimensión: tamaño 10.
- Tercera dimensión: tamaño 4.
- Cuarta dimensión: tamaño 20.

Para acceder a un elemento necesitamos indicar los cuatro índices.

Por ejemplo:

```java
int valor = arrayCuatroDimensiones[2][0][1][19];
```

También podemos modificar una posición:

```java
arrayCuatroDimensiones[2][0][1][19] = 25;
```

### 5.10. Ejemplo práctico: almacenar temperaturas

**Ejemplo 12: temperaturas durante todo el año**

El último ejercicio del profesor consiste en crear un programa que genere un array multidimensional para almacenar las temperaturas de cada una de las 24 horas de los 30 días de los 12 meses del año.

El programa debe cumplir los siguientes requisitos:

- Crear una estructura multidimensional para almacenar las temperaturas.
- Generar las temperaturas de forma aleatoria entre una temperatura mínima y una máxima.
- Mostrar los datos por pantalla indicando el mes.
- Mostrar las temperaturas de cada día utilizando solamente dos dígitos.
- Al terminar de mostrar cada mes, esperar a que el usuario pulse una tecla para continuar.

**Modificación propuesta por el profesor:**

Adaptar la estructura para que cada mes almacene los días que realmente tiene:

| Mes | Número de días |
|---|---:|
| Enero | 31 |
| Febrero | 28 |
| Marzo | 31 |
| Abril | 30 |
| Mayo | 31 |
| Junio | 30 |
| Julio | 31 |
| Agosto | 31 |
| Septiembre | 30 |
| Octubre | 31 |
| Noviembre | 30 |
| Diciembre | 31 |

---

## Resumen del apartado

Los arrays multidimensionales permiten organizar información utilizando varias dimensiones.

En este apartado hemos aprendido:

- Declarar e inicializar matrices.
- Trabajar con filas y columnas.
- Acceder a posiciones utilizando dos índices.
- Recorrer matrices mediante bucles anidados.
- Inicializar matrices de forma procedural.
- Calcular medias recorriendo filas.
- Buscar valores dentro de matrices.
- Crear arrays de más de dos dimensiones.
- Aplicar arrays multidimensionales a un ejemplo de temperaturas.

---

[Volver al apartado anterior](#4-esquemas-fundamentales-en-la-utilizacion-de-arrays)
