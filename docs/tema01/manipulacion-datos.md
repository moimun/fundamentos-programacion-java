
# Manipulación básica de datos

Los programas informáticos trabajan con diferentes tipos de datos para realizar operaciones y obtener resultados.

En Java podemos utilizar números, caracteres, valores lógicos y cadenas de texto. Para trabajar con estos datos necesitamos conocer sus tipos, cómo se almacenan en memoria y qué operaciones podemos realizar con ellos.

En este apartado veremos cómo declarar variables y constantes, realizar operaciones, convertir datos y mostrar o introducir información mediante el teclado.

---

## 2.1. Tipos de datos

Un **tipo de dato** permite indicar qué clase de información estamos utilizando y qué operaciones podemos realizar con ella.

Los tipos de datos primitivos ya están incorporados en el lenguaje de programación y sirven como base para construir otros tipos de datos más complejos.

En Java encontramos diferentes tipos de datos:

### Números enteros

Los números enteros representan valores numéricos sin parte decimal. Pueden ser positivos, negativos o cero.

En Java podemos utilizar los siguientes tipos:

| Tipo | Tamaño |
|---|---:|
| `byte` | 8 bits |
| `short` | 16 bits |
| `int` | 32 bits |
| `long` | 64 bits |

Ejemplo:

```java
int edad = 25;
int temperatura = -5;
int cantidad = 100;
```

### Números reales

Los números reales permiten representar valores que tienen parte decimal.

En Java se utilizan principalmente:

| Tipo | Tamaño |
|---|---:|
| `float` | 32 bits |
| `double` | 64 bits |

Ejemplo:

```java
float precio = 19.99f;
double distancia = 125.75;
double temperatura = -4.5;
```

En los literales de tipo `float` se utiliza la letra `f` al final del número.

### Caracteres

El tipo `char` permite almacenar un único carácter.

Los caracteres se escriben entre comillas simples.

Ejemplo:

```java
char letra = 'A';
char numero = '7';
char simbolo = '#';
```

### Valores booleanos

El tipo `boolean` permite representar dos valores lógicos:

- `true`: verdadero.
- `false`: falso.

Se utiliza para comprobar condiciones y representar situaciones que solamente pueden tener dos estados.

Ejemplo:

```java
boolean activo = true;
boolean encontrado = false;
```

### Cadenas de texto

El tipo `String` permite almacenar secuencias de caracteres, es decir, textos de diferentes longitudes.

A diferencia de los tipos anteriores, `String` no es un tipo primitivo de Java.

Las cadenas de texto se escriben entre comillas dobles.

Ejemplo:

```java
String nombre = "Carlos";
String mensaje = "Hola mundo";
```

### Literales

Un **literal** es un valor fijo que escribimos directamente dentro del código fuente de un programa.

Por ejemplo:

```java
int edad = 20;
double precio = 15.50;
char letra = 'A';
boolean activo = true;
String nombre = "Carlos";
```

En estos ejemplos, `20`, `15.50`, `'A'`, `true` y `"Carlos"` son valores literales.

---

## 2.2. Transformación de los datos

Dentro de un programa podemos realizar operaciones sobre los datos para obtener nuevos valores.

Cada tipo de dato establece qué operaciones se pueden realizar con él.

Las operaciones se pueden dividir en dos grupos:

- **Unarias:** trabajan con un único operando.
- **Binarias:** necesitan dos operandos.

### Operadores aritméticos

Los operadores aritméticos permiten realizar operaciones matemáticas.

| Operador | Operación | Ejemplo |
|---|---|---|
| `+` | Suma | `5 + 3` |
| `-` | Resta | `5 - 3` |
| `*` | Multiplicación | `5 * 3` |
| `/` | División | `10 / 2` |
| `%` | Módulo (resto) | `10 % 3` |

Ejemplo en Java:

```java
int numero1 = 10;
int numero2 = 3;

int suma = numero1 + numero2;
int resta = numero1 - numero2;
int multiplicacion = numero1 * numero2;
int division = numero1 / numero2;
int resto = numero1 % numero2;
```

El operador `%` permite obtener el resto de una división.

### Operadores lógicos

Los operadores lógicos permiten trabajar con valores booleanos y combinar condiciones.

| Operador | Nombre | Funcionamiento |
|---|---|---|
| `&&` | AND | Verdadero si las dos condiciones son verdaderas. |
| `||` | OR | Verdadero si al menos una condición es verdadera. |
| `!` | NOT | Invierte el valor lógico. |

Ejemplo:

```java
boolean condicion1 = true;
boolean condicion2 = false;

System.out.println(condicion1 && condicion2);
System.out.println(condicion1 || condicion2);
System.out.println(!condicion1);
```

### Operadores relacionales

Permiten comparar dos valores y obtener un resultado booleano.

| Operador | Significado |
|---|---|
| `==` | Igual que |
| `!=` | Diferente de |
| `>` | Mayor que |
| `<` | Menor que |
| `>=` | Mayor o igual que |
| `<=` | Menor o igual que |

Ejemplo:

```java
int edad = 20;

System.out.println(edad >= 18);
System.out.println(edad == 20);
System.out.println(edad < 18);
```

### Operadores de cadenas de texto

En Java podemos utilizar el operador `+` para concatenar cadenas de texto.

La concatenación consiste en unir diferentes cadenas de texto para formar una nueva.

Ejemplo:

```java
String saludo = "Hola";
String nombre = "Carlos";

System.out.println(saludo + " " + nombre);
```

Resultado:

```text
Hola Carlos
```

También podemos concatenar cadenas de texto con otros tipos de datos:

```java
int edad = 25;

System.out.println("La edad es " + edad);
```

Resultado:

```text
La edad es 25
```

---

## 2.3. Gestión de datos en la memoria

Cuando ejecutamos un programa, necesitamos almacenar los datos para poder utilizarlos posteriormente.

Para ello utilizamos variables y constantes.

### Variables

Una **variable** es un espacio de memoria identificado mediante un nombre, donde podemos almacenar un valor.

El valor de una variable puede cambiar durante la ejecución del programa.

Antes de utilizar una variable debemos declararla indicando su tipo de dato y su identificador.

La sintaxis es:

```java
tipo identificador = valorInicial;
```

Ejemplo:

```java
int edad = 25;
double precio = 19.99;
String nombre = "Carlos";
boolean activo = true;
```

En estos ejemplos:

- `int`, `double`, `String` y `boolean` son los tipos de datos.
- `edad`, `precio`, `nombre` y `activo` son los identificadores.
- Los valores situados después del signo `=` son los valores iniciales.

### Identificadores

Un identificador es el nombre que utilizamos para reconocer una variable, constante u otro elemento del programa.

Para elegir identificadores debemos respetar las reglas del lenguaje Java.

Algunas recomendaciones son:

- Utilizar nombres que indiquen qué información almacenan.
- No utilizar espacios en blanco.
- No comenzar el nombre con un número.
- No utilizar palabras reservadas del lenguaje.
- Diferenciar entre mayúsculas y minúsculas.

Ejemplos:

```java
int edad;
double precioProducto;
String nombreAlumno;
```

### Palabras reservadas

Las palabras reservadas son palabras que tienen un significado especial dentro del lenguaje Java.

Por ejemplo:

- `int`
- `double`
- `boolean`
- `if`
- `else`
- `for`
- `while`
- `class`
- `public`
- `static`
- `return`

No podemos utilizarlas como identificadores de nuestras variables.

### Declaración e inicialización

Declarar una variable significa indicar su tipo de dato y su nombre.

Inicializarla significa asignarle un valor inicial.

Podemos hacer ambas operaciones al mismo tiempo:

```java
int numero = 10;
```

También podemos declarar primero la variable y asignarle un valor después:

```java
int numero;
numero = 10;
```

### Asignación de valores

El operador `=` permite asignar un valor a una variable.

Ejemplo:

```java
int numero = 10;

numero = 20;

System.out.println(numero);
```

Resultado:

```text
20
```

Cuando asignamos un nuevo valor, el anterior queda sustituido.

### Constantes

Una **constante** es un valor que se establece una vez y no puede modificarse posteriormente.

En Java se utiliza la palabra reservada `final` para declarar una constante.

Ejemplo:

```java
final double PI = 3.14159;
final int EDAD_MINIMA = 18;
```

Por convenio, los nombres de las constantes suelen escribirse en mayúsculas.

Las constantes son útiles cuando un mismo valor aparece varias veces en el programa y no queremos que cambie.

---

## 2.4. Conversiones de tipos

En ocasiones necesitamos transformar un valor de un tipo de dato a otro diferente.

Este proceso se conoce como **conversión de tipos** o *casting*.

Por ejemplo, podemos necesitar convertir un número entero en un número real o transformar un número real en un entero.

### Conversión implícita

Se produce cuando Java realiza automáticamente una conversión entre determinados tipos compatibles.

Por ejemplo, podemos asignar un valor entero a una variable de tipo `double`:

```java
int numero = 10;

double resultado = numero;

System.out.println(resultado);
```

Resultado:

```text
10.0
```

En este caso Java convierte automáticamente el entero en un número real.

### Conversión explícita (casting)

Se utiliza cuando queremos indicar directamente el tipo de dato al que queremos convertir un valor.

Para ello escribimos el tipo de destino entre paréntesis delante del valor.

Ejemplo:

```java
double numeroReal = 15.75;

int numeroEntero = (int) numeroReal;

System.out.println(numeroEntero);
```

Resultado:

```text
15
```

Al convertir un número real en un entero se pierden los decimales. No se realiza un redondeo, sino que se eliminan.

### Pérdida de información

Al realizar conversiones debemos tener cuidado, porque algunos valores pueden perder información.

Por ejemplo:

- Al convertir un número real en entero se eliminan los decimales.
- Al asignar un valor que supera el rango del tipo de destino se puede producir un desbordamiento.

Por eso debemos comprobar que el valor que queremos convertir puede representarse correctamente con el nuevo tipo de dato.

---

## 2.5. Visualización y entrada de datos

Los programas necesitan mostrar información al usuario y, en muchas ocasiones, recoger datos que este introduce mediante el teclado.

En Java podemos realizar estas operaciones utilizando diferentes instrucciones.

### Salida de datos por pantalla

Para mostrar información por pantalla utilizamos principalmente:

- `System.out.print()`: muestra información sin añadir un salto de línea al final.
- `System.out.println()`: muestra información y añade un salto de línea al final.

Ejemplo:

```java
System.out.print("Hola ");
System.out.print("mundo");
```

Resultado:

```text
Hola mundo
```

Si utilizamos `println()`:

```java
System.out.println("Hola");
System.out.println("mundo");
```

Resultado:

```text
Hola
mundo
```

Estas instrucciones permiten mostrar valores de diferentes tipos de datos.

### Entrada de datos por teclado

Para recoger información introducida por el usuario podemos utilizar la clase `Scanner`, que pertenece al paquete `java.util`.

Primero debemos importarla:

```java
import java.util.Scanner;
```

Después creamos un objeto Scanner para leer los datos del teclado:

```java
Scanner entrada = new Scanner(System.in);
```

Según el tipo de dato que queramos leer, utilizaremos diferentes métodos:

| Método | Tipo de dato |
|---|---|
| `nextInt()` | Número entero |
| `nextDouble()` | Número real |
| `nextFloat()` | Número real de tipo float |
| `nextBoolean()` | Valor booleano |
| `nextLine()` | Cadena de texto |

### Ejemplo: introducir un nombre

```java
import java.util.Scanner;

public class ValorNom {

    public static void main(String[] args) {

        Scanner entrada = new Scanner(System.in);

        System.out.print("Escribe tu nombre: ");

        String nombre = entrada.nextLine();

        System.out.println("Tu nombre es: " + nombre);
    }
}
```

En este ejemplo:

1. Importamos la clase `Scanner`.
2. Creamos el objeto `entrada`.
3. Mostramos un mensaje solicitando el nombre.
4. Recogemos el texto mediante `nextLine()`.
5. Mostramos el nombre introducido.

### Ejemplo: sumar dos números enteros

```java
import java.util.Scanner;

public class SumarNumeros {

    public static void main(String[] args) {

        Scanner lector = new Scanner(System.in);

        System.out.print("Escribe un número: ");
        int primerNumero = lector.nextInt();

        lector.nextLine();

        System.out.print("Escribe otro número: ");
        int segundoNumero = lector.nextInt();

        lector.nextLine();

        int resultado = primerNumero + segundoNumero;

        System.out.println("El resultado de la suma es " + resultado + ".");
    }
}
```

Si introducimos los números 5 y 8, el resultado será:

```text
Escribe un número: 5
Escribe otro número: 8
El resultado de la suma es 13.
```

### Algunas consideraciones sobre la entrada de datos

Cuando utilizamos `Scanner`, debemos tener en cuenta que:

- El dato introducido debe coincidir con el tipo que espera el programa.
- Si esperamos un número entero y se introduce un texto, se puede producir un error.
- Para introducir números reales, el separador decimal puede depender de la configuración regional.
- El método `nextLine()` permite leer una línea completa de texto.
- Después de determinadas lecturas numéricas puede ser necesario utilizar `nextLine()` para consumir el salto de línea pendiente.

---

## Resumen del apartado

En este apartado hemos aprendido:

- Los principales tipos de datos utilizados en Java.
- Qué son los literales y los operadores.
- Cómo realizar operaciones aritméticas, lógicas y relacionales.
- Qué son las variables, los identificadores y las constantes.
- Cómo declarar, inicializar y modificar variables.
- Cómo realizar conversiones de tipos.
- Cómo mostrar información mediante `print()` y `println()`.
- Cómo recoger datos utilizando la clase `Scanner`.

---

[Volver al Tema 01](index.md)

[Volver a la página principal](../index.md)
