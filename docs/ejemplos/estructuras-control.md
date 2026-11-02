
# Ejemplos de estructuras de control

En este apartado se muestran ejemplos de las estructuras de control de Java. Estas estructuras permiten controlar el orden en el que se ejecutan las instrucciones de un programa.

---

## 1. Estructura `if`

La estructura `if` permite ejecutar unas instrucciones solamente cuando se cumple una condición.

**Ejemplo:**

```java
public class EjemploIf {

    public static void main(String[] args) {

        int numero = 10;

        if (numero > 0) {
            System.out.println("El número es positivo");
        }
    }
}
```

**Resultado:**

```text
El número es positivo
```

---

## 2. Estructura `if / else`

La estructura `if / else` permite elegir entre dos posibilidades, dependiendo de si se cumple o no una condición.

**Ejemplo:**

```java
public class EjemploIfElse {

    public static void main(String[] args) {

        int edad = 17;

        if (edad >= 18) {
            System.out.println("Es mayor de edad");
        } else {
            System.out.println("Es menor de edad");
        }
    }
}
```

**Resultado:**

```text
Es menor de edad
```

---

## 3. Estructura `if / else if / else`

Se utiliza cuando necesitamos comprobar varias condiciones diferentes.

**Ejemplo:**

```java
public class EjemploIfElseIf {

    public static void main(String[] args) {

        int nota = 7;

        if (nota < 5) {
            System.out.println("Suspenso");
        } else if (nota < 7) {
            System.out.println("Aprobado");
        } else if (nota < 9) {
            System.out.println("Notable");
        } else {
            System.out.println("Excelente");
        }
    }
}
```

**Resultado:**

```text
Notable
```

---

## 4. Estructura `switch`

La estructura `switch` permite seleccionar qué instrucciones ejecutar dependiendo del valor de una variable.

**Ejemplo:**

```java
public class EjemploSwitch {

    public static void main(String[] args) {

        int dia = 2;

        switch (dia) {
            case 1:
                System.out.println("Lunes");
                break;
            case 2:
                System.out.println("Martes");
                break;
            case 3:
                System.out.println("Miércoles");
                break;
            default:
                System.out.println("Día no válido");
        }
    }
}
```

**Resultado:**

```text
Martes
```

La instrucción `break` permite salir del bloque `switch` cuando se ejecuta el caso correspondiente. `default` se ejecuta cuando ningún caso coincide.

---

## 5. Estructura `while`

El bucle `while` repite unas instrucciones mientras se cumpla una condición.

**Ejemplo:**

```java
public class EjemploWhile {

    public static void main(String[] args) {

        int contador = 1;

        while (contador <= 5) {
            System.out.println(contador);
            contador++;
        }
    }
}
```

**Resultado:**

```text
1
2
3
4
5
```

---

## 6. Estructura `do / while`

El bucle `do / while` ejecuta primero las instrucciones y después comprueba la condición. Por eso, el bloque se ejecuta al menos una vez.

**Ejemplo:**

```java
public class EjemploDoWhile {

    public static void main(String[] args) {

        int contador = 1;

        do {
            System.out.println(contador);
            contador++;
        } while (contador <= 5);
    }
}
```

**Resultado:**

```text
1
2
3
4
5
```

---

## 7. Estructura `for`

El bucle `for` permite repetir instrucciones un número determinado de veces.

**Ejemplo:**

```java
public class EjemploFor {

    public static void main(String[] args) {

        for (int contador = 1; contador <= 5; contador++) {
            System.out.println(contador);
        }
    }
}
```

**Resultado:**

```text
1
2
3
4
5
```

---

## Resumen

En estos ejemplos hemos visto cómo utilizar las principales estructuras de control de Java:

- `if`: ejecuta instrucciones si se cumple una condición.
- `if / else`: permite elegir entre dos posibilidades.
- `if / else if / else`: permite comprobar varias condiciones.
- `switch`: selecciona instrucciones según el valor de una variable.
- `while`: repite instrucciones mientras se cumpla una condición.
- `do / while`: ejecuta primero y comprueba después.
- `for`: permite repetir instrucciones un número determinado de veces.
