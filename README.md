# Comandos git


## INICIAR PROYECTO 
 
* Para iniciar un proyecto GIT necesitamos ir, a travez de la consola, a la carpeta del proyecto. Luego ejecutar:
``` 
git init
```


## AGREGAR ARCHIVOS AL STAGING Y/O REPOSITORIO
 
* Para enviar los nuevos archivos al staging:
``` 
git add <nombre_archivo,...>
```

* Para enviar todos los nuevos archivos al staging:
```
git add .
```

* Para guardar los cambios en el repositorio se usa:
```
git commit -m "<Comentario>"
```

* Para agregar al staging las modificaciones de archivos anteriomente agregados y guardar cambios en el repositorio
```
git commit -am "<Comentario>"
```

## ESTADO Y/O CAMBIOS / DIFERENCIAS 
 
* Luego de hacer cambios y/o crear nuevos archivos podemos ver el estado con:
```
git status
```
	
* Para ver los ultimos cambios
```
git show
```
	
* Para ver las diferencias actuales
```
git diff
```

* Para ver el historial de los commits
```
git log
```

* Para ver el historial de los commits resumidos
```
git log --oneline
```

	
## CONFIGURACIONRES GENERALES

* Para configurar el user:
```
git config --global user.name "<Nombre>"
```

* Para configurar el email:
```
git config --global user.email "<Email>"
```

* Para ver la configuracion actual:
```
git config --list
```


## REPOSITORIO REMOTO

* Para agregar nuestro proyecto a un repositorio remoto:
```
git remote add origin <url>
```

* Para ver el repositorio remoto:
```
git remote --v
```

* Para enviar y crear la rama en el repositorio remote:
```
git push -u <remoto> <rama_local>
```

Luego de ejecutar este la primera vez pedira autentificacion.
Si su repositorio esta en GitHub se debe generar un token, en ves de poner user y pass, se coloca user y token.

* Para enviar cambios:
```
git push <remoto> <rama_local>
```

* Para enviar todas las ramas:
```
git push --all
```

* Para obtener los commit del repositorio remoto:
```
git fetch <remoto> <rama_local>
```

* Para obtener y unir los cambios del remoto al local
```
git pull <remoto> <rama_local>
```

* Para obtener y unir los cambios de todas las ramas del remoto al local
```
git pull --all
```

* Para cambiar la url del repositorio
```
git remote set-url origin repository-link.com
```


 ## RAMAS

* Para ver las ramas:
```
git branch
```

* Para crear una rama: 
```
git branch <nombre>
```

* Para moverte de una rama a otra:
```
git checkout <nombre>
```

* Para crear y moverte a la vez de una rama a otra:
```
git checkout -b <nombre>
```

Tener en cuenta que si cambiamos de rama sin agregar los cambios al staging, estos podrian perderse.

* Para unir ramas, posicionarte en la rama donde quieres insertar los cambios y ejecutar:
```
git merge <rama>
```


 ## MOVERSE A OTRO COMMIT

* Para moverte a un commit:
```
git checkout <id_commit>
```

* Para resetear el historial a un commit borrando el staging actual
```
git reset <id_commit> --hard
```


* Para resetear el historial a un commit dejando el staging actual
```
git reset <id_commit> --soft
```

* Volverl al último commit 
```
git checkout master  
```
 
