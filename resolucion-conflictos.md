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
