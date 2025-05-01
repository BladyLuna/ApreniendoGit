#       Mis Inicios Aprendiendo Git
##  Que es git?
 Es un Sistema de control de versiones donde un pilar importante son los repositorios en el que se almacena los ficheros de un proyecto (fichero == es  como una coleccion ordenada).
 los repositorios pueden ser locales o remotos.
 los remotos tienen la peculiaridad de que otras personas puede hacer cambios en el proyecto, y que estos cambios sean visibles y sean sincronisados por otras personas.
##Pilares fundamentales de GIT
a. merge: consiste en combinar los cambios de una bifurcacion con otra rama
(bifurcacion == punto donde se dividen a dos ramas o mas )
b. push: consiste en empujar o subirlo nuestros cambios locales al servidor(nube).
c. pull: de manera analoga o similar es la accion inversa(trae los cambios de nuestro repositorio remoto a el repositorio local).


##  INSTALACION DE GIT EN LINUX
1. la instalacion es con este bash
sudo apt-get install git
2. para comprobar la instalacion de git
git --version

##  CONFIGURAR NOMBRE Y CORREO
1. configurar nombre y correo
```bash 
git config --global user.name "name"
```
```bash
$ git config --global user.email "correo"
```








