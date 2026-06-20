# JDK, JRE, JVM y Bytecode

## 1. Introducción

Para aprender Java no basta con escribir código. También es importante entender qué ocurre cuando un programa se ejecuta.

En Java intervienen varios conceptos técnicos:

- JDK.
- JRE.
- JVM.
- Compilador.
- Bytecode.

Al inicio pueden parecer términos difíciles, pero se pueden entender con una idea sencilla: Java necesita herramientas para convertir el código que escribe el programador en algo que el computador pueda ejecutar.

---

## 2. Código fuente

El **código fuente** es el programa escrito por el programador.

En Java, los archivos de código fuente tienen extensión:

```text
.java
```

Ejemplo:

```text
HolaMundo.java
```

Contenido del archivo:

```java
public class HolaMundo {
    public static void main(String[] args) {
        System.out.println("Hola mundo");
    }
}
```

Este código todavía no está listo para ser ejecutado directamente por la máquina. Primero debe pasar por un proceso de compilación.

---

## 3. Compilador de Java

El compilador de Java se llama:

```text
javac
```

Su trabajo es revisar el código fuente y convertirlo en **bytecode**.

Ejemplo:

```bash
javac HolaMundo.java
```

Después de ejecutar ese comando, se genera un archivo:

```text
HolaMundo.class
```

---

## 4. ¿Qué es el bytecode?

El **bytecode** es un código intermedio generado por el compilador de Java.

No es exactamente código fuente, porque ya no está escrito como el programa original.  
Tampoco es código de máquina específico para Windows, Linux o macOS.

Es una forma intermedia que puede ser ejecutada por la JVM.

Esquema:

```text
Código fuente Java (.java)
        ↓
Compilador javac
        ↓
Bytecode (.class)
        ↓
JVM
        ↓
Ejecución del programa
```

---

## 5. ¿Qué es la JVM?

JVM significa:

```text
Java Virtual Machine
```

En español:

```text
Máquina Virtual de Java
```

La JVM es la encargada de ejecutar el bytecode.

En palabras sencillas, la JVM funciona como un intermediario entre el programa Java y el sistema operativo.

---

## 6. ¿Por qué la JVM permite que Java sea multiplataforma?

Porque el mismo bytecode puede ejecutarse en diferentes sistemas operativos, siempre que cada uno tenga su propia JVM instalada.

Ejemplo:

```text
Bytecode Java
   ↓        ↓        ↓
JVM Mac   JVM Linux  JVM Windows
   ↓        ↓        ↓
Mac       Linux      Windows
```

El programador no tiene que escribir un programa diferente para cada sistema operativo.

---

## 7. ¿Qué es el JRE?

JRE significa:

```text
Java Runtime Environment
```

En español:

```text
Entorno de Ejecución de Java
```

El JRE contiene lo necesario para ejecutar programas Java.

Incluye:

- JVM.
- Librerías necesarias.
- Archivos de soporte para ejecutar programas.

En palabras sencillas:

```text
JRE = herramientas para ejecutar programas Java
```

---

## 8. ¿Qué es el JDK?

JDK significa:

```text
Java Development Kit
```

En español:

```text
Kit de Desarrollo de Java
```

El JDK contiene lo necesario para desarrollar programas Java.

Incluye:

- Compilador `javac`.
- JVM.
- Librerías.
- Herramientas de desarrollo.
- JRE.

En palabras sencillas:

```text
JDK = herramientas para crear y ejecutar programas Java
```

---

## 9. Diferencia entre JDK, JRE y JVM

| Concepto | Significado | Uso principal |
|---|---|---|
| JVM | Java Virtual Machine | Ejecuta bytecode |
| JRE | Java Runtime Environment | Permite ejecutar programas Java |
| JDK | Java Development Kit | Permite crear, compilar y ejecutar programas Java |

Para este curso se necesita instalar el **JDK**, porque el estudiante va a escribir y compilar programas.

---

## 10. Analogía sencilla

Imaginemos que escribir un programa es como escribir una carta en un idioma.

| Elemento | Analogía |
|---|---|
| Código fuente | Carta escrita por el programador |
| Compilador | Traductor |
| Bytecode | Traducción intermedia |
| JVM | Persona que entiende esa traducción y la ejecuta |
| Sistema operativo | Lugar donde se realiza la acción |

---

## 11. Proceso completo de ejecución

Supongamos que tenemos este archivo:

```text
HolaMundo.java
```

Paso 1: compilar.

```bash
javac HolaMundo.java
```

Resultado:

```text
HolaMundo.class
```

Paso 2: ejecutar.

```bash
java HolaMundo
```

Salida:

```text
Hola mundo
```

---

## 12. Diferencia entre compilar y ejecutar

| Acción | Comando | Qué hace |
|---|---|---|
| Compilar | `javac Archivo.java` | Convierte código fuente en bytecode |
| Ejecutar | `java NombreClase` | Ejecuta el bytecode usando la JVM |

---

## 13. Error común

Si el archivo se llama:

```text
HolaMundo.java
```

Y la clase pública se llama:

```java
public class Saludo {
}
```

Java generará un error.

Cuando una clase es pública, el archivo debe tener el mismo nombre de la clase.

Correcto:

Archivo:

```text
HolaMundo.java
```

Clase:

```java
public class HolaMundo {
}
```

---

## 14. Resumen

Java utiliza un proceso especial:

1. El programador escribe código fuente en un archivo `.java`.
2. El compilador `javac` revisa el código.
3. Si no hay errores, genera bytecode en un archivo `.class`.
4. La JVM ejecuta el bytecode.
5. El programa produce una salida.

Este proceso permite que Java sea multiplataforma.
