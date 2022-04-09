# Stash
A veces, tenemos cambios guardado en el área de Stagging, pero por cualquier razón no son cambios suficientes para almacenarlos en el repositorio, es decir, hacer un commit.

Para ese tipo de casos, podemos usar una nueva área llamada Stash, que almacena los cambios en stagging para poder, por ejemplo, cambiar de rama, sin perderlos. También podemos usar esta área para resetear todos los cambios que hemos hecho y que están almacenados en el área de stagging, sin perderlos.

```shell
# Este comando almacena los cambios en stagging en el área
# stash.
git stash

# Te muestra la lista de cambios almacenados en stash.
git stash list

# Restablece los cambios que estén en stash, 
# al área de stagging.
git stash pop

# Transforma los cambios almacenados en stash
# a una nueva rama.
git stash branch branch_name

# Elimina los stash almacenados.
git stash drop
```
