
# Algoritmos

Antes de empezar a escribir un programa es necesario pensar qué queremos conseguir y cómo vamos a hacerlo.

Para desarrollar una aplicación informática se siguen diferentes fases que permiten organizar el trabajo, diseñar una solución, escribir el código y comprobar que funciona correctamente.

En este apartado conoceremos las cinco fases del desarrollo de una aplicación informática y veremos qué función tiene cada una.

---

## 1.1. Definición del problema

El primer paso para desarrollar un programa es tener claro qué problema queremos resolver.

Para ello es necesario conocer las necesidades de las personas que utilizarán el programa y establecer los objetivos que queremos conseguir.

Durante esta fase se realizan diferentes tareas:

- Hablar con los usuarios que utilizarán la aplicación.
- Conocer sus necesidades y los problemas que quieren resolver.
- Establecer claramente los objetivos del programa.
- Analizar los recursos necesarios para desarrollar la solución.
- Estudiar las diferentes soluciones posibles.

También se deben tener en cuenta los costes económicos, los recursos materiales y el personal necesario para realizar el proyecto.

Una vez analizadas las diferentes posibilidades, se propone la solución que mejor se adapta a las necesidades del cliente.

---

## 1.2. Diseño del algoritmo

Una vez definido el problema, el siguiente paso consiste en diseñar un **algoritmo** que permita encontrar una solución.

Un algoritmo es una descripción formada por una serie de pasos que se deben seguir de manera ordenada para conseguir un objetivo.

No es algo exclusivo de la informática, ya que podemos encontrar algoritmos en muchas actividades de nuestra vida cotidiana.

### ¿Por qué es necesario diseñar un algoritmo?

Antes de empezar a escribir el código fuente, el programador debe dedicar tiempo a pensar cómo resolverá el problema.

El diseño del algoritmo condiciona la forma que tendrá el programa.

Si el algoritmo está mal diseñado, podemos acabar escribiendo un programa que no realice correctamente la tarea que necesitamos.

### Programación estructurada

La programación estructurada consiste en organizar los pasos de un algoritmo mediante diferentes bloques de instrucciones.

Para ello se utilizan tres tipos de estructuras de control:

**Estructura lineal o secuencial**

Las instrucciones se ejecutan una detrás de otra, siguiendo el orden en el que aparecen.

**Estructura de selección o condicional**

Permite ejecutar diferentes bloques de instrucciones dependiendo de si se cumple o no una determinada condición.

**Estructura de repetición o iterativa**

Permite ejecutar un bloque de instrucciones varias veces, hasta alcanzar una condición o un número determinado de repeticiones.

Estas tres estructuras permiten controlar el orden en el que se ejecutan las instrucciones de un programa.

### Diagramas de flujo

Un diagrama de flujo permite representar gráficamente los pasos de un algoritmo y las diferentes decisiones que se pueden producir durante su ejecución.

Cada paso se representa mediante una figura geométrica específica.

Los diagramas de flujo permiten visualizar los diferentes caminos que puede seguir un programa.

Entre los símbolos más utilizados encontramos:

| Símbolo | Significado |
|---|---|
| Óvalo | Inicio o final del algoritmo. |
| Rectángulo | Proceso o instrucción. |
| Rombo | Decisión o condición. |
| Paralelogramo | Entrada o salida de datos. |
| Flechas | Dirección del flujo de ejecución. |

---

## 1.3. Implementación del programa

Una vez diseñado el algoritmo, podemos comenzar a escribir el programa utilizando un lenguaje de programación.

Esta fase se conoce como **implementación**.

El programador transforma los pasos definidos en el algoritmo en instrucciones que pueda ejecutar el ordenador.

En nuestro caso utilizaremos Java para desarrollar los programas.

### Código fuente

El código fuente es el conjunto de instrucciones que escribe el programador utilizando un lenguaje de programación.

Por ejemplo:

```java
public class Suma {

    public static void main(String[] args) {

        int numero1 = 5;
        int numero2 = 3;

        int resultado = numero1 + numero2;

        System.out.println("El resultado es: " + resultado);
    }
}
```

Este programa suma dos números enteros y muestra el resultado por pantalla.

La implementación debe respetar el diseño del algoritmo para que el programa realice correctamente la tarea prevista.

---

## 1.4. Verificación y pruebas

Una vez desarrollado el programa, es necesario comprobar que funciona correctamente antes de ponerlo a disposición de los usuarios.

Durante esta fase se buscan posibles errores y se comprueba que el programa realiza las operaciones esperadas.

### Errores del programa

Durante el desarrollo pueden aparecer diferentes errores que impidan que el programa funcione como queremos.

Por eso es necesario revisar el código y realizar diferentes pruebas.

### Juego de pruebas

Un **juego de pruebas** es un conjunto de situaciones o entradas de datos que utilizamos para comprobar el funcionamiento de un programa.

Las pruebas deben abarcar todas las posibilidades reales que puedan producirse durante su utilización.

Por ejemplo, si tenemos un programa que suma dos números, podemos probar diferentes valores:

| Primer número | Segundo número | Resultado esperado |
|---:|---:|---:|
| 5 | 3 | 8 |
| 10 | 20 | 30 |
| 0 | 5 | 5 |
| -4 | 6 | 2 |

De esta manera podemos comprobar que el programa funciona con diferentes valores y no solamente con un caso concreto.

Aunque realicemos muchas pruebas, siempre pueden aparecer situaciones que no habíamos previsto y que se detectarán cuando el programa ya esté siendo utilizado.

---

## 1.5. Puesta en marcha y mantenimiento

Cuando el programa ha superado las pruebas, puede ponerse en funcionamiento y empezar a utilizarse.

Sin embargo, el trabajo no termina aquí. Durante su utilización pueden aparecer problemas o nuevas necesidades que obliguen a modificar el programa.

El **mantenimiento** consiste en revisar y actualizar el programa para que continúe funcionando correctamente.

Algunos motivos por los que puede ser necesario realizar tareas de mantenimiento son:

- El programa no realiza exactamente lo que se esperaba.
- Se detectan errores que no aparecieron durante las pruebas.
- Es necesario incorporar nuevas funcionalidades.
- Hay que adaptar el programa a un nuevo sistema operativo.
- Es necesario realizar cambios para adaptarlo a otras aplicaciones o bases de datos.

Por tanto, el mantenimiento permite corregir errores y adaptar el programa a nuevas necesidades.

---

## Resumen del apartado

El desarrollo de una aplicación informática se puede dividir en cinco fases:

1. **Definición del problema:** conocer qué queremos resolver y establecer los objetivos.
2. **Diseño del algoritmo:** organizar los pasos necesarios para encontrar una solución.
3. **Implementación del programa:** escribir el código fuente utilizando un lenguaje de programación.
4. **Verificación y pruebas:** comprobar que el programa funciona correctamente.
5. **Puesta en marcha y mantenimiento:** utilizar el programa y realizar las modificaciones necesarias.

Estas fases permiten organizar el desarrollo de una aplicación informática y trabajar de forma ordenada.

---

[Volver al Tema 02](index.md)

[Siguiente apartado: Estructuras de selección](estructuras-seleccion.md)
