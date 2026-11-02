
# Fundamentos de Java

En este apartado se muestran ejemplos básicos de programación en Java para comprender cómo se utilizan las variables, los tipos de datos y los operadores.

---

## 1. Declaración de variables

Las variables permiten guardar información que podemos utilizar durante la ejecución de un programa.

Para declarar una variable indicamos primero el tipo de dato y después su nombre.

**Ejemplo:**

```java
int numero = 10;
double precio = 25.50;
boolean activo = true;
char letra = 'A';
String nombre = "Eme";
```

En este ejemplo se utilizan diferentes tipos de datos:

- `int`: guarda números enteros.
- `double`: guarda números decimales.
- `boolean`: guarda valores `true` o `false`.
- `char`: guarda un carácter.
- `String`: guarda una cadena de texto.

---

## 2. Mostrar información por pantalla

Para mostrar información por pantalla utilizamos `System.out.println()`.

**Ejemplo:**

```java
public class Ejemplo01 {

    public static void main(String[] args) {

        String nombre = "Eme";
        int edad = 20;

        System.out.println("Nombre: " + nombre);
        System.out.println("Edad: " + edad);
    }
}
```

**Resultado:**

```text
Nombre: Eme
Edad: 20
```

---

## 3. Operadores aritméticos

Los operadores aritméticos permiten realizar operaciones matemáticas.

**Ejemplo:**

```java
int numero1 = 10;
int numero2 = 5;

System.out.println(numero1 + numero2);
System.out.println(numero1 - numero2);
System.out.println(numero1 * numero2);
System.out.println(numero1 / numero2);
System.out.println(numero1 % numero2);
```

**Resultado:**

```text
15
5
50
2
0
```

Los operadores utilizados son:

- `+`: suma.
- `-`: resta.
- `*`: multiplicación.
- `/`: división.
- `%`: módulo o resto de una división.

---

## 4. Operadores lógicos

Los operadores lógicos permiten combinar o modificar condiciones.

Los principales operadores son:

- `&&`: AND (Y).
- `||`: OR (O).
- `!`: NOT (NO).
- `^`: XOR (O exclusivo).

**Ejemplo:**

```java
boolean condicion1 = true;
boolean condicion2 = false;

System.out.println(condicion1 && condicion2);
System.out.println(condicion1 || condicion2);
System.out.println(!condicion1);
System.out.println(condicion1 ^ condicion2);
```

**Resultado:**

```text
false
true
false
true
```

---

## 5. Conversión de tipos de datos

En Java podemos convertir un valor de un tipo de dato a otro mediante el *casting*.

**Ejemplo:**

```java
double precio = 15.75;

int precioEntero = (int) precio;

System.out.println(precioEntero);
```

**Resultado:**

```text
15
```

En este caso, el valor decimal se convierte en un número entero y se pierde la parte decimal.

---

## Resumen

En estos ejemplos hemos visto cómo:

- Declarar y utilizar variables.
- Trabajar con diferentes tipos de datos.
- Mostrar información por pantalla.
- Realizar operaciones aritméticas.
- Utilizar operadores lógicos.
- Convertir valores entre diferentes tipos de datos.
