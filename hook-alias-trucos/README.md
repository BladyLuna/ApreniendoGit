#  hooks

## que son los hooks?
es una especie de automatisacion qie ocurrira en determinados eventos.
eso nos da control y personalisacion de git 
Hooks del lado del cliente:
Solo afectan al repositorio local en el que estan y su mayor desventaja es que sus acciones solo ocurriran para ti, siendo que tu equipo no tendra estos beneficios.

Tipos de hooks:

1. pre-commit
2. prepare-commit-msg
3. commit-msg
4. post-commit
5. pre-push
6. post-checkout y post-merge
7. 
**Cómo añadir un hook local:**

1.  **Habilitar archivos ocultos:** Ve a la carpeta de tu proyecto.
2.  **Acceder a la carpeta `.git`:** Entra en esta carpeta crucial.
3.  **Ir a la carpeta `hooks`:** Aquí encontrarás ejemplos.
4.  **Crear y configurar un hook:**
    * Copia un archivo `.sample` y renómbralo al nombre del hook deseado (ej., `pre-commit`).
    * Edita el archivo con el código necesario para tu hook.
5.  **Eliminar la extensión `.sample`:** Haz que el archivo sea ejecutable.

>[!NOTE]
>  Los hooks locales no se comparten automáticamente. Debes pasar el archivo a otros para que lo añadan a su carpeta `hooks`.

## GitHub Actions (Hooks del Servidor)

GitHub Actions permite automatizar tareas en tu repositorio remoto, funcionando como hooks del servidor. Puedes usar acciones preexistentes desde la pestaña "Actions" de tu repositorio en GitHub.

## Alias en Git

Los alias son atajos para comandos de Git.

**Cómo crear un alias:**

```bash
git config --global alias.<nombre_alias> <comando_a_ejecutar>
```
## Trucos de Git:

1. git stash: Guarda cambios temporales sin commit.

2. git bisect: Detecta el commit que introdujo un bug.