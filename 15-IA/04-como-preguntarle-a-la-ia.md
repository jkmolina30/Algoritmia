# 04. Cómo preguntarle a la IA

## Presentación

La calidad de la respuesta de una IA depende en gran parte de la calidad de la pregunta.

A una instrucción dada a una IA se le suele llamar **prompt**.

Un buen prompt permite obtener respuestas más claras, útiles y ajustadas a lo que se necesita.

---

## 1. ¿Qué es un prompt?

Un prompt es la instrucción, pregunta o solicitud que se le escribe a una herramienta de IA.

Ejemplo simple:

```text
Explícame qué es un ciclo for.
```

Ejemplo mejorado:

```text
Estoy aprendiendo Java desde cero. Explícame qué es un ciclo for con un ejemplo sencillo, una prueba de escritorio y un ejercicio para practicar.
```

---

## 2. Problema de los prompts vagos

Prompt débil:

```text
Explícame Java.
```

Problema:

La pregunta es demasiado amplia. La IA no sabe si debe explicar historia, sintaxis, variables, clases, instalación o ejemplos.

Prompt mejor:

```text
Estoy en primer semestre de Ingeniería de Sistemas. Explícame qué es una variable en Java, con un ejemplo de edad y otro de nota final.
```

---

## 3. Elementos de un buen prompt

Un buen prompt puede incluir:

| Elemento | Pregunta que responde |
|---|---|
| Rol | ¿Cómo debe actuar la IA? |
| Contexto | ¿Qué estoy haciendo? |
| Tema | ¿Sobre qué necesito ayuda? |
| Nivel | ¿Qué tanto sé? |
| Formato | ¿Cómo quiero la respuesta? |
| Restricciones | ¿Qué debe evitar? |
| Ejemplo | ¿Hay un caso concreto? |

---

## 4. Fórmula básica para preguntar

```text
Actúa como [rol].
Estoy aprendiendo [tema].
Necesito que me expliques [solicitud].
Mi nivel es [nivel].
Dame la respuesta en formato [formato].
No hagas [restricción].
```

---

## 5. Ejemplo aplicado a Java

```text
Actúa como un docente de programación.
Estoy aprendiendo condicionales en Java.
Explícame la diferencia entre if, else if y else.
Mi nivel es principiante.
Dame un ejemplo sencillo con notas académicas.
No uses código avanzado.
```

---

## 6. Pedir explicación, no solo respuesta

Mala práctica:

```text
Hazme el ejercicio.
```

Mejor práctica:

```text
Ayúdame a entender cómo resolver este ejercicio. Primero identifica entrada, proceso y salida. Luego dame una pista, no el código completo.
```

---

## 7. Pedir revisión de código

Prompt recomendado:

```text
Estoy aprendiendo Java. Este código no funciona. No me des una solución nueva desde cero. Revisa mi código, dime dónde está el error, explícame por qué ocurre y ayúdame a corregirlo paso a paso.
```

---

## 8. Pedir ejercicios de práctica

```text
Créame 10 ejercicios de ciclos for en Java para principiantes. Ordénalos de menor a mayor dificultad. No incluyas la solución todavía.
```

---

## 9. Pedir retroalimentación

```text
Revisa mi explicación sobre arreglos en Java. Dime qué está bien, qué está incompleto y qué ejemplo podría agregar para mejorarla.
```

---

## 10. Pedir comparación

```text
Compara arreglo y ArrayList en Java usando una tabla sencilla. Incluye un ejemplo corto de cada uno.
```

---

## 11. Pedir una prueba de escritorio

```text
Haz una prueba de escritorio para este código Java. Muestra cómo cambian las variables en cada iteración.
```

---

## 12. Preguntar en varias etapas

En lugar de pedir todo de una vez, es mejor dividir:

1. Explícame el problema.
2. Identifica entrada, proceso y salida.
3. Dame el pseudocódigo.
4. Haz prueba de escritorio.
5. Ahora sí, ayúdame con Java.
6. Revisa si el código compila.
7. Dame ejercicios similares.

---

## 13. Plantilla para estudiantes

```text
Estoy trabajando en el tema de [tema].
El ejercicio dice: [pegar enunciado].
Mi intento fue: [pegar intento].
Necesito que:
1. Revises mi análisis.
2. Me digas si la lógica está bien.
3. Me expliques los errores.
4. No me entregues el código completo todavía.
```

---

## 14. Prompts que se deben evitar

Evitar:

```text
Hazme la tarea.
Dame el código completo.
Resuelve todo.
Cambia este código para que no parezca copiado.
Hazlo rápido sin explicar.
```

Estos prompts no ayudan al aprendizaje.

---

## 15. Regla de oro

```text
Una buena pregunta debe mostrar qué estás intentando aprender.
```

---

## Conclusión

Preguntar bien es una habilidad. Un estudiante que aprende a formular buenos prompts puede usar la IA como tutor, guía de práctica y apoyo para mejorar su razonamiento.
