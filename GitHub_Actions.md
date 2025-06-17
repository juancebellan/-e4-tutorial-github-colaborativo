# Automatización con GitHub Actions y CI/CD Básico

## ¿Qué es GitHub Actions?

Hasta ahora todos las funcionalidades que hemos explicado, eran para que las hiciese un usuario, ¿pero podria automatizarse?

Para ello esta GitHub Actions, que es una funcionalidad que permite **automatizar tareas dentro de un repositorio** de GitHub. Esto significa que puedes configurar procesos automáticos que se ejecuten en respuesta a eventos, como cuando alguien hace un commit o crea un pull request.

### Tipos de tareas automatizables:

Las tareas más comunes de que se pueden hacer con **GitHub Actions** son:
- Ejecutar pruebas automáticamente al hacer push.
- Verificar que el código cumpla con ciertos estándares.
- Desplegar una aplicación después de aprobar un pull request.
- Generar documentación automáticamente.

---
## ¿Qué es CI/CD?

CI/CD son siglas que significan:

| Sigla | Significado                     | Qué hace                                                       |
|-------|---------------------------------|----------------------------------------------------------------|
| CI    | *Continuous Integration*         | Integración continua: Ejecuta pruebas y verifica el código automáticamente en cada cambio. |
| CD    | *Continuous Delivery/Deployment* | Entrega o despliegue continuo: Automatiza el despliegue del código a producción o entornos de prueba. |

---

### Ventajas de usar GitHub Actions y CI/CD

El uso de automatización en el desarrollo aporta múltiples beneficios, tanto en proyectos personales como colaborativos, entre otras cosas, GitHub Actions y CI/CD mejoran la calidad del software ya que automatizas pruebas y analisis, de esta manera se pueden evitar errores o fallos de formateo. Además, mejora la eficiencia ya que se ocupa de tareas repetitivas y permiten escalar la automatización conforme crece el proyecto.

---

## ¿Cómo se configura un workflow en GitHub Actions?

Los **workflows** son archivos que definen los pasos a seguir para automatizar tareas. Se escriben en formato YAML (`.yml`) y se guardan en la carpeta:

.github/workflows/

Cada archivo define un flujo de trabajo que puede ejecutarse automáticamente cuando ocurre un evento, como un `push`, un `pull_request`, o en una programación definida.

---

### Ejemplo básico de workflow

```yml
# .github/workflows/ci.yml

name: CI

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Mostrar saludo
        run: echo "Hola mundo"
```

### ¿Qué significa este workflow?

- `name: CI` → Nombre del workflow.
- `on: [push]` → Se ejecuta cuando se hace un push al repositorio.
- `jobs:` → Define uno o varios trabajos.
- `build:` → Es el nombre del trabajo principal.
- `runs-on:` → Especifica el sistema operativo del entorno (en este caso Ubuntu).
- `steps:` → Lista de pasos a seguir.
- `uses: actions/checkout@v2` → Clona el código del repositorio.
- `run: echo` → Ejecuta un comando simple en la terminal.

## ¿Dónde colocarlo?
Guarda el archivo con extensión .yml dentro de la ruta:

```bash
.github/workflows/ci.yml
```
Una vez subido al repositorio, cada vez que alguien haga un push, GitHub ejecutará automáticamente ese workflow.