# Comandos Básicos de Git

## Presentación

Este archivo contiene comandos básicos de Git para trabajar con proyectos de programación.

La idea no es memorizar comandos, sino comprender para qué sirve cada uno.

---

## 1. Verificar instalación de Git

```bash
git --version
```

Este comando muestra la versión instalada de Git.

---

## 2. Configurar nombre de usuario

```bash
git config --global user.name "Tu Nombre"
```

Ejemplo:

```bash
git config --global user.name "Juan Carlos Molina"
```

---

## 3. Configurar correo

```bash
git config --global user.email "correo@example.com"
```

Ejemplo:

```bash
git config --global user.email "estudiante@correo.com"
```

---

## 4. Ver configuración

```bash
git config --list
```

Muestra la configuración actual de Git.

---

## 5. Inicializar un repositorio

Ubicarse en la carpeta del proyecto y ejecutar:

```bash
git init
```

Esto convierte la carpeta en un repositorio Git.

---

## 6. Ver estado del repositorio

```bash
git status
```

Muestra archivos modificados, agregados o pendientes.

---

## 7. Agregar archivos

Agregar todos los archivos:

```bash
git add .
```

Agregar un archivo específico:

```bash
git add README.md
```

---

## 8. Crear un commit

```bash
git commit -m "Mensaje del commit"
```

Ejemplo:

```bash
git commit -m "Agrega ejercicios de condicionales"
```

---

## 9. Ver historial de commits

```bash
git log
```

Versión corta:

```bash
git log --oneline
```

---

## 10. Conectar con GitHub

Cuando se crea un repositorio en GitHub, se puede conectar así:

```bash
git remote add origin URL_DEL_REPOSITORIO
```

Ejemplo:

```bash
git remote add origin https://github.com/usuario/repositorio.git
```

---

## 11. Ver repositorios remotos

```bash
git remote -v
```

---

## 12. Subir cambios a GitHub

Primera subida:

```bash
git branch -M main
git push -u origin main
```

Luego, para futuras subidas:

```bash
git push
```

---

## 13. Descargar cambios desde GitHub

```bash
git pull
```

Trae los cambios remotos al computador.

---

## 14. Clonar un repositorio

```bash
git clone URL_DEL_REPOSITORIO
```

Ejemplo:

```bash
git clone https://github.com/usuario/algoritmia.git
```

---

## 15. Ver ramas

```bash
git branch
```

---

## 16. Crear una rama

```bash
git branch nombre-rama
```

Ejemplo:

```bash
git branch unidad-condicionales
```

---

## 17. Cambiar de rama

```bash
git checkout nombre-rama
```

También se puede usar:

```bash
git switch nombre-rama
```

---

## 18. Crear y cambiar a una rama

```bash
git checkout -b nombre-rama
```

O:

```bash
git switch -c nombre-rama
```

---

## 19. Tabla resumen

| Comando | Uso |
|---|---|
| `git init` | Inicia un repositorio |
| `git status` | Revisa el estado |
| `git add .` | Agrega cambios |
| `git commit -m "mensaje"` | Guarda cambios |
| `git log --oneline` | Muestra historial |
| `git remote add origin URL` | Conecta con GitHub |
| `git push` | Sube cambios |
| `git pull` | Descarga cambios |
| `git clone URL` | Copia un repositorio |

---

## 20. Flujo recomendado para estudiantes

Cada vez que termines una actividad:

```bash
git status
git add .
git commit -m "Agrega actividad de arreglos"
git push
```

---

## Recomendación

Usa mensajes de commit claros. Un buen mensaje debe decir qué hiciste.

Bueno:

```bash
git commit -m "Agrega ejercicios de ArrayList"
```

Poco claro:

```bash
git commit -m "cosas"
```
