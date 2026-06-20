# Unidad - Variables, Tipos de Datos y Operadores

## Presentación de la unidad

En programación, los datos son la materia prima con la que trabajan los algoritmos.  
Para poder procesar esos datos, necesitamos almacenarlos en **variables**, definir su **tipo de dato** y aplicar **operadores** para realizar cálculos, comparaciones o decisiones lógicas.

Esta unidad es fundamental porque permite pasar de ideas generales como:

```text
Calcular el promedio de tres notas
```

a expresiones más precisas como:

```text
promedio <- (nota1 + nota2 + nota3) / 3
```

o en Java:

```java
promedio = (nota1 + nota2 + nota3) / 3;
```

---

## 1. ¿Qué es una variable?

Una **variable** es un espacio de memoria donde se almacena un dato que puede cambiar durante la ejecución de un algoritmo o programa.

En palabras sencillas, una variable es como una caja con nombre donde se guarda un valor.

Ejemplo:

```text
edad = 18
```

La variable se llama `edad` y guarda el valor `18`.

---

## 2. ¿Por qué se llaman variables?

Se llaman variables porque su valor puede cambiar.

Ejemplo:

```text
contador = 1
contador = 2
contador = 3
```

La misma variable `contador` va tomando diferentes valores.

---

## 3. Variable en PSeInt

En PSeInt primero se define la variable y luego se puede usar.

```pseint
Definir edad Como Entero

edad <- 18
```

Lectura sencilla:

```text
Se crea una variable llamada edad, de tipo Entero, y se guarda el valor 18.
```

---

## 4. Variable en Java

En Java también se debe indicar el tipo de dato.

```java
int edad = 18;
```

Lectura sencilla:

```text
Se crea una variable llamada edad, de tipo entero, y se guarda el valor 18.
```

---

## 5. ¿Qué es una constante?

Una **constante** es un valor que no cambia durante la ejecución del programa.

Ejemplo:

```text
PI = 3.1416
```

En algunos problemas podemos usar constantes para representar valores fijos.

En Java se recomienda usar `final` para declarar constantes.

```java
final double PI = 3.1416;
```

Esto significa que el valor de `PI` no debe cambiar.

---

## 6. Identificadores

Un **identificador** es el nombre que se le da a una variable, constante, clase o método.

Ejemplos de identificadores:

```text
edad
nombre
notaFinal
cantidadEstudiantes
valorProducto
```

---

## 7. Reglas para nombrar variables

### En PSeInt

Se recomienda:

- Usar nombres claros.
- Evitar espacios.
- Evitar tildes y caracteres especiales.
- No iniciar con números.
- No usar palabras reservadas.

Correcto:

```pseint
Definir notaFinal Como Real
Definir cantidadEstudiantes Como Entero
```

Poco recomendado:

```pseint
Definir n Como Real
Definir x Como Entero
```

---

### En Java

En Java se recomienda usar la convención `camelCase`.

Ejemplos correctos:

```java
int edad;
double notaFinal;
String nombreCompleto;
int cantidadEstudiantes;
```

Ejemplos incorrectos o poco recomendados:

```java
int 1edad;
double nota final;
String nombre-completo;
int x;
```

---

## 8. Palabras reservadas

Las **palabras reservadas** son palabras que el lenguaje ya usa para una función especial.  
No deben utilizarse como nombres de variables.

Ejemplos en Java:

```text
class
public
static
void
int
double
if
else
for
while
return
new
```

Incorrecto:

```java
int class = 5;
```

Correcto:

```java
int cantidad = 5;
```

---

## 9. Tipos de datos

Un **tipo de dato** indica qué clase de valor puede guardar una variable.

No es lo mismo guardar un número entero, un decimal, un texto o un valor verdadero/falso.

---

## 10. Tipos de datos básicos en PSeInt

| Tipo en PSeInt | Uso | Ejemplo |
|---|---|---|
| `Entero` | Números sin decimales | `18`, `25`, `100` |
| `Real` | Números con decimales | `3.5`, `4.8`, `12.75` |
| `Caracter` | Texto o caracteres | `"Ana"`, `"Algoritmia"` |
| `Logico` | Verdadero o falso | `Verdadero`, `Falso` |

---

## 11. Tipos de datos básicos en Java

| Tipo en Java | Uso | Ejemplo |
|---|---|---|
| `int` | Números enteros | `int edad = 18;` |
| `double` | Números decimales | `double nota = 4.5;` |
| `char` | Un solo carácter | `char grupo = 'A';` |
| `String` | Texto | `String nombre = "Ana";` |
| `boolean` | Verdadero o falso | `boolean activo = true;` |

---

## 12. Diferencia entre `char` y `String`

En Java, `char` guarda un solo carácter y se escribe con comillas simples.

```java
char letra = 'A';
```

`String` guarda texto y se escribe con comillas dobles.

```java
String nombre = "Ana";
```

Incorrecto:

```java
char letra = "A";
String nombre = 'Ana';
```

---

## 13. Declaración de variables

Declarar una variable significa crearla.

### En PSeInt

```pseint
Definir edad Como Entero
Definir nota Como Real
Definir nombre Como Caracter
```

### En Java

```java
int edad;
double nota;
String nombre;
```

---

## 14. Asignación de valores

Asignar un valor significa guardar un dato en una variable.

### En PSeInt

```pseint
edad <- 18
nota <- 4.5
nombre <- "Ana"
```

### En Java

```java
edad = 18;
nota = 4.5;
nombre = "Ana";
```

---

## 15. Entrada de datos

La entrada de datos permite que el usuario ingrese información.

### En PSeInt

```pseint
Leer nombre
```

### En Java

```java
nombre = entrada.nextLine();
```

---

## 16. Salida de datos

La salida de datos permite mostrar información al usuario.

### En PSeInt

```pseint
Escribir "Hola ", nombre
```

### En Java

```java
System.out.println("Hola " + nombre);
```

---

## 17. Operadores aritméticos

Los operadores aritméticos permiten realizar operaciones matemáticas.

| Operador | Significado | Ejemplo |
|---|---|---|
| `+` | Suma | `a + b` |
| `-` | Resta | `a - b` |
| `*` | Multiplicación | `a * b` |
| `/` | División | `a / b` |
| `%` | Módulo o residuo, en Java | `a % b` |
| `^` | Potencia, en PSeInt | `a ^ b` |

---

## 18. Módulo o residuo

El módulo permite obtener el residuo de una división.

Ejemplo:

```text
10 % 3 = 1
```

Porque 10 dividido entre 3 da 3 y sobra 1.

En Java:

```java
int residuo = 10 % 3;
```

Este operador será muy útil más adelante para saber si un número es par o impar.

---

## 19. Potencias en PSeInt y Java

En PSeInt se puede usar:

```pseint
resultado <- 2 ^ 3
```

En Java no se debe usar `^` para potencias.  
Para potencias se usa:

```java
resultado = Math.pow(2, 3);
```

---

## 20. Operadores relacionales

Los operadores relacionales permiten comparar valores.

El resultado de una comparación es verdadero o falso.

| Operador | Significado | Ejemplo |
|---|---|---|
| `>` | Mayor que | `edad > 18` |
| `<` | Menor que | `edad < 18` |
| `>=` | Mayor o igual que | `nota >= 3.0` |
| `<=` | Menor o igual que | `nota <= 5.0` |
| `==` | Igual que, en Java | `edad == 18` |
| `!=` | Diferente de, en Java | `edad != 18` |

En PSeInt normalmente se usa:

```pseint
Si nota >= 3.0 Entonces
```

En Java:

```java
if (nota >= 3.0) {
}
```

---

## 21. Cuidado con `=` y `==` en Java

En Java:

| Símbolo | Uso |
|---|---|
| `=` | Asignar un valor |
| `==` | Comparar si dos valores son iguales |

Ejemplo de asignación:

```java
edad = 18;
```

Ejemplo de comparación:

```java
edad == 18
```

---

## 22. Operadores lógicos

Los operadores lógicos permiten combinar condiciones.

| Operador en lógica | Java | Significado |
|---|---|---|
| Y | && | Ambas condiciones deben cumplirse |
| O | || | Al menos una condición debe cumplirse |
| NO | ! | Niega una condición |

Ejemplo:

```java
edad >= 18 && edad <= 25
```

Significa:

```text
La edad debe ser mayor o igual a 18 y menor o igual a 25.
```

---

## 23. Precedencia de operadores

La precedencia indica qué operación se resuelve primero.

Orden básico:

| Prioridad | Operación |
|---:|---|
| 1 | Paréntesis |
| 2 | Multiplicación, división y módulo |
| 3 | Suma y resta |
| 4 | Operadores relacionales |
| 5 | Operadores lógicos |

Ejemplo:

```text
resultado = 8 + 4 * 2
```

Primero:

```text
4 * 2 = 8
```

Luego:

```text
8 + 8 = 16
```

Resultado:

```text
16
```

---

## 24. Uso de paréntesis

Los paréntesis ayudan a evitar errores.

Incorrecto para promedio:

```java
promedio = nota1 + nota2 + nota3 / 3;
```

Correcto:

```java
promedio = (nota1 + nota2 + nota3) / 3;
```

---

## 25. Expresiones

Una expresión combina variables, valores y operadores.

Ejemplo:

```java
total = precio * cantidad + domicilio;
```

Esta expresión calcula un total usando variables y operadores.

---

## 26. Buenas prácticas

- Usar nombres claros para las variables.
- Declarar variables antes de usarlas.
- Escoger el tipo de dato adecuado.
- Usar paréntesis cuando una fórmula pueda generar duda.
- No usar palabras reservadas como nombres.
- En Java, recordar el punto y coma.
- En Java, diferenciar entre `=` y `==`.
- Hacer prueba de escritorio antes de ejecutar.

---

## 27. Resultado de aprendizaje

Al finalizar esta unidad, el estudiante debe poder declarar variables, identificar tipos de datos, usar operadores aritméticos, relacionales y lógicos, construir expresiones y aplicar correctamente la jerarquía de operaciones en PSeInt y Java.
