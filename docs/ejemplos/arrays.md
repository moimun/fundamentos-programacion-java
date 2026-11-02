
# Ejemplos de arrays en Java

En este apartado se muestran diferentes ejemplos de utilización de arrays en Java. Los arrays permiten almacenar varios valores del mismo tipo utilizando un único identificador.

---

## 1. Declaración e inicialización de un array

Para declarar un array indicamos el tipo de dato seguido de corchetes y el nombre de la variable.

**Ejemplo:**

```java
public class EjemploArray01 {

    public static void main(String[] args) {

        int[] numeros = {10, 20, 30, 40, 50};

        System.out.println(numeros[0]);
        System.out.println(numeros[2]);
        System.out.println(numeros[4]);
    }
}
```

**Resultado:**

```text
10
30
50
```

Los elementos de un array se identifican mediante índices, que comienzan en `0`.

---

## 2. Recorrer un array con `for`

Podemos utilizar un bucle `for` para recorrer todos los elementos de un array.

**Ejemplo:**

```java
public class EjemploArray02 {

    public static void main(String[] args) {

        int[] numeros = {10, 20, 30, 40, 50};

        for (int i = 0; i < numeros.length; i++) {
            System.out.println(numeros[i]);
        }
    }
}
```

**Resultado:**

```text
10
20
30
40
50
```

La propiedad `length` permite conocer el número de elementos que contiene el array.

---

## 3. Modificar elementos de un array

Podemos cambiar el valor de un elemento indicando su posición dentro del array.

**Ejemplo:**

```java
public class EjemploArray03 {

    public static void main(String[] args) {

        int[] numeros = {10, 20, 30, 40, 50};

        numeros[2] = 100;

        for (int i = 0; i < numeros.length; i++) {
            System.out.println(numeros[i]);
        }
    }
}
```

**Resultado:**

```text
10
20
100
40
50
```

En este ejemplo hemos cambiado el valor de la posición `2`, que inicialmente era `30`.

---

## 4. Buscar un elemento dentro de un array

Podemos recorrer un array para comprobar si contiene un determinado valor.

**Ejemplo:**

```java
public class EjemploArray04 {

    public static void main(String[] args) {

        int[] numeros = {4, 8, 12, 16, 20};

        int buscar = 12;
        boolean encontrado = false;

        for (int i = 0; i < numeros.length; i++) {

            if (numeros[i] == buscar) {
                encontrado = true;
                break;
            }
        }

        if (encontrado) {
            System.out.println("Número encontrado");
        } else {
            System.out.println("Número no encontrado");
        }
    }
}
```

**Resultado:**

```text
Número encontrado
```

Utilizamos una variable booleana para indicar si hemos encontrado el elemento.

---

## 5. Sumar los elementos de un array

Podemos utilizar una variable acumuladora para sumar todos los valores de un array.

**Ejemplo:**

```java
public class EjemploArray05 {

    public static void main(String[] args) {

        int[] numeros = {10, 20, 30, 40, 50};

        int suma = 0;

        for (int i = 0; i < numeros.length; i++) {
            suma = suma + numeros[i];
        }

        System.out.println("Suma total: " + suma);
    }
}
```

**Resultado:**

```text
Suma total: 150
```

La variable `suma` va acumulando el valor de cada elemento del array.

---

## 6. Arrays multidimensionales

Los arrays multidimensionales permiten almacenar información organizada en filas y columnas.

**Ejemplo:**

```java
public class EjemploArray06 {

    public static void main(String[] args) {

        int[][] numeros = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        for (int fila = 0; fila < numeros.length; fila++) {

            for (int columna = 0; columna < numeros[fila].length; columna++) {
                System.out.print(numeros[fila][columna] + " ");
            }

            System.out.println();
        }
    }
}
```

**Resultado:**

```text
1 2 3
4 5 6
7 8 9
```

En este ejemplo utilizamos dos bucles `for`: uno para recorrer las filas y otro para recorrer las columnas.

---

## Resumen

En estos ejemplos hemos aprendido a:

- Declarar e inicializar arrays.
- Acceder a sus elementos mediante índices.
- Recorrer arrays utilizando bucles.
- Modificar los valores almacenados.
- Buscar elementos.
- Sumar los valores de un array.
- Trabajar con arrays multidimensionales.
