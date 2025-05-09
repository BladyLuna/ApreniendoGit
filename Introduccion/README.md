#       Mis Inicios Aprendiendo Git<img src="../img/logo-git.png" width="70" height="70" />
##  Que es git?
 Es un Sistema de control de versiones donde un pilar importante son los repositorios en el que se almacena los ficheros de un proyecto (fichero == es  como una coleccion ordenada).
 los repositorios pueden ser locales o remotos.
 los remotos tienen la peculiaridad de que otras personas puede hacer cambios en el proyecto, y que estos cambios sean visibles y sean sincronisados por otras personas.
## Pilares fundamentales de GIT
a. merge: consiste en combinar los cambios de una bifurcacion con otra rama
(bifurcacion == punto donde se dividen a dos ramas o mas )
b. push: consiste en empujar o subirlo nuestros cambios locales al servidor(nube).
c. pull: de manera analoga o similar es la accion inversa(trae los cambios de nuestro repositorio remoto a el repositorio local).

## Que es una rama?
![univeros](../img/universo.png) 
es una collecion de directorios y archivos del repositorio.
apartir de esta rama puedes crear mas ramas. tambien puedes integrar los cambios hechos en un fichero se integren a la rama principal a esto se le llama merge(fucionar).
## Para que sirven las ramas?
en un entorno colaborativo las personas de tu equipo pueden estar trabanjando en diferentes partes del proyecto bugs, desarrollando , documentacion entonces todo eso se integrar a la rama principal.

## Que representa la rama Master o Main?
lo importante es que un repositorio necesita tener una rama principal independiente a su nombre.


##  INSTALACION DE GIT EN LINUX
1. la instalacion es con este bash
```bash
sudo apt-get install git
```
2. para comprobar la instalacion de git
```bash
git --version
```

##  CONFIGURAR NOMBRE Y CORREO
1. configurar nombre y correo
```bash 
git config --global user.name "name"
```
```bash
$ git config --global user.email "correo"
```

2. para ver la configuracion de tu git
```bash
 git config --list
```

3. para cambiar la configuracion de un repositorio(fichero) en concreto solo quitas el --global.
cambias de usuario para hacer el respectivo push o pull.
ejemplo:
```bash
cd /direcion/de/repositorio
 git config user.name "name"
 git config user.email "correo"
```

##  CONFIGURAR EL EDITOR DE CODIGO QUE ABRE GIT
por defecto abres lo ficheros con vin pero puedes cambiarlos.
para configurar un editor por defecto para que abra el editor de texto:
 para vs code:
```bash
 git config --global core.editor "code"
```

 para Atom,sublime text, nano. es muyy similar
```bash
  git config --global core.editor "Sublime Text"
```
    COMPROBAR LAS CONFIGURACIONES DE GIT
ver las configuraciones
```bash
 git config --list
```
##   COMO INICIALIZAR UN NUEVO PROYECTO
un repositorio solo puedes tener una rama activa a la ves ,pero puedes tener varias ramas principales
1. creacion de una carpeta local
```bash
 git init name-proyecto
 cd nuevo-proyecto
```
2. para iniciar el proyecto debes estar dentro la raiz de directorio eso quiere decir estar dentro de la carpeta y iniciarlo con el bash:
```bash
 git init
```
3. crear una rama principal o carpeta para un repositorio y iniciarlo
ejemplo:
```bash
git init nameCarpeta --initial-branch=nameDirectorio
para revisar las ramas de nuestro repositorio
 git branch
si la rama tiene por delante un * indica que esta activa.
```

4.cambiar nombre de la rama principal que usa por defecto
```bash
 git config --global init/defaultBrach nameRepositorio
```
(aun falta entender el 4 aaaaaa!)







