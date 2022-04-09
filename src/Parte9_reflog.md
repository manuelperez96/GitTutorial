# Recuperando lo "borrado"
Una cosa interesante de Git, es que nunca jamás se borra nada. Todos los cambios permanecen, aunque estén ocultos dentro del repositorio local.

Existe un comando muy útil, llamado `git reflog`, que te permite ver todo lo que has realizado hasta la fecha y, recuperar por ejemplo, ramas que has eliminado, si se utiliza junto al comando `git reset`.

# git reflog
Este comando te muestra una lista de todos lo que has realizado en git. Incluyendo ramas borradas.

La salida del comando muestra algo así:
```
13fddc9 (HEAD -> main) HEAD@{0}: commit: delete testing file
13547d3 HEAD@{1}: commit: Adding reflog
7579cee HEAD@{2}: reset: moving to HEAD
7579cee HEAD@{3}: commit: Change Parte7_stash for Parte8
4764ed0 HEAD@{4}: commit: First version of Parte7
234d31c (origin/main) HEAD@{5}: commit: Added more information
1a94e76 HEAD@{6}: commit: Added info to Parte7
```

Para volver a un punto donde todo era correcto, solo tenemos que hacer `git reset HEAD@{1}`.