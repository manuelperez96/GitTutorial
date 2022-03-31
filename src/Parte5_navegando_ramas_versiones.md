# Navegando entre ramas y versiones
El tema de las ramas y versiones está muy bien, todo sea dicho, pero ¿qué pasa cuando quiero navegar entre ramas o entre versiones? ¿Cómo lo hago?

Existen diferentes formas de hacerlo y cada una tiene sus ventajas o inconvenientes. Vemos algunas de ellas.

## git reset
Este comando nos permite "resetear" la versión actual de una rama a un commit anterior. Para ellos le tienes que pasar el identificador de dicha versión, que se puede obtener con el comando `git  log`.

Se usa principalmente con tres opcions `hard`, `mixed` y `soft`.
* **soft**:
  * "Elimina" los commits posteriores al commit al que estás haciendo el reset.
  * Conserva los cambios en el stage área.
  * Conserva los cambios que tengas en tus archivos (working directory).
* **mixed**:
  * "Elimina" los commits posteriores al commit al que estás haciendo el reset.
  * Deshace los cambios en el stage área.
  * Conserva los cambios que tengas en tus archivos (working directory).
* **hard**:
  * "Elimina" los commits posteriores al commit al que estás haciendo el reset.
  * Deshace los cambios en el stage área.
  * Deshace los cambios que tengas en tus archivos (working directory).

El principal uso que le vamos a dar a reset es eliminar versiones para volver a un punto anterior del proyecto. Esto lo haremos cuando los cambios que hemos aplicado, no nos sean de utilidad y no nos importe perderlos.

Hay que tener en cuenta que solo la opción `hard`, modifica los archivos realmente, las otras dos opciones, solo elimina la versión de git log y/o los cambios guardados en el stage área, pero no los archivos reales.

```shell
# Restaura los archivos del directorio de trabajo 
# a la versión indicada y elimina los commits posteriores.
git reset --hard identificador
```

## git checkout
Este comando nos permite "viajar al pasado", es decir, volver a una versión anterior del proyecto, sin eliminar las versiones posteriores, a diferencia de `git reset`.

Para poder hacer la navegación seguimos necesitando el identificador de dicha versión que podemos obtener con `git log`.

```shell
# Todo el proyecto viaja a la versión anterior, indicada por el identificador
git checkout identificador

# El archivo especificado viaja a la versión anterior, 
# indicada por el identificador
git checkout identificador archivo

# Restaura el proyecto a la versión más reciente
git checkout branch_name
```

Si cuando hemos "viajado al pasado", modificamos algo y hacemos un commit, destruiremos todas las versiones posteriores a esa versión.