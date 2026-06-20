# Unidad 8. Funciones, Procedimientos y Métodos

## Presentación de la unidad

Cuando los programas crecen, escribir todo el código dentro del `main` puede volverlo difícil de leer, corregir y mantener.

Para organizar mejor el código se utiliza la **modularización**.

Modularizar significa dividir un problema grande en partes más pequeñas.

En programación, esas partes pueden llamarse:

- Funciones.
- Procedimientos.
- Métodos.

En PSeInt se habla generalmente de **funciones** y **subprocesos**.  
En Java se habla de **métodos**.

---

## 1. ¿Qué es modularizar?

Modularizar es dividir un programa en bloques más pequeños, cada uno con una tarea específica.

Ejemplo:

En un sistema de notas podríamos tener métodos para:

- Leer notas.
- Calcular promedio.
- Validar nota.
- Mostrar resultados.
- Determinar si aprueba.

Esto hace que el programa sea más ordenado.

---

## 2. ¿Por qué usar funciones o métodos?

Sirven para:

- Evitar repetir código.
- Organizar mejor el programa.
- Facilitar correcciones.
- Reutilizar instrucciones.
- Hacer el código más fácil de entender.
- Dividir problemas grandes en problemas pequeños.

---

## 3. Función

Una función es un bloque de instrucciones que realiza una tarea y normalmente devuelve un valor.

Ejemplo conceptual:

```text
sumar(5, 3) devuelve 8
```

---

## 4. Procedimiento

Un procedimiento realiza una tarea, pero no necesariamente devuelve un valor.

Ejemplo conceptual:

```text
mostrarMenu()
```

Este procedimiento solo muestra opciones en pantalla.

---

## 5. Método en Java

En Java, las funciones y procedimientos se implementan como **métodos**.

Un método puede:

- Recibir datos.
- Procesar datos.
- Devolver un resultado.
- O simplemente ejecutar instrucciones sin devolver nada.

---

## 6. Parámetros

Los parámetros son datos que recibe una función o método.

Ejemplo:

```java
public static int sumar(int a, int b)
```

Aquí `a` y `b` son parámetros.

---

## 7. Argumentos

Los argumentos son los valores reales que se envían cuando se llama al método.

```java
sumar(5, 3);
```

Aquí `5` y `3` son argumentos.

---

## 8. Retorno

El retorno es el valor que una función o método devuelve.

```java
return a + b;
```

Esto devuelve la suma.

---

## 9. Métodos con retorno en Java

```java
public static int sumar(int a, int b) {
    return a + b;
}
```

Este método:

- Se llama `sumar`.
- Recibe dos enteros.
- Devuelve un entero.
- Usa `return`.

---

## 10. Métodos sin retorno en Java

Cuando un método no devuelve valor, se usa `void`.

```java
public static void saludar() {
    System.out.println("Hola, bienvenido");
}
```

Este método solo muestra un mensaje.

---

## 11. Llamar un método

Para usar un método, se debe llamar por su nombre.

```java
saludar();
```

Si el método recibe parámetros:

```java
int resultado = sumar(5, 3);
```

---

## 12. Estructura general de un método en Java

```java
public static tipoRetorno nombreMetodo(parametros) {
    // instrucciones
    return valor;
}
```

Si no retorna nada:

```java
public static void nombreMetodo() {
    // instrucciones
}
```

---

## 13. ¿Qué significa `static`?

En los ejemplos iniciales usamos `static` para poder llamar los métodos desde el método `main` sin crear objetos.

Más adelante, cuando se estudie Programación Orientada a Objetos, se profundizará en este concepto.

Por ahora, se puede recordar así:

```text
En programas básicos de consola, usamos static para poder llamar métodos desde main.
```

---

## 14. Ejemplo básico

```java
public class EjemploMetodo {
    public static void saludar() {
        System.out.println("Hola, bienvenido");
    }

    public static void main(String[] args) {
        saludar();
    }
}
```

---

## 15. Ejemplo con retorno

```java
public class EjemploSuma {
    public static int sumar(int a, int b) {
        return a + b;
    }

    public static void main(String[] args) {
        int resultado = sumar(5, 3);
        System.out.println("La suma es: " + resultado);
    }
}
```

---

## 16. Métodos y arreglos

Un método puede recibir un arreglo.

```java
public static double calcularPromedio(double[] notas) {
    double suma = 0;

    for (int i = 0; i < notas.length; i++) {
        suma = suma + notas[i];
    }

    return suma / notas.length;
}
```

---

## 17. Métodos y matrices

También puede recibir una matriz.

```java
public static int sumarMatriz(int[][] matriz) {
    int suma = 0;

    for (int fila = 0; fila < matriz.length; fila++) {
        for (int columna = 0; columna < matriz[fila].length; columna++) {
            suma = suma + matriz[fila][columna];
        }
    }

    return suma;
}
```

---

## 18. Buenas prácticas

- Un método debe realizar una tarea clara.
- El nombre del método debe indicar lo que hace.
- Evitar métodos demasiado largos.
- Usar parámetros cuando el método necesita datos.
- Usar `return` cuando se debe devolver un resultado.
- No repetir código innecesariamente.
- Probar cada método por separado.

---

## 19. Nombres recomendados para métodos

Correctos:

```java
calcularPromedio
validarNota
mostrarMenu
sumarNumeros
buscarMayor
```

Poco recomendados:

```java
metodo1
hacer
proceso
x
```

---

## 20. Resultado de aprendizaje

Al finalizar esta unidad, el estudiante debe poder crear funciones en PSeInt y métodos en Java para dividir programas en partes más pequeñas, reutilizables y fáciles de entender.
