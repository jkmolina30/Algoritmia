# Atributos y Métodos en Java

## 1. ¿Qué es un atributo?

Un atributo es una característica de un objeto.

Ejemplo:

Para un estudiante:

```text
nombre
edad
nota final
programa
```

En Java:

```java
String nombre;
int edad;
double notaFinal;
String programa;
```

---

## 2. ¿Qué es un método?

Un método es una acción o comportamiento que puede realizar un objeto.

Ejemplo:

Un estudiante podría:

```text
mostrar información
calcular si aprobó
actualizar nota
```

En Java:

```java
public void mostrarInformacion() {
    System.out.println("Nombre: " + nombre);
}
```

---

## 3. Clase con atributos y método

```java
public class Estudiante {
    String nombre;
    int edad;
    double notaFinal;

    public void mostrarInformacion() {
        System.out.println("Nombre: " + nombre);
        System.out.println("Edad: " + edad);
        System.out.println("Nota final: " + notaFinal);
    }
}
```

---

## 4. Uso de la clase

```java
public class Principal {
    public static void main(String[] args) {
        Estudiante estudiante = new Estudiante();

        estudiante.nombre = "Ana";
        estudiante.edad = 18;
        estudiante.notaFinal = 4.2;

        estudiante.mostrarInformacion();
    }
}
```

---

## 5. Método con retorno

Un método puede devolver un resultado.

```java
public boolean aprobo() {
    return notaFinal >= 3.0;
}
```

Uso:

```java
if (estudiante.aprobo()) {
    System.out.println("Aprobó");
} else {
    System.out.println("Reprobó");
}
```

---

## 6. Clase completa con método de aprobación

```java
public class Estudiante {
    String nombre;
    double notaFinal;

    public boolean aprobo() {
        return notaFinal >= 3.0;
    }

    public void mostrarResultado() {
        System.out.println("Estudiante: " + nombre);
        System.out.println("Nota final: " + notaFinal);

        if (aprobo()) {
            System.out.println("Resultado: Aprobó");
        } else {
            System.out.println("Resultado: Reprobó");
        }
    }
}
```

---

## 7. Método con parámetros

Un método puede recibir datos.

```java
public void actualizarNota(double nuevaNota) {
    notaFinal = nuevaNota;
}
```

Uso:

```java
estudiante.actualizarNota(4.5);
```

---

## 8. Clase Producto con métodos

```java
public class Producto {
    String nombre;
    double precio;
    int cantidad;

    public double calcularTotal() {
        return precio * cantidad;
    }

    public void mostrarInformacion() {
        System.out.println("Producto: " + nombre);
        System.out.println("Precio: " + precio);
        System.out.println("Cantidad: " + cantidad);
        System.out.println("Total: " + calcularTotal());
    }
}
```

Uso:

```java
public class PrincipalProducto {
    public static void main(String[] args) {
        Producto producto = new Producto();

        producto.nombre = "Cuaderno";
        producto.precio = 4500;
        producto.cantidad = 3;

        producto.mostrarInformacion();
    }
}
```

---

## 9. Diferencia entre atributo y variable local

| Atributo | Variable local |
|---|---|
| Pertenece a la clase | Pertenece a un método |
| Puede ser usado por varios métodos de la clase | Solo existe dentro del método |
| Representa una característica del objeto | Sirve para cálculos temporales |

Ejemplo:

```java
public class Producto {
    double precio;
    int cantidad;

    public double calcularTotal() {
        double total = precio * cantidad;
        return total;
    }
}
```

`precio` y `cantidad` son atributos.  
`total` es una variable local.

---

## 10. Buenas prácticas

- Los atributos deben representar características importantes.
- Los métodos deben representar acciones claras.
- Un método debe tener un nombre que indique lo que hace.
- Evitar métodos demasiado largos.
- No repetir código.
- Usar métodos para organizar la lógica.

---

## 11. Ejercicio guiado

Crear una clase `CuentaBancaria` con:

Atributos:

```java
String titular;
double saldo;
```

Métodos:

```java
depositar(double valor)
retirar(double valor)
mostrarSaldo()
```

Validar que no se pueda retirar más dinero del saldo disponible.

---

## 12. Conclusión

Los atributos guardan información del objeto. Los métodos permiten que el objeto realice acciones. Juntos forman la base de la Programación Orientada a Objetos.
