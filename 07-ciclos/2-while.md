# Ciclo `while` en Java

## 1. ¿Qué es el ciclo `while`?

El ciclo `while` permite repetir instrucciones mientras una condición sea verdadera.

En español, puede leerse así:

```text
Mientras se cumpla esta condición, repita estas instrucciones.
```

---

## 2. Sintaxis

```java
while (condicion) {
    // instrucciones que se repiten
}
```

---

## 3. Ejemplo básico

Mostrar los números del 1 al 5.

```java
public class NumerosWhile {
    public static void main(String[] args) {
        int contador = 1;

        while (contador <= 5) {
            System.out.println(contador);
            contador++;
        }
    }
}
```

---

## 4. Explicación línea a línea

```java
int contador = 1;
```

Se crea una variable que inicia en 1.

```java
while (contador <= 5)
```

El ciclo se repite mientras `contador` sea menor o igual a 5.

```java
System.out.println(contador);
```

Muestra el valor actual del contador.

```java
contador++;
```

Aumenta el contador en 1.

---

## 5. Prueba de escritorio

| Iteración | contador antes | Condición | Salida | contador después |
|---:|---:|---|---:|---:|
| 1 | 1 | true | 1 | 2 |
| 2 | 2 | true | 2 | 3 |
| 3 | 3 | true | 3 | 4 |
| 4 | 4 | true | 4 | 5 |
| 5 | 5 | true | 5 | 6 |
| 6 | 6 | false | - | - |

---

## 6. Ejemplo: sumar números del 1 al 5

```java
public class SumaWhile {
    public static void main(String[] args) {
        int contador = 1;
        int suma = 0;

        while (contador <= 5) {
            suma = suma + contador;
            contador++;
        }

        System.out.println("La suma es: " + suma);
    }
}
```

---

## 7. Explicación del acumulador

```java
suma = suma + contador;
```

Esta línea va acumulando los valores.

Proceso:

```text
suma = 0 + 1 = 1
suma = 1 + 2 = 3
suma = 3 + 3 = 6
suma = 6 + 4 = 10
suma = 10 + 5 = 15
```

---

## 8. Ejemplo: pedir contraseña

```java
import java.util.Scanner;

public class ValidarClaveWhile {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        String clave;
        String claveCorrecta = "java123";

        System.out.print("Ingrese la clave: ");
        clave = entrada.nextLine();

        while (!clave.equals(claveCorrecta)) {
            System.out.println("Clave incorrecta");
            System.out.print("Ingrese la clave nuevamente: ");
            clave = entrada.nextLine();
        }

        System.out.println("Acceso permitido");

        entrada.close();
    }
}
```

---

## 9. ¿Por qué se usa `!`?

```java
!clave.equals(claveCorrecta)
```

Significa:

```text
Mientras la clave no sea igual a la clave correcta.
```

---

## 10. Error común: ciclo infinito

Incorrecto:

```java
int contador = 1;

while (contador <= 5) {
    System.out.println(contador);
}
```

Falta actualizar el contador.

Correcto:

```java
int contador = 1;

while (contador <= 5) {
    System.out.println(contador);
    contador++;
}
```

---

## 11. ¿Cuándo usar `while`?

Usa `while` cuando:

- No sabes cuántas veces se repetirá el ciclo.
- La repetición depende de una condición.
- Necesitas validar datos.
- Debes repetir hasta que el usuario ingrese un valor correcto.

---

## 12. Ejercicios rápidos

1. Mostrar los números del 1 al 10 usando `while`.
2. Mostrar los números del 10 al 1 usando `while`.
3. Sumar los números del 1 al 100.
4. Pedir una contraseña hasta que sea correcta.
5. Pedir números hasta que el usuario ingrese 0.
