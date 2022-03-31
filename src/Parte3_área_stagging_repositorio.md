# Área temporal y repositorio
Cuando usamos el comando git init, este entre otras cosas, nos crea una carpeta llamada `.git`. En dicha carpeta, que actúa como **repositorio** se almacena la información de las diferentes versiones de la aplicación. Además, también nos crea un área en memoria RAM, llamada **stagging**, en la cual se almacenan los cambios del proyecto temporalmente.

Esta área temporal, stagging, nos sirve para ir almacenando tantos cambios como queramos, sin necesidad de tener que hacer un commit. Además, dichos cambios son temporales y no están grabados en el repositorio, por lo que podemos eliminarlos o ir añadiendo más y más cambios, que se irán acumulando. 

Añadir cambios a esta área lo podemos hacer con `git add` y removerlo, con `git rm`.

Cuando estemos satisfechos con los cambios, podemos usar el comando `git commit` para almacenar dichos cambios en el repositorio, con un nombre para dicha *versión*.