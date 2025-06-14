# Resolución de Conflictos en Git

En el caso de que varias personas trabajen en un mismo archivo, es normal que surgan conflictos, estos se deben a que Git no sabe cual de los dos criterios prevalece, por ejemplo si en una misma linea de archivo, un usuario la edita y otro la elimina, en estos casos Git no sabe cual de los dos criterios es el correcto y lanza un error de conflicto

---

## ¿Cómo surgen los conflictos?

Los conflictos más comunes aparecen al:

- Realizar un `merge` entre ramas con cambios en las mismas líneas.
- Hacer un `rebase` que reescribe el historial sobre archivos modificados.
- Aplicar `cherry-pick` o recuperar cambios con `stash`.

---

## ¿Cómo detectar un conflicto?

Git te avisa automáticamente durante el proceso:

```bash
Auto-merging archivo.txt
CONFLICT (content): Merge conflict in archivo.txt
Automatic merge failed; fix conflicts and then commit the result.

```

---

## ¿Como aparecen los conflictos?

El archivo en conflicto aparecera de al siguiente manera

<<<<<<< HEAD
Cambios desde tu rama actual
=======
Cambios desde la rama que estás intentando fusionar
>>>>>>> rama-secundaria

De esta manera tu tendras que aceptar el cual de los cambios quieres, si el cambio
que hay ahora mismo en la rama en la que estas on el cambio que quieres fusionar tu

Así tendrias que solucionar todos los conflictos uno a uno.
