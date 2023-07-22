# Comandos Basicos
* git init . : Crea el repositorio vacio en el que estas posicionado en github. Tambien sirve para convertir un proyecto existente y sin versión en un repositorio de Git.
* touch (nombre.extension) : Crea un archivo en la ubicacion actual.
* git add * . : Guarda todos los cambios en la rama actual.
* git add (nombre archivo) . : Guarda los cambios del archivo en la rama actual.
* git commit -m "Comentario" : Realizar un commit con un comentario.
* git commit -a -m "Comentario" : Realiza un add y un commit.
* git restore . : Descartar los cambios localmente (no commiteados).
* git restore --staged <file> : Descartar un archivo no commiteado.
* git pull (fetch + merge): Bajar los cambios de la rama en la que estas posicionado.
* git fetch : Descarga el contenido de la rama pero no lo une con el local. Para que se combine hay que realizar un merge.

## Comandos para el uso de ramas
* git checkout -b nombre-nueva-rama : Crear una nueva rama.
* git checkout "nombre-rama" : Cambiarse de rama.
* git push origin "nombre-rama" : Subir un commit a la rama especificada.
* git branch : Devuelve todas las ramas y la que esta en uso en un color diferente.
* git branch -d "nombre-rama": Elimina la rama especificada.
* git branch -m "nombre-nuevo” : Cambiar el nombre de la rama actual.
* git branch -m "old-name" "new-name": Cambiar el nombre de otra rama.
  
# Comandos mas avanzados
* git show (codigo de commit) : Muestra los cambios agregados en el commit
* git log : Muestra el historial de commits realizados al repo.
* git log --oneline : Muestra lo mismo que el git log pero abreviado.
* vi "nombre.extension" : Muestra y permite editar un archivo.
* esc:wq : Salir del modo insertar de la consola.
* ls -a : Muestra todos los archivos en la carpeta actual (incluyendo los ocultos).
* git remote add origin (origen repo) : Añadir el origen del repo de forma remota.
* git commit --amend : Agregar un archivo a un commit. Lo agrega al ultimo commit no subido al repo. IMPORTANTE: antes hay que hacer un add

## Mergear una rama con la tuya (combinar)
* git merge --abort : Abortar el merge (en caso de que te arrepientas)
Pasos:
<p>git checkout rama-a-mergear -> Cambiarse a la rama a mergear</p>
<p>git pull -> Bajarse todos los cambios de la rama</p>

<p>git checkout tu-rama -> Cambiarte a tu rama</p>
<p>git merge rama-a-mergear -> Mergear la rama con la tuya</p>

## Hacer pull rebase (organizar commits)
* git pull --rebase : Hace un pull pero ordenando los commits cuando hace el merge, de forma que no sea necesario hacer un commit auxiliar para unir ambos commits de forma recursiva.
* Generalmente se puede utilizar cuando mas de una rama hizo cambios al mismo tiempo y se tiene que realizar un merge.
* Es recomendable NO UTILIZARLO con commits pusheados, es decir con commits subidos al master o una rama porque el rebase destruye el historial de commits. 
