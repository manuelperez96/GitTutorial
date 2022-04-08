# Trabajo en remoto
Una de las principales ventaja que tiene Git es que permite trabajar en equipo de forma remota. Para ello se utiliza normalmente, un servidor remoto (en la nube), que almacena una versión del proyecto que todos los desarrolladores usarán como el proyecto compartido.

Por ejemplo, mi compañero y yo, estamos trabajando en un proyecto y tenemos en GitHub (un servidor online de Git), un proyecto. Ambos usamos ese proyecto compartido para ir guardando de forma remota los cambios que hagamos en nuestro proyecto local, sin tener que saber nada del proyecto local de la otra persona ni afectarle a él directamente con nuestros cambios; ya que cada uno tiene, en local, una versión única del proyecto que irá actualizando al proyecto remoto.

Para trabajar en remoto, como he dicho hará falta un repositorio online, que se puede crear por ejemplo en GitHub, GitLab, Codeberg, etc.

Una vez creado dicho repositorio, habrá que descargárselo en local, lo que se puede hacer de diversas formas, con HTTPS o SSH. Y habrá que usar una serie de comandos, que se explicarán a continuación.

## git remote
Este comando nos sirve para gestionar la vinculación de un repositorio local con un repositorio remoto.
```shell
# Muestra el nombre de los repositorios remotos vinculados 
# con el proyecto local. 
git remote

# Hace lo mismo que git remote, pero además, muestra la dirección (url)
# de los repositorios y el tipo de vinculación: fetch y/o push.
# Fetch significa que se puede leer datos del repositorio.
# Push significa que se puede escribir datos en el repositorio.
git remote -v

# Vincula un repositorio local con un repositorio remoto.
# origin es el nombre que recibirá la dirección del repositorio remoto
# en el repositorio local, para no tener que usar la dirección completa
# cuando necesitemos interactuar con el repositorio remoto.
git remote add origin repository_address
```
