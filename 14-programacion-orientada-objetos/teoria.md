# Unidad 12. Programación Orientada a Objetos en Java

## Presentación de la unidad

Hasta este momento se han trabajado programas en Java usando variables, condicionales, ciclos, arreglos, matrices, `ArrayList`, métodos, búsqueda y ordenamiento.

Ahora se inicia un tema central en Java: la **Programación Orientada a Objetos**, también conocida como **POO**.

Java es un lenguaje orientado a objetos. Esto significa que permite construir programas organizados a partir de **clases** y **objetos**.

---

## 1. ¿Qué es la Programación Orientada a Objetos?

La Programación Orientada a Objetos es una forma de programar que permite representar elementos del mundo real o del problema mediante objetos.

Un objeto puede representar, por ejemplo:

- Un estudiante.
- Un docente.
- Una asignatura.
- Un producto.
- Una cuenta bancaria.
- Un vehículo.
- Un libro.
- Una mascota.
- Una factura.

Cada objeto puede tener:

- Características.
- Comportamientos.

---

## 2. Ejemplo cotidiano

Pensemos en un estudiante.

Un estudiante puede tener características como:

```text
nombre
edad
código
programa
nota final
```

También puede tener comportamientos como:

```text
estudiar
presentar examen
calcular promedio
mostrar información
```

En programación, esas características se representan con **atributos** y esos comportamientos se representan con **métodos**.

---

## 3. Clase y objeto

Estos dos conceptos son fundamentales.

| Concepto | Explicación |
|---|---|
| Clase | Molde, plantilla o diseño |
| Objeto | Elemento creado a partir de una clase |

Ejemplo:

```text
Clase: Estudiante
Objeto 1: Ana
Objeto 2: Carlos
Objeto 3: María
```

La clase define qué datos y métodos tendrá un estudiante.  
Cada objeto representa un estudiante específico.

---

## 4. Analogía sencilla

Una clase es como un plano de una casa.  
Un objeto es una casa construida a partir de ese plano.

```text
Clase = plano
Objeto = casa construida
```

Otra analogía:

```text
Clase = molde para galletas
Objeto = cada galleta creada con ese molde
```

---

## 5. Primera clase en Java

```java
public class Estudiante {
    String nombre;
    int edad;
    double notaFinal;
}
```

Esta clase se llama `Estudiante`.

Tiene tres atributos:

```java
String nombre;
int edad;
double notaFinal;
```

---

## 6. Crear un objeto

Para crear un objeto se usa `new`.

```java
Estudiante estudiante1 = new Estudiante();
```

Lectura sencilla:

```text
Se crea un objeto llamado estudiante1 a partir de la clase Estudiante.
```

---

## 7. Asignar valores a un objeto

```java
estudiante1.nombre = "Ana";
estudiante1.edad = 18;
estudiante1.notaFinal = 4.2;
```

---

## 8. Mostrar datos de un objeto

```java
System.out.println("Nombre: " + estudiante1.nombre);
System.out.println("Edad: " + estudiante1.edad);
System.out.println("Nota final: " + estudiante1.notaFinal);
```

---

## 9. Métodos dentro de una clase

Un método representa una acción o comportamiento.

```java
public void mostrarInformacion() {
    System.out.println("Nombre: " + nombre);
    System.out.println("Edad: " + edad);
    System.out.println("Nota final: " + notaFinal);
}
```

Este método muestra la información del estudiante.

---

## 10. Clase completa básica

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

## 11. Usar la clase desde otro archivo

Archivo `Principal.java`:

```java
public class Principal {
    public static void main(String[] args) {
        Estudiante estudiante1 = new Estudiante();

        estudiante1.nombre = "Ana";
        estudiante1.edad = 18;
        estudiante1.notaFinal = 4.2;

        estudiante1.mostrarInformacion();
    }
}
```

---

## 12. ¿Por qué usar POO?

La POO permite:

- Organizar mejor el código.
- Representar entidades reales.
- Reutilizar código.
- Separar responsabilidades.
- Crear programas más fáciles de mantener.
- Trabajar con proyectos más grandes.
- Preparar al estudiante para desarrollo profesional.

---

## 13. Principios básicos de la POO

Los principios más conocidos son:

| Principio | Explicación inicial |
|---|---|
| Abstracción | Representar lo esencial de un objeto |
| Encapsulamiento | Proteger los datos internos |
| Herencia | Crear clases a partir de otras |
| Polimorfismo | Permitir diferentes comportamientos con una misma estructura |

En esta unidad se trabajará principalmente:

- Clases.
- Objetos.
- Atributos.
- Métodos.
- Constructores.
- Encapsulamiento.

Herencia y polimorfismo pueden trabajarse más adelante, cuando el estudiante domine mejor la base.

---

## 14. Abstracción

La abstracción consiste en identificar las características más importantes de un objeto para un problema.

Ejemplo:

Para un sistema académico, de un estudiante nos interesa:

```text
nombre
código
programa
nota final
```

Quizá no sea necesario registrar:

```text
color favorito
comida favorita
estatura
```

La abstracción ayuda a elegir qué información es relevante.

---

## 15. Encapsulamiento

El encapsulamiento consiste en proteger los atributos de una clase y controlar el acceso a ellos.

En Java se usa normalmente:

```java
private
```

para proteger atributos.

Ejemplo:

```java
private String nombre;
private double notaFinal;
```

Luego se usan métodos `get` y `set` para acceder o modificar esos valores.

---

## 16. Constructor

Un constructor es un método especial que se ejecuta cuando se crea un objeto.

Sirve para inicializar los atributos.

Ejemplo:

```java
public Estudiante(String nombre, int edad, double notaFinal) {
    this.nombre = nombre;
    this.edad = edad;
    this.notaFinal = notaFinal;
}
```

---

## 17. `this`

La palabra `this` se usa para referirse al objeto actual.

Ejemplo:

```java
this.nombre = nombre;
```

Significa:

```text
El atributo nombre del objeto recibe el valor del parámetro nombre.
```

---

## 18. Comparación entre programación estructurada y POO

| Programación estructurada | Programación orientada a objetos |
|---|---|
| Se centra en instrucciones y métodos | Se centra en clases y objetos |
| El programa suele organizarse por procesos | El programa se organiza por entidades |
| Es útil para problemas pequeños | Es útil para proyectos medianos y grandes |
| Usa variables y funciones | Usa atributos y métodos |

---

## 19. Buenas prácticas iniciales

- Nombrar clases con mayúscula inicial: `Estudiante`.
- Nombrar atributos con minúscula inicial: `nombre`.
- Usar nombres claros.
- Crear una clase por archivo.
- Proteger atributos con `private`.
- Usar constructores.
- Usar métodos para acciones.
- No escribir toda la lógica en `main`.
- Mantener las clases ordenadas.

---

## 20. Resultado de aprendizaje

Al finalizar esta unidad, el estudiante debe poder crear clases, instanciar objetos, definir atributos y métodos, usar constructores y aplicar encapsulamiento básico en Java.
