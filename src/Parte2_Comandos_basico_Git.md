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
