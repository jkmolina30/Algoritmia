# Representación de la Información

## 1. Introducción

Los computadores trabajan con información, pero internamente no la manejan como lo hacemos las personas.

Una persona puede leer:

```text
Hola
```

Un computador representa esa información mediante códigos internos formados por valores binarios.

Por eso, es importante comprender que todo lo que vemos en un computador, como textos, imágenes, sonidos o videos, internamente se representa mediante datos.

---

## 2. ¿Qué significa representar información?

Representar información significa convertir datos de la realidad a una forma que el computador pueda almacenar, procesar y transmitir.

Ejemplos:

| Información real | Representación en el computador        |
| ---------------- | -------------------------------------- |
| Una letra        | Código numérico                        |
| Un número        | Valor binario                          |
| Una imagen       | Conjunto de píxeles                    |
| Un sonido        | Muestras digitales                     |
| Un video         | Secuencia de imágenes y sonido         |
| Un documento     | Archivo con texto, formato y metadatos |

---

## 3. Sistema binario

El sistema binario es un sistema de numeración que utiliza solo dos símbolos:

```text
0 y 1
```

Los computadores usan el sistema binario porque internamente trabajan con señales eléctricas que pueden interpretarse como dos estados:

| Estado lógico | Interpretación        |
| ------------- | --------------------- |
| 0             | Apagado o falso       |
| 1             | Encendido o verdadero |

---

## 4. Bit

Un **bit** es la unidad mínima de información en computación.

Un bit puede tener uno de dos valores:

```text
0
```

o

```text
1
```

Ejemplo:

```text
1 bit = puede representar 0 o 1
```

---

## 5. Byte

Un **byte** está formado por 8 bits.

```text
1 byte = 8 bits
```

Los bytes se usan para representar caracteres, números y otros datos.

Ejemplo de byte:

```text
01000001
```

Este valor puede representar una letra, dependiendo del sistema de codificación utilizado.

---

## 6. Unidades de almacenamiento

La información digital se mide usando unidades como:

| Unidad   | Equivalencia aproximada |
| -------- | ----------------------- |
| Bit      | Unidad mínima           |
| Byte     | 8 bits                  |
| Kilobyte | 1024 bytes              |
| Megabyte | 1024 kilobytes          |
| Gigabyte | 1024 megabytes          |
| Terabyte | 1024 gigabytes          |

### Ejemplo cotidiano

* Un archivo de texto puede ocupar pocos kilobytes.
* Una foto puede ocupar varios megabytes.
* Un video puede ocupar cientos de megabytes o varios gigabytes.
* Un disco duro puede tener capacidad de varios terabytes.

---

## 7. Representación de números

Los números también se representan internamente usando binario.

Ejemplo:

| Número decimal | Representación binaria |
| -------------: | ---------------------: |
|              0 |                      0 |
|              1 |                      1 |
|              2 |                     10 |
|              3 |                     11 |
|              4 |                    100 |
|              5 |                    101 |
|              6 |                    110 |
|              7 |                    111 |
|              8 |                   1000 |

No es necesario que el estudiante domine conversiones complejas en esta unidad, pero sí debe comprender que el computador representa los números usando códigos internos.

---

## 8. Representación de texto

El texto se representa asignando un código numérico a cada carácter.

Por ejemplo, una letra como:

```text
A
```

puede representarse mediante un número interno.

Luego ese número puede almacenarse en binario.

### Caracteres

Un carácter puede ser:

* Una letra.
* Un número escrito como símbolo.
* Un signo de puntuación.
* Un espacio.
* Un símbolo especial.

Ejemplos:

```text
A
b
7
?
@
```

---

## 9. Cadenas de texto

Una cadena de texto es una secuencia de caracteres.

Ejemplo:

```text
Hola
```

Está formada por los caracteres:

```text
H
o
l
a
```

En Java, las cadenas se representan con el tipo `String`.

Ejemplo:

```java
String nombre = "Ana";
```

---

## 10. Representación de imágenes

Una imagen digital está formada por pequeños puntos llamados píxeles.

Cada píxel tiene información de color.

Mientras más píxeles tenga una imagen, mayor puede ser su calidad, pero también ocupará más espacio.

### Ejemplo

Una imagen de 1000 x 1000 píxeles tiene:

```text
1.000.000 de píxeles
```

Cada píxel necesita información para representar su color.

---

## 11. Representación de sonido

El sonido digital se representa tomando muestras del sonido real.

Cada muestra se convierte en datos numéricos.

Por eso, un archivo de audio es una representación digital de ondas sonoras.

Ejemplos de archivos de sonido:

* `.mp3`
* `.wav`
* `.aac`

---

## 12. Representación de video

Un video combina imágenes y sonido.

Un video está formado por muchas imágenes mostradas rápidamente una después de otra.

Cada una de esas imágenes se llama fotograma.

Además, el video puede incluir audio.

Por eso los videos suelen ocupar más espacio que una imagen o un archivo de texto.

---

## 13. Archivos

Un archivo es una unidad de información almacenada en un dispositivo.

Ejemplos:

| Tipo de archivo | Ejemplo         |
| --------------- | --------------- |
| Texto           | `documento.txt` |
| Java            | `Programa.java` |
| Imagen          | `foto.png`      |
| Audio           | `cancion.mp3`   |
| Video           | `clase.mp4`     |
| PDF             | `guia.pdf`      |

---

## 14. Extensiones de archivo

La extensión ayuda a identificar el tipo de archivo.

Ejemplos:

| Extensión | Tipo de archivo           |
| --------- | ------------------------- |
| `.txt`    | Texto plano               |
| `.java`   | Código fuente Java        |
| `.class`  | Archivo compilado de Java |
| `.pdf`    | Documento PDF             |
| `.png`    | Imagen                    |
| `.mp3`    | Audio                     |
| `.mp4`    | Video                     |
| `.md`     | Archivo Markdown          |

En este repositorio se usarán muchos archivos `.md`, porque GitHub permite mostrarlos como documentos organizados.

---

## 15. Datos en programación

En programación, los datos se almacenan en variables.

Ejemplo en Java:

```java
int edad = 18;
double nota = 4.5;
String nombre = "Carlos";
boolean aprobado = true;
```

Cada variable tiene un tipo de dato.

El tipo de dato indica qué clase de información puede almacenar.

---

## 16. Tipos de datos básicos

| Tipo en Java | Uso               | Ejemplo                  |
| ------------ | ----------------- | ------------------------ |
| `int`        | Números enteros   | `int edad = 18;`         |
| `double`     | Números decimales | `double nota = 4.5;`     |
| `char`       | Un solo carácter  | `char letra = 'A';`      |
| `String`     | Texto             | `String nombre = "Ana";` |
| `boolean`    | Verdadero o falso | `boolean activo = true;` |

Estos tipos se estudiarán con más profundidad en la unidad de variables, tipos de datos y operadores.

---

## 17. Diferencia entre dato y tipo de dato

| Elemento     | Ejemplo | Explicación                     |
| ------------ | ------- | ------------------------------- |
| Dato         | `18`    | Valor específico                |
| Tipo de dato | `int`   | Indica que el valor es entero   |
| Variable     | `edad`  | Espacio donde se guarda el dato |

Ejemplo completo:

```java
int edad = 18;
```

Lectura sencilla:

```text
Se crea una variable llamada edad, de tipo entero, y se guarda el valor 18.
```

---

## 18. ¿Por qué esto es importante para programar?

Porque al programar se debe indicar correctamente qué tipo de dato se va a usar.

No es lo mismo guardar:

```text
18
```

que guardar:

```text
"18"
```

El primero puede ser un número para hacer operaciones matemáticas.

El segundo puede ser texto.

Ejemplo:

```java
int numero = 18;
String texto = "18";
```

Con `numero` se pueden hacer operaciones matemáticas.

Con `texto` se trabaja como cadena de caracteres.

---

## 19. Resumen

El computador representa toda la información usando datos digitales. Internamente trabaja con valores binarios, pero los lenguajes de programación permiten usar tipos de datos más comprensibles como números, textos y valores booleanos. Comprender cómo se representa la información ayuda a entender por qué en programación debemos declarar correctamente las variables y los tipos de datos.

---
