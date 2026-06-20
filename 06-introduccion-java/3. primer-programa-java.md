# Primer Programa en Java

## 1. Introducción

El primer programa que se suele escribir al aprender un lenguaje de programación es el famoso:

```text
Hola mundo
```

Este programa permite verificar que el entorno está funcionando y que el estudiante comprende la estructura mínima de un programa Java.

---

## 2. Código completo

Crear un archivo llamado:

```text
HolaMundo.java
```

Escribir el siguiente código:

```java
public class HolaMundo {
    public static void main(String[] args) {
        System.out.println("Hola mundo");
    }
}
```

---

## 3. Explicación línea a línea

### Línea 1

```java
public class HolaMundo {
```

Esta línea define una clase llamada `HolaMundo`.

En Java, todo programa debe estar dentro de una clase.

La palabra `public` indica que la clase puede ser accesible públicamente.

La palabra `class` indica que se está definiendo una clase.

`HolaMundo` es el nombre de la clase.

La llave `{` indica el inicio del bloque de la clase.

---

### Línea 2

```java
public static void main(String[] args) {
```

Esta línea define el método principal del programa.

El método `main` es el punto de entrada del programa.  
Esto significa que cuando Java ejecuta el programa, empieza por este método.

Partes importantes:

| Parte | Explicación sencilla |
|---|---|
| `public` | Permite que el método sea accesible |
| `static` | Permite ejecutar el método sin crear un objeto |
| `void` | Indica que el método no devuelve un valor |
| `main` | Nombre especial del método principal |
| `String[] args` | Permite recibir argumentos desde la consola |

No es necesario dominar todos estos términos al inicio, pero sí reconocer que esta línea debe estar presente en los programas básicos.

---

### Línea 3

```java
System.out.println("Hola mundo");
```

Esta instrucción muestra un mensaje en pantalla.

`System.out.println` imprime el texto y luego hace un salto de línea.

El texto se escribe entre comillas dobles.

El punto y coma `;` indica el final de la instrucción.

---

### Línea 4

```java
}
```

Cierra el bloque del método `main`.

---

### Línea 5

```java
}
```

Cierra el bloque de la clase.

---

## 4. Llaves en Java

Las llaves `{ }` permiten agrupar instrucciones.

Ejemplo:

```java
public class HolaMundo {
    public static void main(String[] args) {
        System.out.println("Hola mundo");
    }
}
```

La clase tiene un bloque.  
Dentro de la clase está el método `main`.  
Dentro del método están las instrucciones.

---

## 5. Punto y coma

En Java, muchas instrucciones terminan con punto y coma.

Correcto:

```java
System.out.println("Hola mundo");
```

Incorrecto:

```java
System.out.println("Hola mundo")
```

El segundo ejemplo genera error porque falta `;`.

---

## 6. Java distingue mayúsculas y minúsculas

Java es sensible a mayúsculas y minúsculas.

Correcto:

```java
System.out.println("Hola mundo");
```

Incorrecto:

```java
system.out.println("Hola mundo");
```

`System` debe iniciar con mayúscula.

---

## 7. Ejecutar en NetBeans

Pasos generales:

1. Abrir NetBeans.
2. Crear un proyecto Java.
3. Crear una clase llamada `HolaMundo`.
4. Escribir el código.
5. Ejecutar el programa.
6. Revisar la salida en la consola.

---

## 8. Ejecutar desde consola

Ubicarse en la carpeta donde está el archivo `HolaMundo.java`.

Compilar:

```bash
javac HolaMundo.java
```

Ejecutar:

```bash
java HolaMundo
```

Salida esperada:

```text
Hola mundo
```

---

## 9. Errores comunes en el primer programa

### Error 1. El archivo no se llama igual que la clase

Archivo incorrecto:

```text
Programa.java
```

Clase:

```java
public class HolaMundo {
}
```

Si la clase es pública, el archivo debe llamarse:

```text
HolaMundo.java
```

---

### Error 2. Falta el punto y coma

Incorrecto:

```java
System.out.println("Hola mundo")
```

Correcto:

```java
System.out.println("Hola mundo");
```

---

### Error 3. Falta una llave

Incorrecto:

```java
public class HolaMundo {
    public static void main(String[] args) {
        System.out.println("Hola mundo");
}
```

Falta una llave para cerrar la clase.

---

### Error 4. Escribir `Main` en lugar de `main`

Incorrecto:

```java
public static void Main(String[] args) {
}
```

Correcto:

```java
public static void main(String[] args) {
}
```

El método principal debe llamarse exactamente `main`.

---

## 10. Variaciones del primer programa

### Mensaje de bienvenida

```java
public class Bienvenida {
    public static void main(String[] args) {
        System.out.println("Bienvenido al curso de Algoritmia y Programación");
    }
}
```

---

### Varias líneas de salida

```java
public class DatosCurso {
    public static void main(String[] args) {
        System.out.println("Universidad del Pacífico");
        System.out.println("Ingeniería de Sistemas");
        System.out.println("Curso: Algoritmia y Programación");
    }
}
```

---

## 11. Recomendación

El estudiante debe escribir el programa manualmente, no copiarlo y pegarlo.

Escribirlo ayuda a reconocer:

- Llaves.
- Paréntesis.
- Comillas.
- Punto y coma.
- Mayúsculas y minúsculas.
- Estructura del método `main`.

La memoria muscular también hace parte del aprendizaje inicial de programación.
