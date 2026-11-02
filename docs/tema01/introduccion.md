
# Introducción a la programación

La programación consiste en crear instrucciones para que un ordenador pueda realizar diferentes tareas. Para ello se utilizan lenguajes de programación que permiten indicar qué debe hacer el ordenador y en qué orden.

En este apartado veremos qué es un programa informático, cómo funciona un ordenador cuando ejecuta instrucciones y qué pasos se siguen para crear un programa.

---

## 1.1. ¿Qué es un programa?

Un **programa informático** es un conjunto de órdenes, instrucciones o sentencias que se ejecutan de forma secuencial y que trabajan sobre un conjunto de datos.

Dependiendo del programa, los datos que se utilizan pueden ser diferentes:

- **Editor de texto:** trabaja con la información de un documento.
- **Hoja de cálculo:** trabaja principalmente con datos numéricos.
- **Videojuego:** utiliza datos relacionados con los jugadores, enemigos y sus posiciones.
- **Navegador web:** procesa las órdenes del usuario y los datos que recibe de los servidores de Internet.

### La tarea del programador

El trabajo del programador consiste en decidir:

- Qué instrucciones debe contener el programa.
- En qué orden se tienen que ejecutar.
- Sobre qué datos se deben aplicar.

Todo esto tiene como finalidad conseguir que el programa realice correctamente la tarea para la que ha sido creado.

Para programar es necesario conocer un **lenguaje de programación** y utilizar un **entorno de desarrollo (IDE)** que permita escribir, ejecutar y comprobar el código.

### Ejecución de un programa

Cuando ejecutamos un programa, el ordenador realiza las instrucciones que hemos escrito. El resultado dependerá de los datos que se le proporcionen.

Podemos distinguir tres elementos:

- **Programa:** es el código fuente escrito en un lenguaje de programación.
- **Proceso:** es el programa mientras se está ejecutando y se encuentra cargado en la memoria RAM.
- **Almacenamiento:** permite obtener los datos iniciales y guardar los resultados.

De forma sencilla, el funcionamiento de un programa se puede representar así:

1. Se introducen los datos.
2. El programa procesa la información.
3. Se obtiene un resultado.

---

## 1.2. Tipos de órdenes que acepta un ordenador

Un ordenador está formado por diferentes componentes que trabajan conjuntamente para ejecutar los programas y procesar la información.

Entre los componentes principales encontramos el procesador, la memoria y el sistema de entrada y salida.

### El procesador (CPU)

El procesador es uno de los componentes principales del ordenador. Se encarga de ejecutar las instrucciones y realizar las operaciones necesarias para manipular y transformar los datos.

Entre las operaciones que puede realizar encontramos:

- **Operaciones aritméticas:** sumas, restas, multiplicaciones y divisiones.
- **Operaciones lógicas:** AND, OR y NOT.
- **Transferencia de datos:** mover información entre un origen y un destino.
- **Entrada y salida:** intercambiar información con los dispositivos conectados.

### Sistema de entrada y salida (E/S)

El sistema de entrada y salida permite intercambiar información entre el ordenador y los dispositivos externos.

Algunos ejemplos de periféricos son:

- Teclado.
- Ratón.
- Pantalla.

Mediante estos dispositivos podemos introducir información y recibir los resultados que genera el ordenador.

---

## 1.3. Crear un programa ejecutable

Para crear un programa necesitamos escribir las instrucciones utilizando un lenguaje de programación.

Existen diferentes tipos de lenguajes y formas de ejecutar los programas.

### Lenguaje máquina

Es el lenguaje que entiende directamente el procesador. Sus instrucciones se representan mediante secuencias de ceros y unos (0 y 1).

No resulta práctico escribir programas directamente en este lenguaje, porque es difícil de interpretar para las personas.

### Lenguajes de programación de alto nivel

Son lenguajes que utilizan instrucciones más fáciles de entender para las personas.

Permiten escribir programas sin tener que trabajar directamente con las instrucciones específicas de cada procesador.

Una instrucción de Java, por ejemplo, puede ser:

```java
System.out.println("Hola mundo");
```

Esta instrucción permite mostrar un mensaje por pantalla.

### Lenguajes compilados

En los lenguajes compilados se utiliza un programa llamado **compilador**, que se encarga de traducir el código fuente a otro formato que pueda utilizarse para ejecutar el programa.

Algunos conceptos relacionados son:

- **Código fuente:** conjunto de instrucciones escritas por el programador.
- **Compilación:** proceso de traducción del código fuente.
- **Compilador:** programa que realiza esa traducción.
- **Código objeto:** resultado obtenido durante el proceso de compilación.

Si el compilador encuentra instrucciones que no respetan las reglas del lenguaje, se puede producir un error de compilación.

En ese caso hay que revisar el código y corregir los errores. Este proceso se conoce como **depuración (debug)**.

### Lenguajes interpretados

En los lenguajes interpretados se utiliza un programa llamado **intérprete**, que procesa el código fuente y gestiona su ejecución.

En este caso se trabaja directamente con el archivo que contiene el código fuente, sin generar previamente un archivo de código objeto como en el proceso de compilación descrito anteriormente.

### ¿Cómo funciona Java?

Java utiliza un proceso de compilación y ejecución propio.

Para trabajar con Java necesitamos el **JDK (Java Development Kit)**, que incluye el compilador `javac` y otras herramientas de desarrollo.

El proceso básico es el siguiente:

1. Escribimos el código fuente en un archivo `.java`.
2. Utilizamos el compilador `javac` para generar el bytecode.
3. Se obtiene un archivo `.class`.
4. La JVM (Java Virtual Machine) se encarga de ejecutar ese bytecode.

Por ejemplo, si tenemos un archivo llamado `HolaMon.java`, podemos utilizar estos comandos:

```powershell
javac HolaMon.java
java HolaMon
```

El primer comando compila el programa y genera `HolaMon.class`. El segundo ejecuta el programa mediante la máquina virtual de Java.

---

## 1.4. Hola Mundo

El programa **Hola Mundo** es uno de los primeros programas que se suelen realizar cuando se empieza a aprender un lenguaje de programación.

Su función es mostrar un mensaje por pantalla y comprobar que podemos escribir y ejecutar un programa correctamente.

### Código en Java

```java
public class HolaMon {

    public static void main(String[] args) {

        System.out.println("Hola mundo");

    }
}
```

### Explicación del código

- `public class HolaMon`: declara una clase llamada HolaMon.
- `public static void main(String[] args)`: es el método principal desde el que comienza la ejecución del programa.
- `System.out.println("Hola mundo");`: muestra el texto Hola mundo por pantalla.
- Las llaves `{ }` indican el comienzo y el final de los bloques de código.
- El punto y coma `;` indica el final de una instrucción.

### Resultado de la ejecución

Al ejecutar el programa, el resultado que aparece en la consola es:

```text
Hola mundo
```

Este pequeño ejemplo nos permite comprobar que el programa se ha escrito y ejecutado correctamente.

---

## Resumen del apartado

En este apartado hemos aprendido:

- Qué es un programa informático y para qué sirve.
- Cuál es el trabajo de un programador.
- Cómo se ejecutan los programas y cómo se procesan los datos.
- Qué componentes intervienen en el funcionamiento de un ordenador.
- Las diferencias entre lenguajes compilados e interpretados.
- Cómo se compila y ejecuta un programa Java.
- Cómo crear nuestro primer programa Hola Mundo.

---

[Volver al Tema 01](index.md)

[Siguiente apartado: Manipulación básica de datos](manipulacion-datos.md)
