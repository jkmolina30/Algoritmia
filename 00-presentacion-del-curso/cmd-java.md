**Paso 1: Abrir el CMD**
Presionar las teclas Windows + R.
Escribir cmd y presionar Enter.

**Paso 2: Ubicarse en la carpeta donde se guardará el programa**
Por ejemplo, si queremos guardar el programa en una carpeta llamada Java en el disco C:

```text
cd C:\
mkdir Java
cd Java
```

mkdir crea una carpeta y cd permite ingresar a ella.

**Paso 3: Crear el archivo**
Escribir el siguiente comando:

```text
notepad HolaMundo.java
```

Se abrirá el Bloc de notas. Allí se escribe el siguiente código:

```text
public class HolaMundo {
    public static void main(String[] args) {
        System.out.println("Hola, bienvenido al curso de Algoritmia y Programación");
    }
}
```

Luego:

- Hacer clic en Archivo → Guardar.
- Cerrar el Bloc de notas.

**Paso 4: Compilar el programa**
En el CMD escribir:

```text
javac HolaMundo.java
```

Si no aparece ningún mensaje, significa que el programa se compiló correctamente.

**Compilar significa traducir el código escrito por el programador a un lenguaje que la computadora pueda entender.**

**Paso 5: Ejecutar el programa**

Escribir:

```text
java HolaMundo
```

El resultado será:

```text
Hola, bienvenido al curso de Algoritmia y Programación
```

**Resumen**

| Comando                  | Función                     |
| ------------------------ | --------------------------- |
| `notepad HolaMundo.java` | Crea y abre el archivo Java |
| `javac HolaMundo.java`   | Compila el programa         |
| `java HolaMundo`         | Ejecuta el programa         |


**Explicación sencilla:**

1. Crear el archivo (notepad).
2. Escribir el código y guardarlo.
3. Compilar (javac) para verificar que no existan errores.
4. Ejecutar (java) para ver el resultado en pantalla.
