# Constructores en Java

## 1. ¿Qué es un constructor?

Un constructor es un método especial que se ejecuta cuando se crea un objeto.

Sirve para inicializar los atributos del objeto.

Ejemplo:

```java
Estudiante estudiante = new Estudiante("Ana", 18, 4.2);
```

En ese momento se llama al constructor de la clase `Estudiante`.

---

## 2. Características de un constructor

Un constructor:

- Tiene el mismo nombre de la clase.
- No tiene tipo de retorno.
- Se ejecuta al crear un objeto.
- Puede recibir parámetros.
- Sirve para inicializar atributos.

---

## 3. Constructor vacío

```java
public class Estudiante {
    String nombre;
    int edad;

    public Estudiante() {
    }
}
```

Este constructor no recibe parámetros.

Uso:

```java
Estudiante estudiante = new Estudiante();
```

---

## 4. Constructor con parámetros

```java
public class Estudiante {
    String nombre;
    int edad;
    double notaFinal;

    public Estudiante(String nombre, int edad, double notaFinal) {
        this.nombre = nombre;
        this.edad = edad;
        this.notaFinal = notaFinal;
    }
}
```

Uso:

```java
Estudiante estudiante = new Estudiante("Ana", 18, 4.2);
```

---

## 5. ¿Qué significa `this`?

La palabra `this` hace referencia al objeto actual.

Ejemplo:

```java
this.nombre = nombre;
```

El primer `nombre` es el atributo del objeto.  
El segundo `nombre` es el parámetro recibido.

Lectura sencilla:

```text
El atributo nombre del objeto recibe el valor del parámetro nombre.
```

---

## 6. Clase completa con constructor

Archivo `Estudiante.java`:

```java
public class Estudiante {
    String nombre;
    int edad;
    double notaFinal;

    public Estudiante(String nombre, int edad, double notaFinal) {
        this.nombre = nombre;
        this.edad = edad;
        this.notaFinal = notaFinal;
    }

    public void mostrarInformacion() {
        System.out.println("Nombre: " + nombre);
        System.out.println("Edad: " + edad);
        System.out.println("Nota final: " + notaFinal);
    }
}
```

Archivo `Principal.java`:

```java
public class Principal {
    public static void main(String[] args) {
        Estudiante estudiante = new Estudiante("Ana", 18, 4.2);

        estudiante.mostrarInformacion();
    }
}
```

---

## 7. Varios constructores

Una clase puede tener más de un constructor, siempre que tengan parámetros diferentes.

```java
public class Producto {
    String nombre;
    double precio;
    int cantidad;

    public Producto() {
    }

    public Producto(String nombre, double precio, int cantidad) {
        this.nombre = nombre;
        this.precio = precio;
        this.cantidad = cantidad;
    }
}
```

Esto se llama sobrecarga de constructores.

---

## 8. Constructor en clase Producto

```java
public class Producto {
    String nombre;
    double precio;
    int cantidad;

    public Producto(String nombre, double precio, int cantidad) {
        this.nombre = nombre;
        this.precio = precio;
        this.cantidad = cantidad;
    }

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
        Producto producto = new Producto("Cuaderno", 4500, 3);

        producto.mostrarInformacion();
    }
}
```

---

## 9. Buenas prácticas

- Usar constructores para inicializar objetos.
- Usar `this` cuando el parámetro se llama igual que el atributo.
- Evitar crear objetos vacíos si ya se conocen los datos.
- Validar valores si es necesario.
- Mantener constructores claros y cortos.

---

## 10. Ejercicio guiado

Crear una clase `Libro` con:

Atributos:

```java
String titulo;
String autor;
int paginas;
```

Constructor:

```java
public Libro(String titulo, String autor, int paginas)
```

Método:

```java
mostrarInformacion()
```

Luego crear dos objetos `Libro` desde una clase `Principal`.

---

## 11. Conclusión

Los constructores permiten crear objetos con datos iniciales. Esto ayuda a evitar objetos incompletos y mejora la organización del código.
