# Encapsulamiento en Java

## 1. ¿Qué es el encapsulamiento?

El encapsulamiento es un principio de la Programación Orientada a Objetos que consiste en proteger los datos internos de una clase.

En Java, normalmente se protegen los atributos usando `private`.

Luego se accede a ellos mediante métodos públicos llamados:

- `getters`
- `setters`

---

## 2. ¿Por qué encapsular?

Encapsular permite:

- Proteger los datos.
- Evitar cambios incorrectos.
- Controlar cómo se modifican los atributos.
- Mejorar la seguridad del código.
- Hacer clases más ordenadas.

---

## 3. Ejemplo sin encapsulamiento

```java
public class Estudiante {
    public String nombre;
    public double notaFinal;
}
```

Uso:

```java
Estudiante estudiante = new Estudiante();
estudiante.notaFinal = 9.8;
```

Problema:

Una nota de 9.8 no es válida si la escala es de 0.0 a 5.0.

---

## 4. Ejemplo con encapsulamiento

```java
public class Estudiante {
    private String nombre;
    private double notaFinal;

    public void setNombre(String nombre) {
        this.nombre = nombre;
    }

    public String getNombre() {
        return nombre;
    }

    public void setNotaFinal(double notaFinal) {
        if (notaFinal >= 0.0 && notaFinal <= 5.0) {
            this.notaFinal = notaFinal;
        } else {
            System.out.println("Nota no válida");
        }
    }

    public double getNotaFinal() {
        return notaFinal;
    }
}
```

---

## 5. ¿Qué hace `private`?

```java
private double notaFinal;
```

Significa que `notaFinal` solo puede usarse directamente dentro de la clase.

Desde otra clase no se puede hacer:

```java
estudiante.notaFinal = 4.2;
```

Se debe usar:

```java
estudiante.setNotaFinal(4.2);
```

---

## 6. Getter

Un getter permite obtener el valor de un atributo.

```java
public double getNotaFinal() {
    return notaFinal;
}
```

---

## 7. Setter

Un setter permite modificar el valor de un atributo.

```java
public void setNotaFinal(double notaFinal) {
    this.notaFinal = notaFinal;
}
```

También puede incluir validaciones.

```java
public void setNotaFinal(double notaFinal) {
    if (notaFinal >= 0.0 && notaFinal <= 5.0) {
        this.notaFinal = notaFinal;
    }
}
```

---

## 8. Clase completa encapsulada

Archivo `Estudiante.java`:

```java
public class Estudiante {
    private String nombre;
    private int edad;
    private double notaFinal;

    public Estudiante(String nombre, int edad, double notaFinal) {
        this.nombre = nombre;
        this.edad = edad;
        setNotaFinal(notaFinal);
    }

    public String getNombre() {
        return nombre;
    }

    public void setNombre(String nombre) {
        this.nombre = nombre;
    }

    public int getEdad() {
        return edad;
    }

    public void setEdad(int edad) {
        if (edad >= 0 && edad <= 120) {
            this.edad = edad;
        } else {
            System.out.println("Edad no válida");
        }
    }

    public double getNotaFinal() {
        return notaFinal;
    }

    public void setNotaFinal(double notaFinal) {
        if (notaFinal >= 0.0 && notaFinal <= 5.0) {
            this.notaFinal = notaFinal;
        } else {
            System.out.println("Nota no válida");
        }
    }

    public boolean aprobo() {
        return notaFinal >= 3.0;
    }

    public void mostrarInformacion() {
        System.out.println("Nombre: " + nombre);
        System.out.println("Edad: " + edad);
        System.out.println("Nota final: " + notaFinal);
        System.out.println("Aprobó: " + aprobo());
    }
}
```

---

## 9. Uso de la clase encapsulada

Archivo `Principal.java`:

```java
public class Principal {
    public static void main(String[] args) {
        Estudiante estudiante = new Estudiante("Ana", 18, 4.2);

        estudiante.mostrarInformacion();

        estudiante.setNotaFinal(6.0);
        estudiante.setNotaFinal(4.8);

        System.out.println("Nueva nota: " + estudiante.getNotaFinal());
    }
}
```

---

## 10. Clase Producto encapsulada

```java
public class Producto {
    private String nombre;
    private double precio;
    private int cantidad;

    public Producto(String nombre, double precio, int cantidad) {
        this.nombre = nombre;
        setPrecio(precio);
        setCantidad(cantidad);
    }

    public String getNombre() {
        return nombre;
    }

    public void setNombre(String nombre) {
        this.nombre = nombre;
    }

    public double getPrecio() {
        return precio;
    }

    public void setPrecio(double precio) {
        if (precio > 0) {
            this.precio = precio;
        } else {
            System.out.println("Precio no válido");
        }
    }

    public int getCantidad() {
        return cantidad;
    }

    public void setCantidad(int cantidad) {
        if (cantidad >= 0) {
            this.cantidad = cantidad;
        } else {
            System.out.println("Cantidad no válida");
        }
    }

    public double calcularTotal() {
        return precio * cantidad;
    }
}
```

---

## 11. Buenas prácticas

- Declarar atributos como `private`.
- Crear getters y setters cuando sean necesarios.
- Validar datos dentro de los setters.
- Evitar modificar atributos directamente.
- Usar métodos para controlar el comportamiento del objeto.
- No exponer información innecesaria.

---

## 12. Conclusión

El encapsulamiento protege los datos de una clase y permite controlar cómo se accede a ellos. Es una práctica fundamental para escribir programas más seguros, organizados y mantenibles.
