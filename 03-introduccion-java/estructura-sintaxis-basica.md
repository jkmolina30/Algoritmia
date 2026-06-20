# Estructura y Sintaxis Básica de Java

## 1. ¿Qué es la sintaxis?

La **sintaxis** es el conjunto de reglas que indica cómo se debe escribir correctamente un lenguaje de programación.

En español, una frase debe respetar reglas para entenderse.  
En Java ocurre igual: el código debe respetar reglas para que el compilador lo entienda.

---

## 2. Estructura mínima de un programa Java

```java
public class NombreClase {
    public static void main(String[] args) {
        // Instrucciones
    }
}
```

---

## 3. Clase

Una clase es una estructura que agrupa código.

Ejemplo:

```java
public class PromedioNotas {
}
```

En programas básicos, la clase contiene el método `main`.

---

## 4. Método main

El método `main` es el punto de inicio del programa.

```java
public static void main(String[] args) {
}
```

Cuando se ejecuta un programa Java, la JVM busca este método para iniciar.

---

## 5. Instrucciones

Una instrucción es una orden que el programa debe ejecutar.

Ejemplo:

```java
System.out.println("Hola");
```

Las instrucciones suelen finalizar con punto y coma.

---

## 6. Comentarios

Los comentarios sirven para explicar el código.  
Java los ignora al ejecutar el programa.

### Comentario de una línea

```java
// Este programa muestra un mensaje
```

### Comentario de varias líneas

```java
/*
Este programa fue creado
para practicar la estructura básica de Java.
*/
```

---

## 7. Variables

Una variable es un espacio de memoria donde se guarda un dato.

Ejemplo:

```java
int edad = 18;
```

Lectura sencilla:

```text
Se crea una variable llamada edad, de tipo entero, y se guarda el valor 18.
```

---

## 8. Tipos de datos básicos

| Tipo | Uso | Ejemplo |
|---|---|---|
| `int` | Números enteros | `int edad = 18;` |
| `double` | Números decimales | `double nota = 4.5;` |
| `char` | Un solo carácter | `char grupo = 'A';` |
| `String` | Texto | `String nombre = "Ana";` |
| `boolean` | Verdadero o falso | `boolean activo = true;` |

---

## 9. Declaración de variables

Declarar una variable significa crearla e indicar qué tipo de dato guardará.

Ejemplo:

```java
int cantidad;
double promedio;
String nombre;
```

---

## 10. Asignación de valores

Asignar un valor significa guardar un dato en una variable.

Ejemplo:

```java
cantidad = 10;
promedio = 4.3;
nombre = "Carlos";
```

También se puede declarar y asignar en la misma línea:

```java
int cantidad = 10;
double promedio = 4.3;
String nombre = "Carlos";
```

---

## 11. Operadores aritméticos

| Operador | Significado | Ejemplo |
|---|---|---|
| `+` | Suma | `a + b` |
| `-` | Resta | `a - b` |
| `*` | Multiplicación | `a * b` |
| `/` | División | `a / b` |
| `%` | Módulo o residuo | `a % b` |

---

## 12. Concatenación

En Java, el símbolo `+` también se usa para unir texto con variables.

Ejemplo:

```java
String nombre = "Ana";
System.out.println("Hola " + nombre);
```

Salida:

```text
Hola Ana
```

---

## 13. Nombres de clases

Las clases deben usar nombres claros y comenzar con mayúscula.

Ejemplos correctos:

```java
PromedioNotas
AreaRectangulo
SumaDosNumeros
```

Ejemplos poco recomendados:

```java
clase1
programa
x
```

---

## 14. Nombres de variables

Las variables deben usar nombres claros y comenzar con minúscula.

Ejemplos correctos:

```java
notaFinal
cantidadEstudiantes
valorProducto
```

Ejemplos poco recomendados:

```java
x
n
dato
```

---

## 15. Indentación

La indentación es el espacio que se deja al inicio de una línea para mostrar que pertenece a un bloque.

Código desordenado:

```java
public class Ejemplo {
public static void main(String[] args) {
System.out.println("Hola");
}
}
```

Código ordenado:

```java
public class Ejemplo {
    public static void main(String[] args) {
        System.out.println("Hola");
    }
}
```

La indentación no siempre cambia el funcionamiento, pero mejora mucho la lectura.

---

## 16. Reglas básicas que se deben recordar

- Java distingue mayúsculas y minúsculas.
- Las instrucciones suelen terminar en `;`.
- Los textos van entre comillas dobles.
- Los caracteres individuales van entre comillas simples.
- Las llaves `{ }` abren y cierran bloques.
- El archivo debe llamarse igual que la clase pública.
- El método principal debe llamarse `main`.
- Las variables deben declararse antes de usarse.

---

## 17. Ejemplo integrador

```java
public class DatosEstudiante {
    public static void main(String[] args) {
        String nombre = "Ana";
        int edad = 18;
        double nota = 4.5;

        System.out.println("Nombre: " + nombre);
        System.out.println("Edad: " + edad);
        System.out.println("Nota: " + nota);
    }
}
```

---

## 18. Explicación

```java
String nombre = "Ana";
```

Crea una variable de texto.

```java
int edad = 18;
```

Crea una variable entera.

```java
double nota = 4.5;
```

Crea una variable decimal.

```java
System.out.println("Nombre: " + nombre);
```

Muestra texto junto con el contenido de una variable.

---

## 19. Resumen

La sintaxis de Java exige escribir el código con reglas claras. Aunque al inicio puede parecer estricta, esta precisión ayuda a formar disciplina y orden al programar.
