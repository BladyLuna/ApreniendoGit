# buenas practicas en Git
## para que sirven las buenas practicas?
1. es el estandar manejado en la mayoria de equipos desarrollo
2. resolver conflictos y problemas
3. historial de commit mas legibles
4. mejor adaptacion a un flujo de trabajo
## Cada cuanto hago un commit?
De preferencia amenudo, tipo es mejor que hagas cambios pequeños, no es bueno hacer un commit con 40 kilometros de recorrido ya que los errores que cometas seran mas dificiles de arreglas.

Esto no significa que hagas un commit de cosas sin sentido, hacelas con criterio.
Como escribo buenos commits?
Bueno hay ciertas reglas/consejos que deberias seguir para que tengas mejores commits, te dare algunos ejemplos de ellas:

## Hace tus commits en verbo imperativo.
No uses punto final ni suspensivos en tus commits.

Maximo 50 caracteres, tipo mantente en un margen cerca de 50 no pasa nada si te pasas por un poco.
Añade el contexto necesario.
Usa prefijos para especificar que tipo de commit es ejemplo:
>[!IMPORTANT]
> - feat: Una nueva característica para el usuario.
> - fix: Arregla un bug que afecta al usuario.
> - perf: Cambios que mejoran el rendimiento del sitio.
> - build: Cambios en el sistema de build, tareas de despliegue o instalación.
> - ci: Cambios en la integración continua.
> - docs: Cambios en la documentación.
> - refactor: Refactorización del código como cambios de nombre de variables o funciones.
> - style: Cambios de formato, tabulaciones, espacios o puntos y coma, etc; no afectan al usuario.
> - test: Añade tests o refactoriza uno existente.

## como hago buenos nombres de la ramas?

Se consistente al crear tus nombres de rama, ademas es recomendable describir el proposito de la rama en esta ejemplo:
>[!WARNING]
>feature/add_new_class