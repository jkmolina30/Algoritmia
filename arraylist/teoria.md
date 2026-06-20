# Unidad 9. ArrayList en Java

## Presentación de la unidad

En la unidad anterior se trabajaron los **arreglos**. Los arreglos permiten guardar varios datos del mismo tipo, pero tienen una limitación importante: su tamaño es fijo.

Ejemplo:

```java
double[] notas = new double[5];
```

Ese arreglo solo puede guardar 5 notas. Si después necesitamos guardar más notas, el arreglo no crece automáticamente.

Para resolver este tipo de situaciones, Java ofrece una estructura llamada **ArrayList**.

---

## 1. ¿Qué es un ArrayList?

Un `ArrayList` es una estructura dinámica que permite almacenar varios datos del mismo tipo.

La principal diferencia con un arreglo es que el `ArrayList` puede crecer o disminuir durante la ejecución del programa.

En palabras sencillas:

```text
Un arreglo es una lista con tamaño fijo.
Un ArrayList es una lista que puede crecer o reducirse.
```

---

## 2. ¿Para qué sirve un ArrayList?

Un `ArrayList` sirve cuando no sabemos exactamente cuántos datos vamos a guardar.

Ejemplos:

- Registrar nombres de estudiantes.
- Guardar notas de una cantidad variable de estudiantes.
- Crear una lista de productos.
- Registrar compras.
- Guardar opciones seleccionadas por un usuario.
- Crear listas que pueden cambiar durante el programa.

---

## 3. Diferencia entre arreglo y ArrayList

| Característica | Arreglo | ArrayList |
|---|---|---|
| Tamaño | Fijo | Dinámico |
| Sintaxis | Más simple al inicio | Requiere importar clase |
| Acceso | `notas[i]` | `notas.get(i)` |
| Agregar elementos | No crece automáticamente | Usa `.add()` |
| Eliminar elementos | No es directo | Usa `.remove()` |
| Tamaño | `.length` | `.size()` |

---

## 4. Importar ArrayList

Para usar `ArrayList`, primero se debe importar:

```java
import java.util.ArrayList;
```

Esta línea se escribe al inicio del archivo Java.

---

## 5. Crear un ArrayList

Sintaxis general:

```java
ArrayList<Tipo> nombre = new ArrayList<>();
```

Ejemplos:

```java
ArrayList<String> nombres = new ArrayList<>();
ArrayList<Integer> edades = new ArrayList<>();
ArrayList<Double> notas = new ArrayList<>();
```

---

## 6. Tipos envoltorio

En `ArrayList` no se usan directamente tipos primitivos como `int` o `double`.

Se usan sus clases envoltorio:

| Tipo primitivo | Tipo para ArrayList |
|---|---|
| `int` | `Integer` |
| `double` | `Double` |
| `char` | `Character` |
| `boolean` | `Boolean` |

Ejemplo correcto:

```java
ArrayList<Integer> numeros = new ArrayList<>();
```

Ejemplo incorrecto:

```java
ArrayList<int> numeros = new ArrayList<>();
```

---

## 7. Agregar elementos

Para agregar elementos se usa `.add()`.

```java
ArrayList<String> nombres = new ArrayList<>();

nombres.add("Ana");
nombres.add("Carlos");
nombres.add("María");
```

---

## 8. Obtener un elemento

Para obtener un elemento se usa `.get(indice)`.

```java
System.out.println(nombres.get(0));
```

Esto muestra el primer elemento.

Recordemos que los índices empiezan en 0.

---

## 9. Cambiar un elemento

Para cambiar un valor se usa `.set(indice, nuevoValor)`.

```java
nombres.set(1, "Camila");
```

Esto cambia el elemento de la posición 1.

---

## 10. Eliminar un elemento

Para eliminar se usa `.remove()`.

Eliminar por posición:

```java
nombres.remove(0);
```

Eliminar por valor:

```java
nombres.remove("Ana");
```

---

## 11. Saber el tamaño

Para conocer cuántos elementos tiene un `ArrayList`, se usa `.size()`.

```java
System.out.println(nombres.size());
```

---

## 12. Recorrer un ArrayList con `for`

```java
for (int i = 0; i < nombres.size(); i++) {
    System.out.println(nombres.get(i));
}
```

---

## 13. Recorrer con `for-each`

```java
for (String nombre : nombres) {
    System.out.println(nombre);
}
```

El `for-each` es útil cuando solo necesitamos leer los elementos.

---

## 14. Verificar si contiene un elemento

Para saber si un elemento está en el `ArrayList`, se usa `.contains()`.

```java
if (nombres.contains("Ana")) {
    System.out.println("Ana está registrada");
}
```

---

## 15. Verificar si está vacío

```java
if (nombres.isEmpty()) {
    System.out.println("La lista está vacía");
}
```

---

## 16. Limpiar todos los elementos

```java
nombres.clear();
```

Esto elimina todos los elementos del `ArrayList`.

---

## 17. Ejemplo conceptual

Supongamos que queremos registrar estudiantes, pero no sabemos cuántos se van a ingresar. Con un arreglo tendríamos que definir un tamaño desde el inicio. Con `ArrayList`, podemos agregar estudiantes uno por uno.

```java
ArrayList<String> estudiantes = new ArrayList<>();

estudiantes.add("Ana");
estudiantes.add("Carlos");
estudiantes.add("María");
```

---

## 18. ArrayList y Scanner

También podemos llenar un `ArrayList` con datos ingresados por el usuario.

```java
Scanner entrada = new Scanner(System.in);
ArrayList<String> nombres = new ArrayList<>();

String nombre;

System.out.print("Ingrese un nombre: ");
nombre = entrada.nextLine();

nombres.add(nombre);
```

---

## 19. Buenas prácticas

- Usar `ArrayList` cuando la cantidad de datos puede cambiar.
- Usar nombres claros para las listas.
- Recordar importar `java.util.ArrayList`.
- Usar clases envoltorio como `Integer` y `Double`.
- Usar `.size()` para conocer el tamaño.
- Usar `.get()` para leer un elemento.
- Usar `.add()` para agregar.
- Usar `.remove()` con cuidado.
- Validar posiciones antes de acceder.

---

## 20. Resultado de aprendizaje

Al finalizar esta unidad, el estudiante debe poder crear, llenar, recorrer, modificar, buscar y eliminar elementos en un `ArrayList` usando Java.
