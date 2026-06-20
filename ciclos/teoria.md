# Unidad 5. Ciclos en Java

## Presentación de la unidad

En programación, muchas tareas deben repetirse varias veces.

Por ejemplo:

- Mostrar los números del 1 al 10.
- Pedir notas de varios estudiantes.
- Sumar una lista de valores.
- Validar una contraseña hasta que sea correcta.
- Mostrar una tabla de multiplicar.
- Recorrer un arreglo.

Para resolver estos casos se usan **ciclos**, también llamados **estructuras repetitivas**.

---

## 1. ¿Qué es un ciclo?

Un ciclo es una estructura que permite repetir instrucciones mientras se cumpla una condición o durante un número determinado de veces.

Ejemplo cotidiano:

```text
Mientras tenga tareas pendientes, sigo estudiando.
```

Ejemplo en Java:

```java
while (contador <= 5) {
    System.out.println(contador);
    contador++;
}
```

---

## 2. ¿Para qué sirven los ciclos?

Sirven para evitar repetir código manualmente.

Sin ciclo:

```java
System.out.println(1);
System.out.println(2);
System.out.println(3);
System.out.println(4);
System.out.println(5);
```

Con ciclo:

```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

El ciclo hace el código más corto, ordenado y flexible.

---

## 3. Tipos principales de ciclos en Java

En Java trabajaremos tres ciclos principales:

| Ciclo | Uso principal |
|---|---|
| `while` | Repetir mientras una condición sea verdadera |
| `do-while` | Ejecutar al menos una vez y luego repetir si la condición se cumple |
| `for` | Repetir un número conocido de veces |

---

## 4. Partes importantes de un ciclo

En muchos ciclos aparecen tres elementos:

| Elemento | Explicación |
|---|---|
| Inicialización | Valor inicial de una variable de control |
| Condición | Indica si el ciclo continúa |
| Actualización | Cambia la variable para evitar ciclo infinito |

Ejemplo:

```java
int contador = 1;

while (contador <= 5) {
    System.out.println(contador);
    contador++;
}
```

- Inicialización: `int contador = 1;`
- Condición: `contador <= 5`
- Actualización: `contador++`

---

## 5. Contador

Un contador es una variable que aumenta o disminuye siguiendo un patrón.

Ejemplo:

```java
contador++;
```

Significa:

```text
contador = contador + 1
```

---

## 6. Acumulador

Un acumulador es una variable que guarda una suma progresiva.

Ejemplo:

```java
suma = suma + numero;
```

Si se ingresan varios números, `suma` va acumulando el total.

---

## 7. Ciclo infinito

Un ciclo infinito ocurre cuando la condición nunca se vuelve falsa.

Ejemplo incorrecto:

```java
int contador = 1;

while (contador <= 5) {
    System.out.println(contador);
}
```

El problema es que `contador` nunca cambia.  
Siempre vale 1, por eso la condición siempre será verdadera.

Corrección:

```java
int contador = 1;

while (contador <= 5) {
    System.out.println(contador);
    contador++;
}
```

---

## 8. ¿Cuándo usar `while`?

Se usa `while` cuando no sabemos exactamente cuántas veces se repetirá algo, pero sí sabemos la condición para continuar.

Ejemplo:

```text
Pedir contraseña mientras sea incorrecta.
```

---

## 9. ¿Cuándo usar `do-while`?

Se usa `do-while` cuando queremos que el bloque se ejecute al menos una vez.

Ejemplo:

```text
Mostrar un menú al menos una vez y repetir mientras el usuario no elija salir.
```

---

## 10. ¿Cuándo usar `for`?

Se usa `for` cuando conocemos cuántas veces debe repetirse el ciclo.

Ejemplo:

```text
Mostrar los números del 1 al 10.
```

---

## 11. Comparación rápida

| Situación | Ciclo recomendado |
|---|---|
| Repetir hasta que una clave sea correcta | `while` |
| Mostrar un menú al menos una vez | `do-while` |
| Repetir 10 veces | `for` |
| Recorrer números del 1 al 100 | `for` |
| Pedir datos hasta que el usuario escriba 0 | `while` |
| Validar una opción de menú | `do-while` |

---

## 12. Buenas prácticas

- Inicializar correctamente las variables.
- Verificar que la condición pueda volverse falsa.
- Actualizar el contador dentro del ciclo.
- Usar nombres claros como `contador`, `suma`, `cantidad`, `opcion`.
- No escribir ciclos demasiado largos.
- Probar con pocos datos primero.
- Usar comentarios cuando el ciclo tenga lógica importante.
- Evitar ciclos infinitos.

---

## 13. Resultado de aprendizaje

Al finalizar esta unidad, el estudiante debe poder crear programas en Java que repitan instrucciones usando `while`, `do-while` y `for`, aplicando contadores, acumuladores, validaciones y menús básicos.
