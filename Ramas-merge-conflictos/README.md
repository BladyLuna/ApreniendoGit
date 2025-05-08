# RAMAS, MERGE Y CONFLICTOS

## Que es una rama?

son una instantanea (snapshot) de la division de codigo de distintos estados.
snapshot: copia del estado 
es un apuntador hacia una de la confirmaciones.

![que es una rama](img/que-es-una-rama.png)

## Para que sirven las ramas?
 permiten realizar un desarrollo no lineal y colaborativo.

## Como Usar nuetras ramas?
![creacion de ramas](img/creacion-de-ramas.png)


### el comando git branch nos permite crear , listar, eliminar, renombrar ramas. 

1. creacion de una rama
bash
git branch miprimeraRama

2. cambiamos de rama con:
bash
git switch mi-primera-rama
Switched to branch 'mi-primera-rama'


3. quieres crear y dirigirte o cambiar puedes hacer:
bash
git switch -c mi-primera-rama

4. eliminar una rama
bash 
git branch -d mi-pimera-rama

5. Listar ramas disponibles 
solo una puede estar activa y se ve * antes del nombre es que estas trabjando ahi 
bash
git branch
git branch --show-current
git branch --sort=committerdate

## Como usar Checkount?
### se lo cambio por el switch
vemos que git checkout cambia entre ramas y restaura el directorio del trabajo
nota: no hace bien su trabajo segun la filosofia de Unix.
bash
git checkout

# Fucionar ramas
