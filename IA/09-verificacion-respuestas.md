# 09. Cómo Verificar Respuestas de la IA

## Presentación

La IA puede ayudar mucho, pero no siempre responde correctamente.

Por eso, todo estudiante debe aprender a verificar las respuestas que recibe.

---

# 1. ¿Por qué verificar?

Porque la IA puede:

- Inventar datos.
- Generar código con errores.
- Omitir condiciones.
- Dar explicaciones incompletas.
- Usar temas que aún no se han visto.
- No seguir exactamente el enunciado.
- Confundir versiones de herramientas.

---

# 2. Verificar una explicación

Cuando la IA explique un tema, revisa:

- ¿La explicación es clara?
- ¿Tiene ejemplos?
- ¿Coincide con lo visto en clase?
- ¿Usa palabras que entiendo?
- ¿Puedo explicarlo con mis propias palabras?

Si no puedes explicarlo, pide una explicación más sencilla.

Prompt útil:

```text
Explícalo con palabras más sencillas y usa un ejemplo cotidiano.
```

---

# 3. Verificar código Java

Antes de aceptar código generado por IA, revisar:

- ¿Compila?
- ¿Ejecuta?
- ¿Cumple el enunciado?
- ¿Usa temas vistos en clase?
- ¿Tiene variables claras?
- ¿Tiene validaciones necesarias?
- ¿Puedo explicar cada línea?
- ¿Se probó con varios datos?

---

# 4. Checklist para código

```text
[ ] Leí el código completo.
[ ] Entiendo las variables.
[ ] Entiendo los condicionales.
[ ] Entiendo los ciclos.
[ ] El código compila.
[ ] El código ejecuta.
[ ] Probé datos válidos.
[ ] Probé datos inválidos.
[ ] Hice prueba de escritorio.
[ ] Puedo explicar la solución.
```

---

# 5. Verificar con casos de prueba

Ejemplo:

Programa que valida nota entre 0.0 y 5.0.

Casos de prueba:

| Nota | Resultado esperado |
|---:|---|
| -1.0 | No válida |
| 0.0 | Válida |
| 2.5 | Válida |
| 5.0 | Válida |
| 6.0 | No válida |

---

# 6. Verificar con prueba de escritorio

Si un programa usa ciclos, se debe revisar cómo cambian las variables.

Ejemplo:

```java
int suma = 0;

for (int i = 1; i <= 3; i++) {
    suma = suma + i;
}
```

Prueba:

| i | suma antes | suma después |
|---:|---:|---:|
| 1 | 0 | 1 |
| 2 | 1 | 3 |
| 3 | 3 | 6 |

---

# 7. Verificar si usa temas no vistos

A veces la IA puede usar código avanzado.

Ejemplo:

```java
stream()
lambda
var
records
interfaces avanzadas
```

Si el curso aún no ha trabajado esos temas, se debe pedir una versión más básica.

Prompt:

```text
Reescribe el código usando solo Scanner, if, for, arreglos y métodos básicos. No uses temas avanzados.
```

---

# 8. Verificar fuentes

Cuando la IA dé información teórica o datos actuales, se debe pedir fuente.

Prompt:

```text
Dame fuentes confiables para verificar esta información.
```

Pero no basta con que la IA cite. También hay que revisar si la fuente existe y si realmente dice eso.

---

# 9. Verificar comandos

Cuando la IA sugiera comandos de Git o instalación, revisar:

- Si el comando corresponde al sistema operativo.
- Si se entiende qué hace.
- Si se puede revertir.
- Si no borra archivos.
- Si no expone contraseñas.

---

# 10. Señales de alerta

Desconfía si la respuesta:

- Parece demasiado perfecta.
- No explica el razonamiento.
- Usa código que no entiendes.
- No responde al enunciado.
- Da información sin fuente.
- Mezcla varios temas.
- Usa librerías que no conoces.
- No incluye validaciones.

---

# 11. Preguntas para verificar comprensión

Después de recibir una respuesta de IA, responde:

1. ¿Cuál era el problema?
2. ¿Qué datos entran?
3. ¿Qué proceso se realiza?
4. ¿Qué resultado sale?
5. ¿Qué variables se usan?
6. ¿Qué hace cada condicional?
7. ¿Qué hace cada ciclo?
8. ¿Qué pasaría con un dato inválido?
9. ¿Qué cambiaría si el enunciado cambia?
10. ¿Puedo explicarlo sin mirar la IA?

---

## Conclusión

Verificar no es opcional. La IA puede ser una guía, pero el estudiante sigue siendo responsable de lo que entrega.
