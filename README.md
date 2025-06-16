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