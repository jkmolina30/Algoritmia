# Errores Comunes al Iniciar en Java

## 1. Introducción

Cuando se empieza a programar en Java, los errores son normales. No significan que el estudiante no pueda aprender. Significan que hay algo que debe revisarse y corregirse.

Aprender a leer errores es una habilidad fundamental en programación.

---

## 2. Tipos de errores

| Tipo de error | Explicación |
|---|---|
| Error de sintaxis | El código está mal escrito según las reglas de Java |
| Error lógico | El programa ejecuta, pero el resultado es incorrecto |
| Error de ejecución | El programa se detiene mientras está funcionando |

---

## 3. Error por falta de punto y coma

Incorrecto:

```java
System.out.println("Hola mundo")
```

Correcto:

```java
System.out.println("Hola mundo");
```

En Java, muchas instrucciones terminan con `;`.

---

## 4. Error por mayúsculas y minúsculas

Incorrecto:

```java
system.out.println("Hola mundo");
```

Correcto:

```java
System.out.println("Hola mundo");
```

Java distingue mayúsculas y minúsculas.

---

## 5. Error por nombre de archivo diferente a la clase

Archivo:

```text
Programa.java
```

Código:

```java
public class HolaMundo {
}
```

Esto genera error si la clase es pública.

Correcto:

Archivo:

```text
HolaMundo.java
```

Código:

```java
public class HolaMundo {
}
```

---

## 6. Error por falta de llaves

Incorrecto:

```java
public class HolaMundo {
    public static void main(String[] args) {
        System.out.println("Hola mundo");
}
```

Falta una llave para cerrar la clase.

Correcto:

```java
public class HolaMundo {
    public static void main(String[] args) {
        System.out.println("Hola mundo");
    }
}
```

---

## 7. Error por no importar Scanner

Incorrecto:

```java
public class LeerEdad {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);
    }
}
```

Falta importar `Scanner`.

Correcto:

```java
import java.util.Scanner;

public class LeerEdad {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);
    }
}
```

---

## 8. Error por usar mal el método main

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

## 9. Error lógico en el promedio

Incorrecto:

```java
promedio = nota1 + nota2 + nota3 / 3;
```

Java primero divide `nota3 / 3`.

Correcto:

```java
promedio = (nota1 + nota2 + nota3) / 3;
```

Los paréntesis son necesarios.

---

## 10. Error por división entera

Código:

```java
int a = 5;
int b = 2;
double resultado = a / b;
```

Resultado:

```text
2.0
```

¿Por qué?

Porque `a` y `b` son enteros. Java realiza división entera antes de guardar el resultado.

Correcto:

```java
double resultado = (double) a / b;
```

O también:

```java
double resultado = 5.0 / 2;
```

Resultado:

```text
2.5
```

---

## 11. Error al mezclar `nextInt` y `nextLine`

Problema:

```java
int edad;
String nombre;

edad = entrada.nextInt();
nombre = entrada.nextLine();
```

`nombre` puede quedar vacío.

Solución:

```java
edad = entrada.nextInt();
entrada.nextLine();
nombre = entrada.nextLine();
```

---

## 12. Error por no inicializar variables

Incorrecto:

```java
int edad;
System.out.println(edad);
```

La variable fue declarada, pero no tiene valor.

Correcto:

```java
int edad = 18;
System.out.println(edad);
```

---

## 13. Error por usar comillas incorrectas

Para texto se usan comillas dobles:

```java
String nombre = "Ana";
```

Para un solo carácter se usan comillas simples:

```java
char grupo = 'A';
```

Incorrecto:

```java
String nombre = 'Ana';
char grupo = "A";
```

---

## 14. Recomendaciones para corregir errores

Cuando aparezca un error:

1. Leer el mensaje con calma.
2. Revisar la línea indicada.
3. Verificar punto y coma.
4. Verificar llaves.
5. Revisar mayúsculas y minúsculas.
6. Revisar nombres de variables.
7. Revisar si falta un import.
8. Revisar si el archivo se llama igual que la clase.
9. Corregir una cosa a la vez.
10. Volver a ejecutar.

---

## 15. Recomendación final

El error no debe verse como fracaso.

En programación, corregir errores es parte del proceso de aprendizaje. Cada error ayuda a comprender mejor cómo funciona el lenguaje.
