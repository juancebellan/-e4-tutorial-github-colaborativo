# Guía de Buenas Prácticas en GitHub

Este repositorio contiene una recopilación de buenas prácticas para el desarrollo colaborativo en proyectos utilizando Git y GitHub. Está orientado tanto a principiantes como a personas con conocimientos intermedios que deseen trabajar de forma ordenada, eficiente y profesional.

-----------

## Convenciones de Commits

Una buena convención en los mensajes de commit mejora la claridad del historial y facilita el trabajo en equipo. Utilizamos la convención **Conventional Commits**, que establece una estructura clara:

```
<tipo>[alcance]: <mensaje en infinitivo>
```

### Tipos más comunes:

- `feat`: Nueva funcionalidad
- `fix`: Corrección de errores
- `docs`: Cambios en la documentación
- `style`: Formato, sin afectar el código
- `refactor`: Reestructuración de código
- `test`: Añadir o modificar tests
- `chore`: Tareas de mantenimiento

### Ejemplo:

```bash
git commit -m "feat(login): añadir validación de formulario"
```

Escribe los mensajes en modo infinitivo: `"añadir"`, no `"añadido"`.

-----------

## Flujo Básico con Git

Para trabajar de forma segura y ordenada con Git:

### 1. Clonar el repositorio

```bash
git clone https://github.com/usuario/repositorio.git
```

### 2. Crear una rama de trabajo

```bash
git checkout -b nombre-rama
```

### 3. Añadir archivos al staging

```bash
git add archivo.txt
```

### 4. Crear un commit

```bash
git commit -m "feat: descripción del cambio"
```

### 5. Subir la rama a GitHub

```bash
git push origin nombre-rama
```

### 6. Crear un Pull Request desde GitHub

Permite la revisión del código antes de fusionarlo a la rama principal.

-----------

## Introducción a GitHub

**GitHub** es una plataforma basada en la nube que permite almacenar, gestionar y colaborar en proyectos que usan Git.

### ¿Por qué usar GitHub?

- Control de versiones distribuido
- Trabajo colaborativo
- Automatización de procesos (CI/CD)
- Visualización de tareas y problemas
- Hosting gratuito para proyectos públicos

### Historia breve

GitHub fue fundado en 2008 y rápidamente se convirtió en la plataforma líder para el alojamiento de código fuente. En 2018 fue adquirida por Microsoft y hoy cuenta con más de 100 millones de desarrolladores registrados.

-----------

## GitHub Actions

**GitHub Actions** permite automatizar flujos de trabajo dentro del repositorio. Puedes ejecutar scripts automáticamente cuando se realicen ciertas acciones como `push`, `pull_request`, etc.

### ¿Para qué sirve?

- Ejecutar tests automáticamente
- Compilar código
- Desplegar aplicaciones
- Enviar notificaciones

### Ejemplo de workflow:

```yml
name: CI
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Ejecutar script
        run: echo "Hola mundo"
```

Guarda el workflow en la ruta: `.github/workflows/nombre.yml`.

-----------

## Issues, Projects y Milestones

### Issues

Los **Issues** son tickets que representan tareas, errores o ideas. Cada issue puede tener:

- Título y descripción
- Etiquetas (bug, feature, enhancement...)
- Asignados
- Comentarios

### Milestones

Permiten agrupar issues bajo un mismo objetivo o versión del proyecto. Útil para planificar entregas.

### Projects

Los **Projects** de GitHub permiten organizar los issues como en un tablero Kanban. Son ideales para visualizar el progreso general.

---

## Recomendaciones Finales

- Haz commits pequeños y frecuentes.
- Trabaja siempre en ramas, no directamente en `main`.
- Revisa y comenta los Pull Requests.
- Mantén la documentación actualizada.
- Automatiza tareas repetitivas con Actions.

-----------

> Esta guía ha sido elaborada por [Unai Pinilla](https://www.github.com/unaipini) y [Juan Cebellán](https://www.github.com/juancebellan), como parte del trabajo para la **E4** de la asignatura **Ingeniería Web**.
