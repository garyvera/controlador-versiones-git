# Tarea 1
## Comandos de git
* Comandos básicos de git
* Comandos avanzados de git
### Comandos básicos de git
#### `git config --global user.name` "Gary Vera"
Permite crear un usuario de manera global, en la configuración inicial del cliente, para identificar los cambios realizados en git
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
La salida en consola utilizado el comando `git init` es la siguiente:
```
git init
Initialized empty Git repository in H:/Mi unidad/MDW101 CONTROLADOR DE VERSIONES/mi-primer-repo/.git/
```

#### `git status`
Permite revisar los cambios realizados en los archivos del repositorio 
La salida en consola utilizado el comando `git status` es la siguiente:   
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
