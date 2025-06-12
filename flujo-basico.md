# Flujo Básico con Git y GitHub

Este documento explica los comandos esenciales utilizados en un flujo de trabajo básico en GitHub. Aprenderás a usar `clone`, `branch`, `add`, `commit`, `push`, `pull` y cómo se crea un Pull Request.  
Ejemplo basado en nuestro repositorio:

https://github.com/juancebellan/-e4-tutorial-github-colaborativo.git


## git clone

El comando `git clone` se utiliza para clonar un repositorio remoto y trabajar en él de manera local. Es el primer paso para colaborar en un proyecto que ya existe en GitHub.

**Ejemplo:**

```bash
git clone https://github.com/juancebellan/-e4-tutorial-github-colaborativo.git
```

Esto creará una carpeta con el contenido del repositorio, incluyendo todo el historial de versiones.


## git branch

Las ramas permiten trabajar en nuevas tareas o características sin afectar la rama principal (main).

**Ejemplo: Crear y cambiar a una nueva rama llamada flujo-basico**

```bash
git checkout -b flujo-basico
```

Esta rama servirá para hacer los cambios necesarios para tu tarea sin alterar el trabajo de tus compañeros.


## git add

El comando git add se usa para preparar los archivos modificados o nuevos antes de confirmarlos con el commit.

**Ejemplo al crear o modificar el archivo flujo-basico.md:**

```bash
git add flujo-basico.md
```
También puedes añadir todos los archivos con:
```bash
git add .
```


## git commit

El comando git commit guarda los cambios añadidos al área de preparación. Es como hacer una foto del estado actual del proyecto.

**Ejemplo:**

```bash
git commit -m "mensaje de la accion realizada"
```
Es recomendable hacer commits con mensajes claros que expliquen qué has cambiado.