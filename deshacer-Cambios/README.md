# Deshacer cambios
## en que casos deshacemos cambios
1. deja de funcionar proyectos
2. queremos recuperar una parte del codigo eliminado
3. recuperar archivos eliminados
## comandos destructivos
## Comandos destructivos
>[!IMPORTANT]
>Estos pueden llegar a alterar el historial de commits. Lo opuesto serían los no destructivos, estos >trabajan en base al historial sin afectarlo, se basan en este para crear nuevos commits.

| Comando | Descripción |
|---|---|
| `git reset --soft <id_commit_que_quieres_ir>` o <br> `git reset --soft HEAD~<tu_numero_de_commit>` | Mantiene los cambios que ocurrieron antes de hacer commit de donde apunta. Quita la capacidad de volver a puntos futuros. |
| `git reset --hard <id_commit_que_quieres_ir>` o <br> `git reset --hard HEAD~<tu_numero_de_commit>` | Descarta todos los cambios. Quita la capacidad de volver a puntos futuros. |
| `git commit --amend -m "<nuevo mensaje para el commit>"` | Este comando cambia el mensaje del último commit realizado. |
| `git push -f <nombre_repo_remoto> <rama_a_subirse>` | Fuerza a sincronizar los cambios con el repositorio remoto (no recomendado). |

## comandos no destructivos
>[!IMPORTANT]
> no cambian el historial del los commits

| Comando | Descripción |
|---|---|
| `git revert HEAD~<numero_de_commit>` o <br> `git revert HEAD <id_commit>` | Revierte los cambios que un commit introdujo y crea uno nuevo con los cambios revertidos. |
| `git revert --abort` | Aborta el revert. |
| `git revert --continue` | Continua con el revert luego de solucionar conflictos. (si es que hubiese) |
| `git checkout <id_commit>` | Con este comando podemos volver a una etapa anterior de nuestro código, ahí podrás observar como se encontraba tu código en ese commit. |
| `git checkout <id_commit> <archivo_a_recuperar>` | Puede traer un archivo en específico del pasado y agregarlo en el presente. |