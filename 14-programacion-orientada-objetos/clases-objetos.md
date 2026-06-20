# Clases y Objetos en Java

## 1. ¿Qué es una clase?

Una clase es una plantilla o molde que define cómo será un objeto.

La clase indica:

- Qué atributos tendrá.
- Qué métodos podrá ejecutar.
- Cómo se construirá el objeto.

Ejemplo:

```java
public class Estudiante {
    String nombre;
    int edad;
}
```

Esta clase indica que un estudiante tendrá un nombre y una edad.

---

## 2. ¿Qué es un objeto?

Un objeto es una instancia de una clase.

En palabras sencillas:

```text
La clase es el molde.
El objeto es el elemento creado con ese molde.
```

Ejemplo:

```java
Estudiante estudiante1 = new Estudiante();
```

Aquí `estudiante1` es un objeto creado a partir de la clase `Estudiante`.

---

## 3. Archivo de clase

En Java, si una clase es pública, el archivo debe llamarse igual.

Archivo:

```text
Estudiante.java
```

Contenido:

```java
public class Estudiante {
    String nombre;
    int edad;
}
```

---

## 4. Crear una clase Estudiante

Archivo `Estudiante.java`:

```java
public class Estudiante {
    String nombre;
    int edad;
    String programa;
}
```

Esta clase tiene tres atributos:

- `nombre`
- `edad`
- `programa`

---

## 5. Crear objetos de la clase

Archivo `Principal.java`:

```java
public class Principal {
    public static void main(String[] args) {
        Estudiante estudiante1 = new Estudiante();
        Estudiante estudiante2 = new Estudiante();

        estudiante1.nombre = "Ana";
        estudiante1.edad = 18;
        estudiante1.programa = "Ingeniería de Sistemas";

        estudiante2.nombre = "Carlos";
        estudiante2.edad = 20;
        estudiante2.programa = "Ingeniería de Sistemas";

        System.out.println(estudiante1.nombre);
        System.out.println(estudiante2.nombre);
    }
}
```

---

## 6. Explicación

```java
Estudiante estudiante1 = new Estudiante();
```

Crea un objeto llamado `estudiante1`.

```java
estudiante1.nombre = "Ana";
```

Asigna el valor `"Ana"` al atributo `nombre` del objeto `estudiante1`.

Cada objeto tiene sus propios valores.

---

## 7. Múltiples objetos

Si creamos varios objetos, cada uno puede tener información diferente.

```java
Estudiante e1 = new Estudiante();
Estudiante e2 = new Estudiante();
Estudiante e3 = new Estudiante();
```

Aunque todos pertenecen a la clase `Estudiante`, cada uno representa un estudiante diferente.

---

## 8. Clase Producto

Archivo `Producto.java`:

```java
public class Producto {
    String nombre;
    double precio;
    int cantidad;
}
```

Archivo `PrincipalProducto.java`:

```java
public class PrincipalProducto {
    public static void main(String[] args) {
        Producto producto1 = new Producto();

        producto1.nombre = "Cuaderno";
        producto1.precio = 4500;
        producto1.cantidad = 3;

        double total = producto1.precio * producto1.cantidad;

        System.out.println("Producto: " + producto1.nombre);
        System.out.println("Total: " + total);
    }
}
```

---

## 9. Clase Libro

```java
public class Libro {
    String titulo;
    String autor;
    int paginas;
}
```

Uso:

```java
public class PrincipalLibro {
    public static void main(String[] args) {
        Libro libro = new Libro();

        libro.titulo = "Fundamentos de Programación";
        libro.autor = "Joyanes Aguilar";
        libro.paginas = 500;

        System.out.println("Título: " + libro.titulo);
        System.out.println("Autor: " + libro.autor);
        System.out.println("Páginas: " + libro.paginas);
    }
}
```

---

## 10. Buenas prácticas

- Las clases deben tener nombres claros.
- El nombre de la clase inicia con mayúscula.
- Cada clase debe representar una entidad.
- Un objeto debe tener datos coherentes.
- Evitar nombres como `Clase1`, `Objeto`, `Datos`.

Ejemplos recomendados:

```text
Estudiante
Producto
Libro
CuentaBancaria
Asignatura
```

---

## 11. Ejercicio guiado

Crear una clase `Mascota` con estos atributos:

```java
String nombre;
String especie;
int edad;
```

Luego crear un objeto y mostrar sus datos.

---

## 12. Conclusión

Las clases y objetos permiten organizar el código de forma más cercana a la realidad. En lugar de trabajar con muchas variables sueltas, se agrupan datos relacionados dentro de objetos.
