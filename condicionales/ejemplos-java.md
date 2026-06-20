# Ejemplos en Java: Condicionales

## Presentación

En este archivo se desarrollan ejemplos de condicionales en Java.  
Cada ejemplo busca que el estudiante comprenda cómo un programa puede tomar decisiones.

---

# Ejemplo 1. Mayor de edad

## Problema

Leer la edad de una persona e indicar si es mayor de edad.

## Código

```java
import java.util.Scanner;

public class MayorEdad {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int edad;

        System.out.print("Ingrese su edad: ");
        edad = entrada.nextInt();

        if (edad >= 18) {
            System.out.println("La persona es mayor de edad");
        } else {
            System.out.println("La persona es menor de edad");
        }

        entrada.close();
    }
}
```

## Explicación

```java
if (edad >= 18)
```

Evalúa si la edad es mayor o igual a 18.

Si la condición es verdadera, se ejecuta el primer bloque.  
Si es falsa, se ejecuta el bloque del `else`.

---

# Ejemplo 2. Número positivo, negativo o cero

```java
import java.util.Scanner;

public class PositivoNegativoCero {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double numero;

        System.out.print("Ingrese un número: ");
        numero = entrada.nextDouble();

        if (numero > 0) {
            System.out.println("El número es positivo");
        } else if (numero < 0) {
            System.out.println("El número es negativo");
        } else {
            System.out.println("El número es cero");
        }

        entrada.close();
    }
}
```

## Explicación

Se usan tres caminos posibles:

- Si `numero > 0`, es positivo.
- Si `numero < 0`, es negativo.
- Si no cumple ninguna de las anteriores, es cero.

---

# Ejemplo 3. Nota aprobada o reprobada

```java
import java.util.Scanner;

public class AprobarMateria {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double nota;

        System.out.print("Ingrese la nota final: ");
        nota = entrada.nextDouble();

        if (nota >= 3.0) {
            System.out.println("El estudiante aprobó");
        } else {
            System.out.println("El estudiante reprobó");
        }

        entrada.close();
    }
}
```

---

# Ejemplo 4. Validar nota

```java
import java.util.Scanner;

public class ValidarNota {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double nota;

        System.out.print("Ingrese la nota: ");
        nota = entrada.nextDouble();

        if (nota >= 0.0 && nota <= 5.0) {
            System.out.println("La nota es válida");
        } else {
            System.out.println("La nota no es válida");
        }

        entrada.close();
    }
}
```

## Explicación

La condición usa `&&`, porque ambas condiciones deben cumplirse:

```java
nota >= 0.0 && nota <= 5.0
```

---

# Ejemplo 5. Desempeño académico

```java
import java.util.Scanner;

public class DesempenoAcademico {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double nota;

        System.out.print("Ingrese la nota: ");
        nota = entrada.nextDouble();

        if (nota < 0.0 || nota > 5.0) {
            System.out.println("Nota no válida");
        } else if (nota < 3.0) {
            System.out.println("Desempeño bajo");
        } else if (nota < 4.0) {
            System.out.println("Desempeño básico");
        } else if (nota < 4.6) {
            System.out.println("Desempeño alto");
        } else {
            System.out.println("Desempeño superior");
        }

        entrada.close();
    }
}
```

## Explicación

Primero se valida si la nota está fuera del rango.  
Después se clasifican los desempeños.

---

# Ejemplo 6. Comparar textos

## Problema

Leer un usuario y verificar si es `admin`.

```java
import java.util.Scanner;

public class CompararUsuario {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        String usuario;

        System.out.print("Ingrese el usuario: ");
        usuario = entrada.nextLine();

        if (usuario.equalsIgnoreCase("admin")) {
            System.out.println("Usuario administrador");
        } else {
            System.out.println("Usuario común");
        }

        entrada.close();
    }
}
```

## Explicación

Para comparar textos se usa:

```java
equalsIgnoreCase()
```

Así no importa si el usuario escribe `admin`, `Admin` o `ADMIN`.

---

# Ejemplo 7. Menú con `switch`

```java
import java.util.Scanner;

public class MenuBasico {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int opcion;

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

        entrada.close();
    }
}
```

---

# Ejemplo 8. Calculadora básica con `switch`

```java
import java.util.Scanner;

public class CalculadoraBasica {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double num1;
        double num2;
        int opcion;

        System.out.print("Ingrese el primer número: ");
        num1 = entrada.nextDouble();

        System.out.print("Ingrese el segundo número: ");
        num2 = entrada.nextDouble();

        System.out.println("1. Sumar");
        System.out.println("2. Restar");
        System.out.println("3. Multiplicar");
        System.out.println("4. Dividir");
        System.out.print("Ingrese una opción: ");
        opcion = entrada.nextInt();

        switch (opcion) {
            case 1:
                System.out.println("Resultado: " + (num1 + num2));
                break;
            case 2:
                System.out.println("Resultado: " + (num1 - num2));
                break;
            case 3:
                System.out.println("Resultado: " + (num1 * num2));
                break;
            case 4:
                if (num2 != 0) {
                    System.out.println("Resultado: " + (num1 / num2));
                } else {
                    System.out.println("No se puede dividir entre cero");
                }
                break;
            default:
                System.out.println("Opción no válida");
                break;
        }

        entrada.close();
    }
}
```

---

## Recomendación

Ejecuta cada programa varias veces con datos diferentes para probar todos los caminos posibles.
