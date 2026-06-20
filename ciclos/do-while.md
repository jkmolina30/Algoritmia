# Ciclo `do-while` en Java

## 1. ¿Qué es el ciclo `do-while`?

El ciclo `do-while` ejecuta primero las instrucciones y después evalúa la condición.

Esto significa que el bloque se ejecuta **al menos una vez**.

---

## 2. Sintaxis

```java
do {
    // instrucciones
} while (condicion);
```

Observa que al final hay punto y coma:

```java
} while (condicion);
```

---

## 3. Diferencia entre `while` y `do-while`

| Ciclo | Evalúa condición | ¿Ejecuta al menos una vez? |
|---|---|---|
| `while` | Antes de entrar | No necesariamente |
| `do-while` | Después de ejecutar | Sí |

---

## 4. Ejemplo básico

Mostrar los números del 1 al 5.

```java
public class NumerosDoWhile {
    public static void main(String[] args) {
        int contador = 1;

        do {
            System.out.println(contador);
            contador++;
        } while (contador <= 5);
    }
}
```

---

## 5. Explicación

Primero se ejecuta el bloque:

```java
System.out.println(contador);
contador++;
```

Luego se revisa la condición:

```java
contador <= 5
```

Si es verdadera, se repite.

---

## 6. Ejemplo: menú básico

```java
import java.util.Scanner;

public class MenuDoWhile {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int opcion;

        do {
            System.out.println("===== MENÚ =====");
            System.out.println("1. Saludar");
            System.out.println("2. Mostrar curso");
            System.out.println("3. Salir");
            System.out.print("Ingrese una opción: ");
            opcion = entrada.nextInt();

            switch (opcion) {
                case 1:
                    System.out.println("Hola, bienvenido");
                    break;
                case 2:
                    System.out.println("Curso de Algoritmia y Programación");
                    break;
                case 3:
                    System.out.println("Saliendo del programa");
                    break;
                default:
                    System.out.println("Opción no válida");
                    break;
            }

        } while (opcion != 3);

        entrada.close();
    }
}
```

---

## 7. ¿Por qué usar `do-while` en menús?

Porque un menú debe mostrarse al menos una vez.

Luego, dependiendo de la opción del usuario, se decide si se repite o termina.

---

## 8. Ejemplo: validar opción

```java
import java.util.Scanner;

public class ValidarOpcion {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int opcion;

        do {
            System.out.print("Ingrese una opción entre 1 y 3: ");
            opcion = entrada.nextInt();
        } while (opcion < 1 || opcion > 3);

        System.out.println("Opción válida: " + opcion);

        entrada.close();
    }
}
```

---

## 9. Explicación

La condición:

```java
opcion < 1 || opcion > 3
```

significa:

```text
Repetir mientras la opción sea menor que 1 o mayor que 3.
```

---

## 10. Error común

Olvidar el punto y coma final.

Incorrecto:

```java
do {
    System.out.println("Hola");
} while (opcion != 0)
```

Correcto:

```java
do {
    System.out.println("Hola");
} while (opcion != 0);
```

---

## 11. ¿Cuándo usar `do-while`?

Usa `do-while` cuando:

- El proceso debe ejecutarse al menos una vez.
- Estás trabajando con menús.
- Necesitas pedir un dato y validar después.
- Quieres repetir hasta que el usuario decida salir.

---

## 12. Ejercicios rápidos

1. Crear un menú que se repita hasta elegir salir.
2. Pedir una nota hasta que esté entre 0.0 y 5.0.
3. Pedir una opción entre 1 y 4.
4. Crear una calculadora que se repita hasta que el usuario elija salir.
5. Pedir una edad válida entre 0 y 120.
