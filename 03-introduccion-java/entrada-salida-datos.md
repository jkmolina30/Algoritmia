# Entrada y Salida de Datos en Java

## 1. Introducción

Todo programa necesita comunicarse con el usuario.

Para eso existen dos acciones básicas:

```text
Entrada de datos → El programa recibe información
Salida de datos  → El programa muestra información
```

Ejemplo:

```text
Entrada: nombre del estudiante
Salida: mensaje de bienvenida
```

---

## 2. Salida de datos

En Java se usa `System.out.print` o `System.out.println` para mostrar información.

---

## 3. `System.out.println`

Muestra un mensaje y luego hace un salto de línea.

```java
System.out.println("Hola mundo");
System.out.println("Bienvenido al curso");
```

Salida:

```text
Hola mundo
Bienvenido al curso
```

---

## 4. `System.out.print`

Muestra un mensaje sin saltar a la siguiente línea.

```java
System.out.print("Ingrese su nombre: ");
```

Esto permite que el usuario escriba en la misma línea.

---

## 5. Diferencia entre `print` y `println`

| Instrucción | Acción |
|---|---|
| `print` | Muestra texto sin salto de línea |
| `println` | Muestra texto con salto de línea |

Ejemplo:

```java
System.out.print("Hola ");
System.out.print("Ana");
```

Salida:

```text
Hola Ana
```

Ejemplo:

```java
System.out.println("Hola");
System.out.println("Ana");
```

Salida:

```text
Hola
Ana
```

---

## 6. Entrada de datos con Scanner

Para leer datos desde el teclado se usa la clase `Scanner`.

Primero se importa:

```java
import java.util.Scanner;
```

Luego se crea el objeto:

```java
Scanner entrada = new Scanner(System.in);
```

---

## 7. Leer números enteros

```java
int edad;

System.out.print("Ingrese su edad: ");
edad = entrada.nextInt();
```

`nextInt()` lee un número entero.

---

## 8. Leer números decimales

```java
double nota;

System.out.print("Ingrese su nota: ");
nota = entrada.nextDouble();
```

`nextDouble()` lee un número decimal.

---

## 9. Leer texto de una palabra

```java
String nombre;

System.out.print("Ingrese su nombre: ");
nombre = entrada.next();
```

`next()` lee solo una palabra.

Si el usuario escribe:

```text
Juan Carlos
```

Solo se leerá:

```text
Juan
```

---

## 10. Leer texto completo

```java
String nombreCompleto;

System.out.print("Ingrese su nombre completo: ");
nombreCompleto = entrada.nextLine();
```

`nextLine()` lee toda la línea.

Si el usuario escribe:

```text
Juan Carlos Molina
```

Se guarda todo el texto.

---

## 11. Problema común con `nextLine`

Cuando se usa `nextInt()` o `nextDouble()` antes de `nextLine()`, puede quedar un salto de línea pendiente.

Ejemplo problemático:

```java
int edad;
String nombre;

System.out.print("Ingrese su edad: ");
edad = entrada.nextInt();

System.out.print("Ingrese su nombre: ");
nombre = entrada.nextLine();
```

En algunos casos, `nombre` queda vacío.

Solución:

```java
entrada.nextLine();
```

Ejemplo corregido:

```java
int edad;
String nombre;

System.out.print("Ingrese su edad: ");
edad = entrada.nextInt();

entrada.nextLine(); // Limpia el salto de línea pendiente

System.out.print("Ingrese su nombre: ");
nombre = entrada.nextLine();
```

---

## 12. Ejemplo 1. Leer nombre

```java
import java.util.Scanner;

public class LeerNombre {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        String nombre;

        System.out.print("Ingrese su nombre: ");
        nombre = entrada.nextLine();

        System.out.println("Hola, " + nombre);

        entrada.close();
    }
}
```

---

## 13. Ejemplo 2. Leer edad

```java
import java.util.Scanner;

public class LeerEdad {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int edad;

        System.out.print("Ingrese su edad: ");
        edad = entrada.nextInt();

        System.out.println("Su edad es: " + edad);

        entrada.close();
    }
}
```

---

## 14. Ejemplo 3. Leer nota

```java
import java.util.Scanner;

public class LeerNota {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double nota;

        System.out.print("Ingrese su nota: ");
        nota = entrada.nextDouble();

        System.out.println("La nota ingresada es: " + nota);

        entrada.close();
    }
}
```

---

## 15. Ejemplo 4. Nombre y nota

```java
import java.util.Scanner;

public class NombreYNota {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        String nombre;
        double nota;

        System.out.print("Ingrese el nombre del estudiante: ");
        nombre = entrada.nextLine();

        System.out.print("Ingrese la nota final: ");
        nota = entrada.nextDouble();

        System.out.println("El estudiante " + nombre + " obtuvo " + nota);

        entrada.close();
    }
}
```

---

## 16. Recomendaciones

- Usar `nextInt()` para enteros.
- Usar `nextDouble()` para decimales.
- Usar `nextLine()` para textos completos.
- Recordar limpiar el salto de línea cuando se mezclan números y textos.
- Mostrar mensajes claros al usuario antes de leer datos.
- Cerrar el `Scanner` al final del programa.

---

## 17. Resumen

La entrada y salida de datos permite que los programas interactúen con el usuario. En Java, la salida se realiza con `System.out.print` y `System.out.println`, mientras que la entrada se realiza usando `Scanner`.
