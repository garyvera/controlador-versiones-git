# CONTROLADOR DE VERSIONES
## Tarea 1 de:
**Gary Ramon Vera Lucas**
## Comandos de git
* Comandos básicos de git
* Comandos avanzados de git
### Comandos básicos de git
#### `git config --global user.name` "Gary Vera"
Permite crear un usuario global, en la configuración inicial de git, para identificar los cambios realizados
 #### `git config --global user.email` garyveralucas@gmail.com
Admite crear el email de forma global en la configuración inicial en un repositorio de git
#### `git config --list`
Muestra la configuración actual de git  
La salida en consola utilizado el comando `git config --list` es la siguiente:
```
git config --list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/etc/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=false
pull.rebase=false
credential.helper=manager
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
user.email=garyveralucas@gmail.com
user.name=Gary Vera
```
#### `git init`
Inicializa un repositorio de git en el directorio actual  
La salida en consola utilizado con `git init` es la siguiente:
```
git init
Initialized empty Git repository in H:/Mi unidad/MDW101 CONTROLADOR DE VERSIONES/mi-primer-repo/.git/
```

#### `git status`
Permite revisar los cambios realizados en el repositorio   
la salida en consola utilizado el comando `git status` es la siguiente:   
```
git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.js

nothing added to commit but untracked files present (use "git add" to track)
```
> El mensaje de consola indica lo siguiente:
1. **On branch master** => Indica el nombre de la rama **main o master**
1. **No commits yet** => Archivos no rastreados
1. **Untracked files:** => Archivos sin seguimiento

#### `git add`
Este comando incluye uno o todos los archivos a seguimiento como por ejemplo:  
* `git add index.js` => agrega el archivo index.js   
* `git add .` => agrega todos los archivos 

#### `git commit`
Confirma los cambios realizados  
Esta linea de comados => `git commit -m "Primer commit"` agrega un commit 

#### `git log`
Consulta el historial de confirmaciones **commit**

#### `git diff`
Muestra los cambios realizados

#### `git branch`
Crea una nueva rama  
el siguiente comando `git branch garyvera/tarea-1-multiplicacion`
crea una rama llamada **garyvera/tarea-1-multiplicacion**

#### `git checkout`
Permite cambiar de rama  
el siguiente comando `git checkout garyvera/tarea-1-multiplicacion`
cambia a la **garyvera/tarea-1-multiplicacion**

#### `git checkout -b`
Este comado crea una rama y ademas realiza el cambio de la rama  
el formato es el siguiente: `git checkout -b garyvera-tarea-2-division`

#### `git branch --list`
Muestra las ramas del repositorio

#### `git merge`
Permite unir ramas  
Este comado `git merge garyvera-tarea-2-division `  une la rama main con  la rama  **garyvera-tarea-2-division**

#### `git tag`
Es un tipo de puntero a un commit especifico   
Este comando `git tag v0.0.1 `  crea un tag en un commit  
para listar las etiquetas se utiliza `git tag` 

#### `git tag -d`
Comando que elimina un tag   
Este comando `git tag -d v0.0.1 ` elimina el tag

#### `git push origin` 
Este comando `git push origin 0.0.1 ` sube el tag al repositorio 

### Comandos avanzados de git
#### `git rebase`
Modifica el historial de un commit (cambia la base de una rama mas el cambio de la otra) y ademas brinda un historial mejor detallado   

#### `git rebase -i`
Este comado mas el hash del commit muestra las siguiente salida 

```
# Commands:
# p, pick <commit> = use commit
# r, reword <commit> = use commit, but edit the commit message
# e, edit <commit> = use commit, but stop for amending
# s, squash <commit> = use commit, but meld into previous commit
# f, fixup [-C | -c] <commit> = like "squash" but keep only the previous
#                    commit's log message, unless -C is used, in which case
#                    keep only this commit's message; -c is same as -C but
#                    opens the editor
# x, exec <command> = run command (the rest of the line) using shell
# b, break = stop here (continue rebase later with 'git rebase --continue')
# d, drop <commit> = remove commit
# l, label <label> = label current HEAD with a name
# t, reset <label> = reset HEAD to a label
# m, merge [-C <commit> | -c <commit>] <label> [# <oneline>]
#         create a merge commit using the original merge commit's
#         message (or the oneline, if no original merge commit was
#         specified); use -c <commit> to reword the commit message
# u, update-ref <ref> = track a placeholder for the <ref> to be updated
#                       to this position in the new commits. The <ref> is
#                       updated at the end of the rebase
#
# These lines can be re-ordered; they are executed from top to bottom.
#
# If you remove a line here THAT COMMIT WILL BE LOST.
#
# However, if you remove everything, the rebase will be aborted.

```
Listamos las aprendidas en clases:
* r, reword : cambia la descripción del commit
* s, squash : fuciona las descriciones de los commit  
* f, fixup : al unirse se pierde toda referencia del commit sola queda una referencia 

#### `git show`
Consulta los cambios de un commit

#### `git stash`
Este comando permite realizar cambios temporales que se almacenan en una pila sin nesecidad de hacer un commit 

#### `git stash list`
Muestra los cambios temporales en la pila

#### `git stash pop`
Trae y borra los ultimos cambios en la pila **vuele a la ultima modificacion de un archivo**

#### `git stash apply stash@{0}`
Aplica cambio sin eliminarlos

#### `git stash pop stash@{0}`
Elimina en la pila

#### `Git checkout  -- .`
Borra los datos de la pila no se puede recuperar

#### `git cherry-pick`
Selecciona un commit y lo copia en otra rama  

#### `git revert` 
Crea un commit de un cambio realizado en otro commit

#### `rm -rf .git >` 
Reinica el repositorio 

#### `git commit amend` 
Edita el mensaje del commit en local

#### `git blame` 
Consulta todos los commits realizados en un archivo `git blame nombre de archivo` 
