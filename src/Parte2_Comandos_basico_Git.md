# Git - Comándos básicos
Git es realmente potente. Para poder utilizarlo hará falta descargarlo (desde la página web) e instalarlo.

## git init
Este comando inicializa un repositorio local de Git, el cual irá almacenando los cambios de los archivos que le expecifiquemos.
Este comando debe ejecutarse en la terminal y creará una carpeta llamada ".git" en el directorio actual donde esté la terminal.

## git status
Este comando muestra información actual sobre los cambios que se han realizado en el proyecto y no se han guardado. Por ejemplo, si se ha modificado algún archivo, te saldrá con este comando.

## git add
Este comando permite añadir al area de stagging los cambios realizados en los archivos, para posteriormente guardarlo.

```shell
# Añade solo un archivo por su nombre
git add archivo.txt

# Añade todo los archivos del directorio actual
# y de los directorios internos.
git add .
```
##git rm
Este comando nos permite eliminar archivos del disco duro o del área de stagging. Es importante usarlo con cuidado. El qué elimine dependerá de los parámetros que usemos con el comando.

Puede ser útil cuando hemos hecho un add de un archivo o archivos, que realmente no queríamos guardar.

```shell
# Elimina el archivo del disco y del repositorio de git
git rm nombre_archivo.txt

# A veces es necesario forzar la eliminación.
git rm nombre_archivo.txt -f

# Si solo queremos eliminar el archivo del repositorio de Git
git rm nombre_archivo.txt --cached
```
Como dato curioso si queremos usar este comando para eliminar un archivo, dicho archivo deberá haber sido añadido al área de stagging con el comando add, previamente.

## git commit
Este comando almacena los datos que están en el área de stagging, de forma que creamos una **versión nueva** del fichero y la almacenamos en el repositorio, para poder volver a ella en cualquier momento.

``` shell
# Creamos un commit y le añadimos un mensaje al mismo.
git commit -m "mensaje descriptivo"

# Traqueamos todos los cambios realizados y hacemos commit.
# Es la fusión de add + commit
git commit -am "mensaje descriptivo"

# Con este comando fusionamos el commit actual con el anterior,
# de forma que en el anterior commit se añaden todos los cambios 
# realizados en los dos commits.
git commit --amend
```

## git config
Este comando nos muestra información referente a la configuración de git y el repositorio actual.

Si lo usamos sin parámetros, nos muestra la lista de opciones que le podemos pasar al comando.

```shell
# Muestra todas las opciones disponibles para el comando
git config

# Muestra la configuración actual de git 
git config --list

# Muestra la configuración actual de git y donde están almacenadas
git config --list --show-origin
```

Es necesario que configuremos nuestro nombre de usuario e email para Git, sino nos intentará coger el que tenga la máquina por defecto y en caso de no tenerlo, no nos dejará hacer commits.

Dichos datos se pueden configurar de forma global o local para cada repositorio.

```shell
# Configuración global (para todos los repositorios)
# del nombre y el email de git.
git config --global user.name "Nombre Usuario"
git config --global user.email "nombre@usuario.com"

# Configuración local (para el repositorio actual)
# del nombre y el email de git.
git config user.name "Nombre Usuario"
git config user.email "nombre@usuario.com"
```
## git log
Este comando nos muestra información del repositorio, como por ejemplo, el número de commit realizados, el nombre de dichos commits, etc.

El siguiente código es un ejemplo de cómo se mostraría la información cuando se ejecuta el comando.
```shell
commit 5d50de9a1f127b723badcf51c8fe77b5351f6ea5 (HEAD -> master)
Author: Manuel <perez.soto.manuel@hotmail.com>
Date:   Sun Mar 27 16:28:56 2022 +0200

    Added first and second part
```
En la primera línea, nos encontramos identificador/tag del commit `5d50de9a1f127b723badcf51c8fe77b5351f6ea5`. Luego, `HEAD` que nos dice que nos encontramos actualmente en ese commit (versión del archivo). Por último, el nombre de la rama en la que estamos, `master`.

En la segunda línea, nos encontramos con información sobre el autor del commit.

En la tercera línea, cuando se realizó.

Y por último, un mensaje que el autor le dio al commit.

```shell
# Muestra información de las diferentes versiones del proyecto 
# y un indicador visual con las ramas creadas y sus merges.
git log --graph 

# Muestra información de forma reducida, para que quepa en una línea
git log --oneline
```

## git show
Muestra información sobre un tag, commit, tree, etc., de forma descriptiva.

Si no le pasamos sobre qué queremos obtener la información, nos devuelve la información de donde esté HEAD en este momento.

El formato o la información que muestra, dependerá del tipo de dato que le hayamos pasado al comando, por lo que recomiendo, leer la [documentación](https://git-scm.com/docs/git-show) para más información.

## git diff
Este comando nos permite comparar diferentes **versiones** de un repositorio. Para ello nos hará falta el identificador de la versión, que podemos obtener a través del comando git log, por ejemplo.

El comando recibe dos referencias, debemos pasarle como primera referencia la más vieja, para que nos muestre los cambios en el orden correcto.

```shell
git diff ref1 ref2
```

## git alias
Este comando nos permite hacer un alias para un comando con varias opciones. 

Por ejemplo, podemos transformar el siguiente comando `git log --oneline --graph --decorator` en `fullinfo`.

```shell
git alias fullinfo="git log --oneline --graph --decorator"
```

para usarlo, bastaría con poner en la consola fullinfo, sin ni siquiera usar la palabra git. 