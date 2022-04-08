# ¿Qué es y por qué usar un sistema de control de versiones?
Un sistema de control de versiones, nos permite de forma cómoda mantener todas **las versiones** de un archivo; es decir, si quiero hacerle cambio a uno de mis documentos, en lugar de tener que copiar y renombrar ese documento como algo así: "old_nombre_document.txt", por ejemplo; puedo simplemente modificar el archivo y si necesito volver a una versión anterior del mismo, el sistema de control de versiones, me habrá mantenido la versión anterior al cambio.

## ¿Qué es Git?
Git es un sistema de control de versiones distribuido, diseñado por Linus Torvalds. Está pensando en la eficiencia y la confiabilidad del mantenimiento de versiones de aplicaciones cuando estas tienen un gran número de archivos de código fuente. Git está optimizado para guardar todos estos cambios de forma atómica e incremental.

## Ignorar archivos
Por muy cómodo y útil que sea un sistema de versiones, no siempre queremos que todos los archivos se guarden en el repositorio. Por ejemplo, ¿de qué sirve mantener el cambio de versiones de los archivos que genera un Mac por defecto? De nada.

Para evitar que ese tipo de archivos sean versionados por Git, podemos crear un archivo `.gitignore` en la carpeta del proyecto, justo a la misma altura que nuestra carpeta `.git`.

En ese archivo podemos colocar las rutas de los archivos, de los tipos de archivos, de las carpetas, etc., que no queremos que Git vigile.

### Cómo excluir archivos con gitignore
```
# Excluye todo los archivos con la extensión jpg
*.jpg 

# Excluye todos los archivos que estén dentro de la carpeta
nombre_carpeta/

# Excluye todos los archivos que se llamen igual
nombre_archivo.extensión
```
 