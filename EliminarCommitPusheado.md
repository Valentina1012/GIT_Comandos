# EliminarCommitPusheado
## El repo local y el remoto tienen que estar sincronizados
<p>Primero hay que destruir el commit localmente con:</p>
<p><b>git reset HEAD^ --hard</b>  (HEAD es el id del commit anterior al que queremos borrar)</p>
<p>y a continuación forzando los cambios al repositorio remoto de origen con:</p>
<p><b>git push origin -f</b></p>

### Explicación
<p>En condiciones normales un push al origen falla si el commit que está "arriba" no es un ancestro del commit que se está intentado hacer. Es decir, si el repo remoto va por delante del repo local. Con el parámetro -f (o --force que es lo mismo) forzamos a que esta comprobación no se haga. Esto puede tener efectos destructivos y que se pierdan los commits que van por delante de nosotros, cosa que es justo lo que queremos en este caso: con la instrucción reset estamos situados en un commit inmediatamente anterior al último y con el push forzado estamos haciendo que éste desaparezca.</p>
