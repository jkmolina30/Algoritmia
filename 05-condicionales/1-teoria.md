# Unidad 4. Condicionales

## Presentación de la unidad

En programación no todos los problemas se resuelven siguiendo una sola secuencia de instrucciones. Muchas veces el programa debe **tomar decisiones**.

Por ejemplo:

- Si la nota es mayor o igual a 3.0, el estudiante aprueba.
- Si la edad es mayor o igual a 18, la persona es mayor de edad.
- Si el usuario escribe una opción del menú, el programa debe ejecutar una acción.
- Si una contraseña es correcta, se permite el acceso.

Para resolver este tipo de situaciones se utilizan las **estructuras condicionales**.

---

## 1. ¿Qué es una condición?

Una condición es una expresión que puede tener únicamente dos resultados:

```text
Verdadero
Falso
```

En Java, esos resultados se representan como:

```java
true
false
```

Ejemplo:

```java
edad >= 18
```

Esta condición pregunta:

```text
¿La edad es mayor o igual a 18?
```

Si `edad` vale 20, la condición es verdadera.  
Si `edad` vale 15, la condición es falsa.

---

## 2. ¿Para qué sirven los condicionales?

Los condicionales permiten que un programa tome decisiones.

Sin condicionales, un programa solo ejecutaría instrucciones en orden, una detrás de otra.

Con condicionales, el programa puede elegir qué camino seguir.

Ejemplo cotidiano:

```text
Si está lloviendo, llevo paraguas.
Si no está lloviendo, salgo sin paraguas.
```

Ejemplo en programación:

```java
if (nota >= 3.0) {
    System.out.println("Aprobó");
} else {
    System.out.println("Reprobó");
}
```

---

## 3. Operadores relacionales

Los operadores relacionales permiten comparar valores.

| Operador | Significado | Ejemplo |
|---|---|---|
| `>` | Mayor que | `edad > 18` |
| `<` | Menor que | `edad < 18` |
| `>=` | Mayor o igual que | `nota >= 3.0` |
| `<=` | Menor o igual que | `nota <= 5.0` |
| `==` | Igual que | `opcion == 1` |
| `!=` | Diferente de | `opcion != 0` |

---

## 4. Diferencia entre `=` y `==`

Este es uno de los errores más comunes en Java.

| Símbolo | Uso | Ejemplo |
|---|---|---|
| `=` | Asignar un valor | `edad = 18;` |
| `==` | Comparar igualdad | `edad == 18` |

Ejemplo incorrecto:

```java
if (edad = 18) {
}
```

Ejemplo correcto:

```java
if (edad == 18) {
}
```

---

## 5. Operadores lógicos

Los operadores lógicos permiten combinar varias condiciones.

| Operador | Nombre | Significado |
|---|---|---|
| `&&` | Y lógico | Todas las condiciones deben cumplirse |
| `||` | O lógico | Al menos una condición debe cumplirse |
| `!` | Negación | Invierte el valor lógico |

---

## 6. Ejemplo con operador `&&`

Problema:

Una nota es válida si está entre 0.0 y 5.0.

```java
if (nota >= 0.0 && nota <= 5.0) {
    System.out.println("La nota es válida");
}
```

Explicación:

La condición solo será verdadera si se cumplen las dos partes:

```text
nota >= 0.0
nota <= 5.0
```

---

## 7. Ejemplo con operador `||`

Problema:

Un usuario puede tener acceso especial si es administrador o docente.

```java
if (rol.equals("administrador") || rol.equals("docente")) {
    System.out.println("Acceso permitido");
}
```

La condición será verdadera si al menos una de las dos condiciones se cumple.

---

## 8. Ejemplo con operador `!`

```java
if (!activo) {
    System.out.println("El usuario no está activo");
}
```

Si `activo` es `false`, entonces `!activo` se convierte en `true`.

---

# 9. Condicional simple `if`

El condicional simple ejecuta instrucciones solo si la condición es verdadera.

## Sintaxis

```java
if (condicion) {
    // instrucciones si la condición es verdadera
}
```

## Ejemplo

```java
if (edad >= 18) {
    System.out.println("La persona es mayor de edad");
}
```

Si la edad es menor de 18, no se muestra nada.

---

# 10. Condicional doble `if - else`

El condicional doble permite ejecutar una acción cuando la condición es verdadera y otra cuando es falsa.

## Sintaxis

```java
if (condicion) {
    // instrucciones si la condición es verdadera
} else {
    // instrucciones si la condición es falsa
}
```

## Ejemplo

```java
if (nota >= 3.0) {
    System.out.println("Aprobó");
} else {
    System.out.println("Reprobó");
}
```

---

# 11. Condicional múltiple `if - else if - else`

Se usa cuando hay varias opciones posibles.

## Sintaxis

```java
if (condicion1) {
    // instrucciones
} else if (condicion2) {
    // instrucciones
} else if (condicion3) {
    // instrucciones
} else {
    // instrucciones si ninguna condición anterior se cumple
}
```

## Ejemplo

```java
if (nota < 3.0) {
    System.out.println("Desempeño bajo");
} else if (nota < 4.0) {
    System.out.println("Desempeño básico");
} else if (nota < 4.6) {
    System.out.println("Desempeño alto");
} else {
    System.out.println("Desempeño superior");
}
```

---

# 12. Condicionales anidados

Un condicional anidado es un condicional dentro de otro.

## Ejemplo

```java
if (usuarioCorrecto) {
    if (claveCorrecta) {
        System.out.println("Acceso permitido");
    } else {
        System.out.println("Clave incorrecta");
    }
} else {
    System.out.println("Usuario incorrecto");
}
```

Se recomienda no abusar de los condicionales anidados porque pueden hacer que el código sea difícil de leer.

---

# 13. Condicional `switch`

El `switch` se usa cuando una variable puede tomar varios valores específicos.

Es útil para menús.

## Sintaxis

```java
switch (opcion) {
    case 1:
        // instrucciones
        break;
    case 2:
        // instrucciones
        break;
    default:
        // instrucciones si no coincide ninguna opción
        break;
}
```

## Ejemplo

```java
switch (opcion) {
    case 1:
        System.out.println("Consultar saldo");
        break;
    case 2:
        System.out.println("Retirar dinero");
        break;
    case 3:
        System.out.println("Salir");
        break;
    default:
        System.out.println("Opción no válida");
        break;
}
```

---

## 14. ¿Para qué sirve `break`?

En un `switch`, `break` detiene la ejecución del caso actual.

Si se omite, Java puede continuar ejecutando el siguiente caso, lo cual puede generar errores lógicos.

---

# 15. Comparación de textos en Java

Para comparar números usamos `==`.

Ejemplo:

```java
if (edad == 18) {
}
```

Pero para comparar textos no se recomienda usar `==`.  
Para textos se usa `.equals()`.

## Correcto

```java
if (usuario.equals("admin")) {
    System.out.println("Usuario administrador");
}
```

## Ignorar mayúsculas y minúsculas

```java
if (usuario.equalsIgnoreCase("admin")) {
    System.out.println("Usuario administrador");
}
```

Esto permite que funcionen entradas como:

```text
Admin
ADMIN
admin
```

---

# 16. Validación de datos

Validar significa revisar si un dato ingresado por el usuario cumple ciertas condiciones.

Ejemplo:

Una nota debe estar entre 0.0 y 5.0.

```java
if (nota >= 0.0 && nota <= 5.0) {
    System.out.println("Nota válida");
} else {
    System.out.println("Nota inválida");
}
```

La validación es una práctica importante porque evita que el programa trabaje con datos incorrectos.

---

# 17. Ejemplo completo: nota válida y aprobación

```java
import java.util.Scanner;

public class ValidarNota {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double nota;

        System.out.print("Ingrese la nota: ");
        nota = entrada.nextDouble();

        if (nota >= 0.0 && nota <= 5.0) {
            if (nota >= 3.0) {
                System.out.println("Nota válida. El estudiante aprobó.");
            } else {
                System.out.println("Nota válida. El estudiante reprobó.");
            }
        } else {
            System.out.println("La nota ingresada no es válida.");
        }

        entrada.close();
    }
}
```

---

# 18. Buenas prácticas con condicionales

- Usar nombres de variables claros.
- Evitar condiciones demasiado largas.
- Usar paréntesis cuando mejoren la lectura.
- Validar datos antes de procesarlos.
- Comparar textos con `.equals()` o `.equalsIgnoreCase()`.
- No confundir `=` con `==`.
- Usar `switch` cuando haya un menú con opciones fijas.
- Probar cada camino posible del condicional.
- Hacer prueba de escritorio.

---

# 19. Resultado de aprendizaje

Al finalizar esta unidad, el estudiante debe poder construir programas en Java que tomen decisiones usando `if`, `if-else`, `else if`, condicionales anidados, operadores relacionales, operadores lógicos y `switch`.
