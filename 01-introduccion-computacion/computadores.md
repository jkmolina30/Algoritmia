Unidad 1. Introducción a la Computación

Presentación de la unidad
Antes de aprender a programar, es necesario comprender qué es un computador, cómo procesa la información y por qué los lenguajes de programación son necesarios para comunicarnos con una máquina.

Muchas veces se piensa que programar es simplemente escribir código. Sin embargo, la programación comienza mucho antes. Primero se debe comprender el problema, identificar los datos, organizar una solución y luego escribir instrucciones que el computador pueda ejecutar. Esta unidad introduce los conceptos fundamentales de computación que servirán como base para el resto del curso de Algoritmia y Programación.

1. ¿Qué es la computación?
La computación es el área que estudia cómo representar, procesar, almacenar y transmitir información utilizando computadores. En palabras sencillas, la computación estudia cómo las máquinas pueden ayudar a resolver problemas mediante el manejo de datos.

Por ejemplo:

* Una calculadora procesa números.

* Un celular procesa mensajes, imágenes, llamadas y aplicaciones.

* Un cajero automático procesa datos de tarjetas, claves y transacciones.

* Una plataforma académica procesa notas, estudiantes, cursos y reportes.

* Un sistema de inventario procesa productos, cantidades y precios.

En todos estos casos hay datos que entran, operaciones que se realizan y resultados que se muestran.

2. ¿Qué es un computador?
Un computador es una máquina electrónica capaz de recibir datos, procesarlos, almacenarlos y entregar resultados. De forma general, un computador trabaja con el siguiente esquema:

Entrada → Procesamiento → Almacenamiento → Salida

Ejemplo cotidiano:

Cuando una persona calcula el promedio de tres notas usando un computador:

| Etapa | Descripción | 
| ------------- | ------------- |
| Entrada | El usuario escribe las tres notas |
| Procesamiento | El computador suma las notas y divide entre tres |
| Almacenamiento | El resultado se guarda temporalmente en memoria |
| Salida | Celda B2 | El computador muestra el promedio en pantalla |
	                    
Aunque para el usuario parezca una acción sencilla, internamente el computador ejecuta instrucciones precisas.

3. Entrada, procesamiento, almacenamiento y salida

Todo sistema computacional puede entenderse mediante cuatro acciones principales.

3.1. Entrada

La entrada corresponde a los datos que recibe el computador.

Ejemplos:

Escribir el nombre de un estudiante.
Digitar una nota.
Hacer clic en un botón.
Escanear un código de barras.
Subir un archivo.
Tomar una fotografía.
3.2. Procesamiento

El procesamiento corresponde a las operaciones que realiza el computador con los datos recibidos.

Ejemplos:

Sumar dos números.
Calcular un promedio.
Comparar una nota con 3.0.
Ordenar una lista de nombres.
Buscar un producto en un inventario.
Verificar si una contraseña es correcta.
3.3. Almacenamiento

El almacenamiento corresponde a guardar datos para usarlos después.

Ejemplos:

Guardar un documento.
Guardar las notas de un estudiante.
Guardar usuarios en una base de datos.
Guardar fotos en el celular.
Guardar archivos en una memoria USB.
3.4. Salida

La salida corresponde al resultado que el computador entrega al usuario.

Ejemplos:

Mostrar un mensaje en pantalla.
Imprimir un reporte.
Reproducir un sonido.
Generar un archivo PDF.
Mostrar una gráfica.
Enviar una notificación.
4. ¿Qué es un dato?

Un dato es una representación básica de un valor.

Ejemplos de datos:

Juan
18
4.5
Verdadero
A

Un dato por sí solo puede no tener mucho significado. Pero cuando se organiza dentro de un contexto, se convierte en información.

5. ¿Qué es información?

La información es el resultado de organizar, procesar o interpretar datos.

Ejemplo:

Datos:

Nombre: Ana
Nota 1: 4.0
Nota 2: 3.5
Nota 3: 4.5

Información:

Ana obtuvo un promedio de 4.0 y aprobó la asignatura.

El computador trabaja con datos, pero el objetivo de muchos programas es producir información útil.

6. ¿Qué es un programa?

Un programa es un conjunto de instrucciones que le indican al computador qué debe hacer.

Ejemplo:

Un programa puede indicar:

Leer el nombre de un estudiante.
Leer tres notas.
Calcular el promedio.
Determinar si aprobó o reprobó.
Mostrar el resultado.

Un computador no adivina lo que debe hacer. Necesita instrucciones claras, ordenadas y precisas.

7. ¿Qué es programar?

Programar es escribir instrucciones para que un computador resuelva un problema o realice una tarea.

Pero programar no es solo escribir código.

Programar implica:

Comprender el problema.
Analizar los datos necesarios.
Diseñar una solución.
Escribir instrucciones.
Probar el programa.
Corregir errores.
Mejorar la solución.

En este curso, se aprenderá primero a pensar la solución y luego a implementarla en Java.

8. ¿Qué es un lenguaje de programación?

Un lenguaje de programación es un conjunto de reglas, símbolos e instrucciones que permite escribir programas.

Así como las personas usan idiomas como español, inglés o francés para comunicarse, los programadores usan lenguajes como Java, Python, C++, JavaScript o C# para comunicarse con el computador.

Ejemplo de instrucción en Java:

System.out.println("Hola mundo");

Esta instrucción le dice al computador que muestre el mensaje Hola mundo en pantalla.

9. ¿Por qué el computador no entiende directamente el lenguaje humano?

El computador no entiende frases humanas como:

Por favor, calcula el promedio de estas notas.

El computador necesita instrucciones formales, escritas con reglas exactas.

Por eso usamos lenguajes de programación.

En un lenguaje de programación, una instrucción debe escribirse correctamente. Si falta un símbolo, una palabra o un punto y coma, el programa puede generar error.

10. Relación entre algoritmo, pseudocódigo y programa

Estos tres conceptos estarán presentes durante todo el curso.

Concepto	Explicación sencilla
Algoritmo	Secuencia ordenada de pasos para resolver un problema
Pseudocódigo	Forma de escribir el algoritmo usando un lenguaje cercano al humano
Programa	Implementación del algoritmo en un lenguaje como Java
Ejemplo

Problema:

Calcular el doble de un número.

Algoritmo en lenguaje natural:

1. Pedir un número.
2. Multiplicar el número por 2.
3. Mostrar el resultado.

Pseudocódigo:

Algoritmo CalcularDoble
    Definir numero, doble Como Entero

    Escribir "Ingrese un número:"
    Leer numero

    doble <- numero * 2

    Escribir "El doble es: ", doble
FinAlgoritmo

Programa en Java:

import java.util.Scanner;

public class CalcularDoble {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int numero;
        int doble;

        System.out.print("Ingrese un número: ");
        numero = entrada.nextInt();

        doble = numero * 2;

        System.out.println("El doble es: " + doble);

        entrada.close();
    }
}
11. ¿Por qué iniciar con computación antes de programar?

Porque antes de escribir código es importante entender:

Qué es un computador.
Cómo recibe datos.
Cómo procesa instrucciones.
Cómo almacena información.
Cómo muestra resultados.
Qué papel cumple el software.
Qué papel cumple el hardware.
Por qué existen los lenguajes de programación.

Esto permite que el estudiante no vea la programación como una serie de comandos aislados, sino como un proceso lógico para resolver problemas usando tecnología.

12. Conceptos clave de la unidad
Concepto	Definición sencilla
Computador	Máquina que recibe, procesa, almacena y entrega información
Dato	Valor básico que puede ser procesado
Información	Datos organizados con significado
Hardware	Parte física del computador
Software	Programas e instrucciones que usa el computador
Programa	Conjunto de instrucciones
Lenguaje de programación	Medio para escribir instrucciones que el computador puede ejecutar
Algoritmo	Pasos ordenados para resolver un problema
Pseudocódigo	Representación sencilla de un algoritmo
13. Resultado de aprendizaje de la unidad

Al finalizar esta unidad, el estudiante estará en capacidad de explicar qué es un computador, identificar sus componentes básicos, diferenciar hardware y software, reconocer el papel de los lenguajes de programación y relacionar los conceptos de dato, información, algoritmo y programa.

14. Resumen de la unidad

Un computador es una máquina capaz de recibir datos, procesarlos, almacenarlos y entregar resultados. Para que pueda realizar tareas, necesita programas. Los programas se escriben usando lenguajes de programación. Antes de escribir un programa, se debe diseñar una solución mediante un algoritmo.

Por eso, aprender programación no consiste únicamente en aprender comandos. Consiste en aprender a pensar de manera ordenada para que una máquina pueda ejecutar una solución correctamente.
