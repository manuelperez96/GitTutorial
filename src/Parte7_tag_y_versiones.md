# Tags y versiones en git
Las tags son indicativos que podemos usar para determinar un nombre para una versión concreta del proyecto.

Cuando hacemos git log, sale algo así:
```shell
commit f260f5bb823630c3aa32e3be056f7fa167a0a678 (HEAD -> main, origin/main)
Author: Manuel <perez.soto.manuel@hotmail.com>
Date:   Fri Apr 8 12:19:21 2022 +0200

    Added parted 6 and added more command to Parte2

commit 5000821939aea15254601665a79b55f8c697e1ab
Merge: 4172f2a e2bf56a
Author: Manuel <perez.soto.manuel@hotmail.com>
Date:   Fri Apr 8 11:57:27 2022 +0200
```

Después de la palabra commit viene el nombre de la versión de ese instante en el proyecto. Ese nombre es autogenerado por git. 

Nosotros podemos cambiar ese nombre y darle un tag/etiqueta específicos. Por ejemplo, le podríamos dar el nombre de **v.0.1**, para indicar que es esa versión del proyecto. Esto suele ser más útil en repositorios remotos, que en repositorios locales.

```shell
# Muestra todos los tags que haya en local.
git tag

# Añade un tag a una versión específica del proyecto, determinada por 
# el id del commit.
git tag nombre_tag identificador_commit

# Sube al repositorio remoto los tags en local
git push origin --tags

# Elimina del repositorio local (no del remoto) un tag.
git tag -d nombre_tabgit

# Elimina del repositorio remoto (no del local) un tag.
git push origin :refs/tags/nombre_tag
```