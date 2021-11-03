# Comandos git
</br>

### INICIAR PROYECTO 
 
* Para iniciar un proyecto GIT necesitamos ir, a travez de la consola, a la carpeta del proyecto. Luego ejecutar:
</br>```git init```

</br>

### AGREGAR ARCHIVOS AL STAGING Y/O REPOSITORIO
 
* Enviar los cambios y nuevos archivos al staging:
</br>```git add <archivo,...>```

* Enviar todos los cambios y nuevos archivos al staging
</br>```git add .```

* Guardar los cambios en el repositorio local:
</br>```git commit -m "<Comentario>"```

* Agregar al staging las modificaciones de archivos anteriomente agregados y guardar cambios en el repositorio local
</br>```git commit -am "<Comentario>"```

* Remover archivo
</br>```git rm --cached <archivo>```

</br>

### ESTADO Y/O CAMBIOS / DIFERENCIAS 
 
* Ver el estado
</br>```git status```
	
* Ver los ultimos cambios
</br>```git show```
	
* Ver las diferencias actuales
</br>```git diff```

* Ver el historial de los commits
</br>```git log```

* Ver el historial de los commits resumidos
</br>```git log --oneline```

</br>

### CONFIGURACIONRES GENERALES

* Configurar el user:
</br>```git config --global user.name "<Nombre>"```

* Configurar el email:
</br>```git config --global user.email "<Email>"```

* Ver la configuracion actual:
</br>```git config --list```

</br>

### REPOSITORIO REMOTO

* Agregar nuestro proyecto a un repositorio remoto:
</br>```git remote add <rama_romota> <url>```

* Ver el repositorio remoto:
</br>```git remote --v```

* Enviar y crear la rama en el repositorio remote:
</br>```git push -u <rama_remota> <rama_local>```

Luego de ejecutar este la primera vez pedira autentificacion.
Si su repositorio esta en GitHub se debe generar un token, en ves de poner user y pass, se coloca user y token.

* Enviar cambios:
</br>```git push <remoto> <rama_local>```

* Enviar todas las ramas:
</br>```git push --all```

* Obtener los commit del repositorio remoto:
</br>```git fetch <rama_remota> <rama_local>```

* Obtener y unir los cambios del remoto al local
</br>```git pull <rama_remota> <rama_local>```

* Obtener y unir los cambios de todas las ramas del remoto al local
</br>```git pull --all```

* Cambiar la url del repositorio
</br>```git remote set-url origin repository-link.com```

</br>

### RAMAS

* Ver las ramas:
</br>```git branch```

* Crear una rama: 
</br>```git branch <nombre>```
   
* Renombrar rama actual
</br>```git branch -m <nombre>```

* Borrar rama
</br>```git branch <rama_local> -d``` 

* Moverte de una rama a otra:
</br>```git checkout <nombre>```

* Crear y moverte a la vez de una rama a otra:
</br>```git checkout -b <nombre>```

Tener en cuenta que si cambiamos de rama sin agregar los cambios al staging, estos podrian perderse.

* Unir ramas, posicionarte en la rama donde quieres insertar los cambios y ejecutar:
</br>```git merge <rama>```

</br>

### MOVERSE A OTRO COMMIT

* Para moverte a un commit:
</br>```git checkout <id_commit>```

* Rresetear el historial a un commit borrando el staging actual
</br>```git reset <id_commit> --hard```


* Resetear el historial a un commit dejando el staging actual
</br>```git reset <id_commit> --soft```

* Volverl al último commit 
</br>```git checkout master```
 
