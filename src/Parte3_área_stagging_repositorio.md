# Áreas de git
Cuando trabajamos con Git, detectamos que tiene diferentes área de trabajo, por ejemplo, `Stagging`, en la cual se guardan los datos temporalmente.

Estas áreas representan diferentes zonas del proyecto y cada una cumple una función.

## Directorio de trabajo
Esta zona o área, es el archivo, las carpetas, las imágenes, todo, lo que está en el disco duro. Lo que persiste en memoria no volátil.
Es el proyecto en local, la versión actual del mismo.

## Stagging área
Esta área representa una localización en memoria RAM, que sirve para guardar cambios temporales de la versión actual del proyecto.

Esta zona es no permanente, por tanto, si no guardamos los cambios que haya aquí, se perderán con el tiempo, por ejemplo, al cerrar el proyecto.

## Repositorio local
Es un área donde se almacenan las diferentes versiones del proyecto. En esa área iremos guardando los cambios de `Stagging` para hacerlos permanentes.

## Repositorio remoto
Representa las versiones del proyecto alojadas en algún servidor remoto. Normalmente, es el punto de unión para todos los proyectos locales de los diferentes desarrolladores.
