# Convenciones de Commits y Nombres de Ramas

Es importante, nombrar a las cosas correctamente y explicar bien todas
las cosas que vas a añadir, ya que de esta manera se puede saber bien que cosas se han modificado añadido y quitado, de esta manera para los demas desarrolladores y colaboradores es facil hacer un seguimiento de los cambios.

## Convenciones para mensajes de commit

Seguir una estructura clara en los commits ayuda a mantener un historial limpio, comprensible y profesional. A continuación, se indican las mejores prácticas usando la convención `Conventional Commits`. Esta fue una convención creada por el equipo Angular en **2018**, con el fin de estandarizar los mensajes de commit dentro de su ecosistema.

### Ejemplos:

Alguno mensajes genericos que se pueden poner son los siguientes
- `feat`: Añadir una nueva funcionalidad
- `fix`: corregir un error
- `docs`: Cambios en la documentación
- `style`: Cambios de estilo
- `refactor`: Reestructuración del código sin cambiar su comportamiento  
- `test`: Añadir o modificar tests 
- `chore`: Tareas menores que no afectan directamente el código (actualizar dependencias, configuración, etc.)

>Estos mensajes se ponen lo primero y luego se explica un poco la funcionalidad

##  Convenciones para Nombres de Ramas

Nombrar las ramas de forma clara y consistente ayuda a entender su propósito sin necesidad de inspeccionar el contenido. 

### Ejemplos

`feature/`: Nuevas funcionalidades
`fix/`: Correcciones de errores
`hotfix/`: Correcciones urgentes en producción
`chore/`: Tareas de mantenimiento o configuración
`docs/`: Cambios en la documentación
`refactor/`: Reestructurar código sin modificar funcionalidad
`test/`: Ramas relacionadas con pruebas

---

## Recomendaciones Generales

A parte de seguir los mensajes genericos, es importante seguir un estilo fijo todo el rato
por ello algunos recomendaciones son:

- Escribir los mensajes de commit en **modo imperativo**: "añadir" en lugar de "añadido".
- Limitar la descripción a **máximo 72 caracteres**.
- Utilizar el cuerpo del commit (si es necesario) para explicar el "por qué" del cambio.
- Evitar mensajes genéricos como `update`, `cambiar`, `eliminar`, `agregar`, `cosas`.






