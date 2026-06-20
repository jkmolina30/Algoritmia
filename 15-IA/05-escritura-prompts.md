# 05. Escritura de Prompts

## Presentación

La escritura de prompts es la habilidad de construir instrucciones claras para que una IA responda de manera útil.

En programación, un buen prompt puede ayudar a entender errores, practicar ejercicios y mejorar el código.

---

# 1. Estructura recomendada de un prompt

Una estructura útil es:

```text
Rol + contexto + tarea + nivel + formato + restricciones
```

---

## 2. Rol

El rol le indica a la IA cómo debe responder.

Ejemplos:

```text
Actúa como docente de programación.
Actúa como tutor de Java para principiantes.
Actúa como revisor de código.
Actúa como estudiante que explica paso a paso.
```

---

## 3. Contexto

El contexto le dice a la IA qué estás haciendo.

Ejemplo:

```text
Estoy en primer semestre y estoy aprendiendo ciclos en Java.
```

---

## 4. Tarea

La tarea explica lo que necesitas.

Ejemplo:

```text
Necesito entender por qué mi ciclo while no termina.
```

---

## 5. Nivel

El nivel ayuda a ajustar la explicación.

Ejemplo:

```text
Explícalo para una persona que apenas está empezando a programar.
```

---

## 6. Formato

El formato indica cómo quieres recibir la respuesta.

Ejemplos:

```text
Dame una tabla.
Dame pasos numerados.
Dame un ejemplo en Java.
Dame primero pseudocódigo y luego Java.
Dame una prueba de escritorio.
```

---

## 7. Restricciones

Las restricciones indican lo que la IA no debe hacer.

Ejemplos:

```text
No me des la solución completa.
No uses temas avanzados.
No uses programación orientada a objetos todavía.
No uses ArrayList, solo arreglos.
No cambies todo mi código.
```

---

# 8. Prompt para estudiar un tema

```text
Actúa como docente de programación.
Estoy aprendiendo arreglos en Java.
Explícame qué es un arreglo, para qué sirve y cómo se recorre con for.
Mi nivel es principiante.
Incluye un ejemplo sencillo y una prueba de escritorio.
```

---

# 9. Prompt para corregir código

```text
Actúa como revisor de código Java.
Estoy aprendiendo ciclos.
Este código no funciona como espero:

[pegar código]

Necesito que:
1. Identifiques el error.
2. Me expliques por qué ocurre.
3. Me muestres cómo corregirlo.
4. No cambies toda la estructura si no es necesario.
```

---

# 10. Prompt para practicar sin copiar

```text
Estoy aprendiendo condicionales en Java.
Dame 5 ejercicios para practicar.
No incluyas las soluciones.
Ordénalos de menor a mayor dificultad.
Incluye qué tema practica cada ejercicio.
```

---

# 11. Prompt para pedir pistas

```text
Tengo este ejercicio:

[pegar enunciado]

No me des el código completo.
Dame solo una pista para empezar y ayúdame a identificar entrada, proceso y salida.
```

---

# 12. Prompt para mejorar un README

```text
Actúa como revisor de documentación.
Este es el README de mi proyecto:

[pegar README]

Ayúdame a mejorarlo para que sea claro, ordenado y adecuado para GitHub.
No inventes funcionalidades que mi proyecto no tiene.
```

---

# 13. Prompt para preparar una sustentación

```text
Tengo que sustentar este proyecto de Java:

[describir proyecto]

Ayúdame a preparar una explicación de 3 minutos.
Incluye:
1. Qué problema resuelve.
2. Qué clases tiene.
3. Qué métodos importantes usa.
4. Qué aprendí con el proyecto.
```

---

# 14. Prompt para prueba de escritorio

```text
Haz una prueba de escritorio del siguiente código.
Muestra una tabla con las variables en cada iteración.

[código]
```

---

# 15. Prompt para comparar conceptos

```text
Compara while, do-while y for en Java.
Usa una tabla.
Incluye cuándo conviene usar cada uno y un ejemplo corto.
```

---

# 16. Prompt para verificar comprensión

```text
Hazme 5 preguntas sobre métodos en Java para comprobar si entendí el tema.
Después de mis respuestas, dime qué debo reforzar.
```

---

# 17. Prompt completo modelo

```text
Actúa como docente de Algoritmia y Programación.
Estoy en primer semestre y estoy aprendiendo arreglos en Java.
Tengo este ejercicio: leer 5 notas y calcular el promedio.
Ya sé usar variables, Scanner, for y condicionales básicos.
Necesito que me guíes paso a paso.
Primero ayúdame a identificar entrada, proceso y salida.
Luego dame el pseudocódigo.
Después dame el código Java.
Finalmente, haz una prueba de escritorio.
No uses ArrayList ni métodos todavía.
```

---

# 18. Checklist para evaluar un prompt

Antes de enviar un prompt, revisa:

- [ ] ¿Dije qué tema estoy trabajando?
- [ ] ¿Dije mi nivel?
- [ ] ¿Expliqué qué necesito?
- [ ] ¿Pedí el formato de respuesta?
- [ ] ¿Agregué restricciones?
- [ ] ¿Incluí mi intento si ya hice algo?
- [ ] ¿Pedí explicación y no solo respuesta?

---

## Conclusión

Un buen prompt no solo pide una respuesta. También guía a la IA para que responda de acuerdo con el nivel, el objetivo y las reglas del aprendizaje.
