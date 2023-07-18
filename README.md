# Comandos Basicos
* git init . : Crea el repositorio vacio en el que estas posicionado en github. Tambien sirve para convertir un proyecto existente y sin versión en un repositorio de Git.
* git add * . : Guarda todos los cambios en la rama actual.
* git add (nombre archivo) . : Guarda los cambios del archivo en la rama actual.
* git commit -m "Comentario" : Realizar un commit con un comentario.
* git restore . : Descartar los cambios localmente (no commiteados).
* git restore --staged <file> : Descartar un archivo no commiteado.
* git pull : Bajar los cambios de la rama en la que estas posicionado.  

## Comandos para el uso de ramas
* git checkout -b nombre-nueva-rama : Crear una nueva rama.
* git checkout "nombre-de-rama" : Cambiarse de rama.
* git push origin "nombre-rama" : Subir un commit a la rama especificada.
* git branch : Devuelve todas las ramas y la que esta en uso en un color diferente.
  
# Comandos mas avanzados
* git show (codigo de commit) : Muestra los cambios agregados en el commit
* git log : Muestra el historial de commits realizados al repo.
* git log --oneline : Muestra lo mismo que el git log pero abreviado.
* esc:wq : Salir del modo insertar de la consola.
* git remote add origin (origen repo) : Añadir el origen del repo de forma remota.

## Mergear una rama con la tuya (combinar)
Pasos:
<p>git checkout rama-a-mergear -> Cambiarse a la rama a mergear</p>
<p>git pull -> Bajarse todos los cambios de la rama</p>

<p>git checkout tu-rama -> Cambiarte a tu rama</p>
<p>git merge rama-a-mergear -> Mergear la rama con la tuya</p>
