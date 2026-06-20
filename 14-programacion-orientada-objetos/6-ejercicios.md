# Ejercicios: Programación Orientada a Objetos en Java

## Instrucciones generales

Para cada ejercicio entregar:

1. Código Java.
2. Clase principal para probar objetos.
3. Explicación breve.
4. Evidencia de ejecución si el docente lo solicita.

---

# Nivel 1. Clases y objetos

## Ejercicio 1

Crear una clase `Estudiante` con los atributos:

```java
String nombre;
int edad;
String programa;
```

Crear un objeto y mostrar sus datos.

---

## Ejercicio 2

Crear una clase `Producto` con:

```java
String nombre;
double precio;
int cantidad;
```

Crear un objeto y calcular el total.

---

## Ejercicio 3

Crear una clase `Libro` con:

```java
String titulo;
String autor;
int paginas;
```

Crear dos objetos y mostrar sus datos.

---

## Ejercicio 4

Crear una clase `Mascota` con:

```java
String nombre;
String especie;
int edad;
```

Crear tres objetos.

---

## Ejercicio 5

Crear una clase `Asignatura` con:

```java
String nombre;
int creditos;
String docente;
```

---

# Nivel 2. Atributos y métodos

## Ejercicio 6

Agregar a la clase `Estudiante` un método `mostrarInformacion()`.

---

## Ejercicio 7

Agregar a la clase `Producto` un método `calcularTotal()`.

---

## Ejercicio 8

Crear una clase `CuentaBancaria` con:

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

---

## Ejercicio 9

Crear una clase `Rectangulo` con atributos `base` y `altura`. Agregar métodos para calcular área y perímetro.

---

## Ejercicio 10

Crear una clase `Circulo` con atributo `radio`. Agregar método para calcular área.

---

# Nivel 3. Constructores

## Ejercicio 11

Agregar constructor a la clase `Estudiante`.

---

## Ejercicio 12

Agregar constructor a la clase `Producto`.

---

## Ejercicio 13

Crear una clase `Empleado` con constructor y método para calcular salario.

---

## Ejercicio 14

Crear una clase `Vehiculo` con constructor y método `mostrarInformacion()`.

---

## Ejercicio 15

Crear una clase `Nota` con atributos `corte1`, `corte2`, `corte3` y método para calcular definitiva.

---

# Nivel 4. Encapsulamiento

## Ejercicio 16

Encapsular la clase `Estudiante` usando atributos `private`, getters y setters.

---

## Ejercicio 17

Validar en `setNotaFinal` que la nota esté entre 0.0 y 5.0.

---

## Ejercicio 18

Encapsular la clase `Producto` y validar que el precio sea mayor que cero.

---

## Ejercicio 19

Encapsular la clase `CuentaBancaria` y evitar retirar más dinero del saldo disponible.

---

## Ejercicio 20

Crear una clase `Persona` con atributos privados, constructor, getters y setters.

---

# Nivel 5. Aplicados

## Ejercicio 21

Crear un programa que registre 5 estudiantes usando un arreglo de objetos `Estudiante[]`.

---

## Ejercicio 22

Crear un programa que registre productos usando `ArrayList<Producto>`.

---

## Ejercicio 23

Crear una clase `Curso` que tenga:

```java
String nombreCurso;
ArrayList<Estudiante> estudiantes;
```

Agregar métodos para:

- Agregar estudiante.
- Mostrar estudiantes.
- Calcular promedio del grupo.

---

## Ejercicio 24

Crear una clase `Factura` con una lista de productos y calcular el total.

---

## Ejercicio 25

Crear un sistema simple de biblioteca con clases:

```java
Libro
Usuario
Prestamo
```

---

# Reto integrador

## Sistema académico básico orientado a objetos

Crear un programa en Java con las siguientes clases:

```text
Estudiante
Asignatura
RegistroNota
Principal
```

La clase `Estudiante` debe tener:

- nombre
- código
- programa

La clase `Asignatura` debe tener:

- nombre
- créditos
- docente

La clase `RegistroNota` debe tener:

- estudiante
- asignatura
- corte1
- corte2
- corte3

Métodos:

- calcularDefinitiva()
- determinarResultado()
- mostrarResumen()

Reglas:

```text
definitiva = corte1 * 0.30 + corte2 * 0.30 + corte3 * 0.40
Aprueba si definitiva >= 3.0
```

---

## Criterios de revisión

| Criterio | Descripción |
|---|---|
| Clases | Crea clases coherentes |
| Objetos | Instancia objetos correctamente |
| Atributos | Usa atributos adecuados |
| Métodos | Define comportamientos claros |
| Constructores | Inicializa objetos |
| Encapsulamiento | Usa private, getters y setters |
| Organización | Separa clases en archivos |
| Explicación | Puede explicar el diseño |
