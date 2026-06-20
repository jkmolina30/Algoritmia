# Ciclo `for` en Java

## 1. ¿Qué es el ciclo `for`?

El ciclo `for` permite repetir instrucciones un número determinado de veces.

Se usa principalmente cuando sabemos cuántas repeticiones se necesitan.

Ejemplo:

```text
Mostrar los números del 1 al 10.
```

---

## 2. Sintaxis

```java
for (inicializacion; condicion; actualizacion) {
    // instrucciones
}
```

---

## 3. Ejemplo básico

Mostrar los números del 1 al 5.

```java
public class NumerosFor {
    public static void main(String[] args) {
        for (int i = 1; i <= 5; i++) {
            System.out.println(i);
        }
    }
}
```

---

## 4. Explicación del ciclo

```java
for (int i = 1; i <= 5; i++)
```

Tiene tres partes:

| Parte | Explicación |
|---|---|
| `int i = 1` | El contador inicia en 1 |
| `i <= 5` | El ciclo se repite mientras `i` sea menor o igual a 5 |
| `i++` | En cada repetición, `i` aumenta en 1 |

---

## 5. Prueba de escritorio

| Iteración | i | Condición `i <= 5` | Salida |
|---:|---:|---|---:|
| 1 | 1 | true | 1 |
| 2 | 2 | true | 2 |
| 3 | 3 | true | 3 |
| 4 | 4 | true | 4 |
| 5 | 5 | true | 5 |
| 6 | 6 | false | - |

---

## 6. Ejemplo: tabla de multiplicar

```java
import java.util.Scanner;

public class TablaMultiplicar {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int numero;

        System.out.print("Ingrese un número: ");
        numero = entrada.nextInt();

        for (int i = 1; i <= 10; i++) {
            System.out.println(numero + " x " + i + " = " + (numero * i));
        }

        entrada.close();
    }
}
```

---

## 7. Ejemplo: sumar números del 1 al 100

```java
public class SumaUnoACien {
    public static void main(String[] args) {
        int suma = 0;

        for (int i = 1; i <= 100; i++) {
            suma = suma + i;
        }

        System.out.println("La suma es: " + suma);
    }
}
```

---

## 8. Ejemplo: promedio de varias notas

```java
import java.util.Scanner;

public class PromedioVariasNotas {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int cantidadNotas;
        double nota;
        double suma = 0;
        double promedio;

        System.out.print("Ingrese la cantidad de notas: ");
        cantidadNotas = entrada.nextInt();

        for (int i = 1; i <= cantidadNotas; i++) {
            System.out.print("Ingrese la nota " + i + ": ");
            nota = entrada.nextDouble();

            suma = suma + nota;
        }

        promedio = suma / cantidadNotas;

        System.out.println("El promedio es: " + promedio);

        entrada.close();
    }
}
```

---

## 9. Ciclo descendente

También se puede contar hacia atrás.

```java
public class CuentaRegresiva {
    public static void main(String[] args) {
        for (int i = 10; i >= 1; i--) {
            System.out.println(i);
        }

        System.out.println("Fin");
    }
}
```

---

## 10. ¿Cuándo usar `for`?

Usa `for` cuando:

- Sabes cuántas veces se repetirá el ciclo.
- Necesitas contar.
- Quieres recorrer una secuencia.
- Vas a trabajar con tablas de multiplicar.
- Vas a pedir una cantidad conocida de datos.
- Más adelante, cuando recorras arreglos.

---

## 11. Errores comunes

### Error 1. Condición incorrecta

```java
for (int i = 1; i >= 10; i++) {
    System.out.println(i);
}
```

El ciclo no se ejecuta porque `1 >= 10` es falso.

---

### Error 2. Actualización incorrecta

```java
for (int i = 1; i <= 10; i--) {
    System.out.println(i);
}
```

Esto puede generar ciclo infinito porque `i` disminuye y nunca llega a ser mayor que 10.

---

## 12. Ejercicios rápidos

1. Mostrar los números del 1 al 20.
2. Mostrar los números pares del 2 al 50.
3. Mostrar una tabla de multiplicar.
4. Sumar los números del 1 al 100.
5. Leer 5 notas y calcular el promedio.
