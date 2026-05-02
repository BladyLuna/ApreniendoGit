# 🚀 INICIO RÁPIDO: GIT & GITHUB 🚀

> *Mi resumen de 8 días aprendiendo Git desde cero*

---



# Día 1: Finalmente entiendo qué es Git

Honestamente, cuando empecé a aprender Git pensé que era complicadísimo. Pero después de estos primeros días, todo tiene sentido.

## ¿Qué es Git realmente?

Git es un **sistema de control de versiones**. En palabras simples: es como tener puntos de guardado en un videojuego, pero para tu código. Si algo se daña o quieres volver atrás, simplemente cargas una versión anterior.

### Una historia que lo explica mejor

Imagina que Linus Torvalds estaba creando Linux y recibía correos de mil personas diciendo "hey, aquí tengo una mejora". Tedioso, ¿verdad? Usaba BitKeeper para gestionar eso, pero un día se enojó porque no podía seguir usándolo. Así que en 10 días, **Linus creó Git por pura frustración**. Y ahora lo usa toda la industria. Moraleja: a veces la enojo produce cosas increíbles.

## Instalando Git (finalmente)

La mayoría de ustedes probablemente ya lo tiene instalado, pero por si acaso:

### Si estás en Linux (Debian/Ubuntu)
```bash
sudo apt install git
```
Y listo, ya está.

### Si estás en Windows
1. Descarga el instalador en [git-scm.com/downloads](https://git-scm.com/downloads)
2. Dale click, click, siguiente, siguiente... (deja todo por defecto la primera vez)
3. Abre la terminal y prueba

### Si estás en Mac
```bash
brew install git
```
O descarga el instalador si prefieres la GUI.

## Los primeros comandos que necesitas

Después de instalar, verifica que esté funcionando:
```bash
git version
```

Luego, lo más importante: **dile a Git quién eres**. Es para que cuando hagas cambios, Git sepa que fuiste tú:

```bash
git config --global user.name "Tu Nombre Aquí"
git config --global user.email "tu@email.com"
```

Si quieres ver todo lo que configuraste:
```bash
git config --global --list
```

## Mi primer repositorio

La parte que más me gustó fue crear mi primer repositorio. Es sorprendentemente simple:

1. Crea una carpeta vacía
2. Abre terminal ahí
3. Ejecuta:
   ```bash
   git init
   ```

Eso es todo. Git creó una carpeta invisible llamada `.git` donde guarda toda la magia.

Luego creas un archivo (típicamente `README.md`) y haces:

```bash
git add .
git commit -m "inicial: primer commit"
```

Y listo, guardaste tu primer punto de guardado. Sentí que había logrado algo real en ese momento.

---

# Día 2: Los 3 estados que siempre me confundían

Esto es lo que finalmente me hizo "cliquear" con Git. Git tiene exactamente **3 estados**, y todo se reduce a eso:

## Los 3 Estados (sin complicarse)

| Estado | Explicación Real |
| :--- | :--- |
| **Working** | Tus archivos en la carpeta. Git solo los observa. |
| **Staging** | Archivo de espera. Dices "quiero guardar estos cambios" |
| **Committed** | Guardado oficial. Tu punto de guardado está seguro. |

Es literal: cambias algo → lo añades al staging → lo guardas. Flujo simple.

## Los Comandos que Necesito Todos los Días

### Ver qué cambié
```bash
git status
```
Mi comando favorito. Te dice exactamente qué está roto, qué está sin guardar, qué está listo. Es como tu brújula en Git.

### "Oops, no quería haber cambiado eso"
```bash
git restore [nombre-del-archivo]
```
Lo deshace todo. Vuelve a la última versión guardada. Extremadamente útil cuando experimentas y todo se va al traste.

### "Cambié de opinión, saca eso del staging"
```bash
git restore --staged [archivo]
```
Lo saca de la lista de "cosas a guardar". Pero tus cambios siguen ahí en el archivo.

### "Guardar todo"
```bash
git add .
```
Añade todos los cambios al staging. El punto (`.`) significa "todo lo que cambié".

### El guardado oficial
```bash
git commit -m "descripción corta"
```
Aquí es donde la magia sucede. Creas un punto de guardado con un mensaje descriptivo.

## El archivo .gitignore que me salvó

Hay archivos que **nunca quiero que Git guarde**: las bases de datos locales, archivos de configuración privada, esas carpetas gigantes de `node_modules`.

Creas un archivo llamado `.gitignore` y escribes:
```
node_modules/
.env
*.log
```

Y Git simplemente los ignora. Como si no existieran.

## Commits Atómicos (lo que aprendí tarde)

Un **commit atómico** significa: un cambio pequeño y útil = un commit.

No hagas esto:
- ❌ Cambias 5 funciones, corriges bugs, refactorizas código y lo guardas TODO en un solo commit

Haz esto:
- ✅ Completa una función → commit
- ✅ Corriges un bug → commit
- ✅ Refactorizas → commit

Así, si algo sale mal, puedes volver a un punto específico sin perder todo.

## Escribiendo commits como un profesional

Resulta que existe un estándar. Los prefijos más comunes son:

| Prefijo | Significado |
| :--- | :--- |
| `feat:` | Nueva funcionalidad |
| `fix:` | Corregir un bug |
| `refactor:` | Cambio de código sin alterar funciones |
| `docs:` | Solo cambios de documentación |
| `style:` | Formato, espacios, etc. |
| `test:` | Añadir o cambiar tests |

Y un buen commit se ve así:
```bash
git commit -m "feat: agregar validación de email en login"
```

No así:
```bash
git commit -m "ARREGLÉ COSAS!!!"
```

Créanme, esos commits te odiarán en 3 meses cuando busques algo.

---

# Día 3: GitHub y esas llaves SSH misteriosas

Hasta aquí era todo local. Pero luego descubrí GitHub, y ahí es donde Git realmente brilla.

## ¿GitHub = Git?

No, no es lo mismo. Y aquí está la diferencia que finalmente entendí:

- **Git:** La herramienta en tu computadora que guarda versiones
- **GitHub:** El servidor en la nube que almacena tus repositorios

Es como la diferencia entre tu Word local y Google Drive. Uno es local, el otro es en la nube.

## Mi cuenta en GitHub

Fui a [github.com](https://github.com/) y creé una cuenta. Consejo: usa tu correo personal, no el institucional. Así tu cuenta siempre será tuya.

**Pro tip:** Después vincula tu correo de estudiante y solicita el **GitHub Student Developer Pack**. Obtienes:
- GitHub Copilot gratis
- Créditos para servidores
- Un montón de herramientas premium

Vale la pena.

## Las Llaves SSH (finalmente tiene sentido)

Esto es lo que me confundía. ¿Por qué llaves SSH?

Simples: cada vez que subes código a GitHub, no quieres escribir tu contraseña. Es tedioso y inseguro. Las llaves SSH son como una "llave digital" que tu PC le muestra a GitHub y GitHub dice "ah, eres tú, adelante."

### Cómo funciona (en 3 pasos)

**Paso 1: Generar la llave**
```bash
ssh-keygen -t ed25519 -C "tu@email.com"
```
Presionas Enter dos veces (acepta ubicación por defecto y sin contraseña adicional).

**Paso 2: Copiar la llave pública**
```bash
cat ~/.ssh/id_ed25519.pub
```
Copia TODO lo que sale (será algo como `ssh-ed25519 AAAAB3...`).

**Paso 3: Pegarlo en GitHub**
1. Vas a tu perfil → Settings → SSH and GPG keys
2. New SSH key
3. Pegas el código

Listo. Ahora tu PC y GitHub son amigos.

## Crear y Conectar Repositorios

### En GitHub (crear el repo)
1. Click en "+" (arriba a la derecha)
2. New repository
3. Le das un nombre, descripción
4. Público o privado (yo recomiendo público para aprender)
5. Click en Create

### Conectar tu código local
Si ya escribiste código en tu PC y quieres subirlo:

```bash
git remote add origin git@github.com:TU_USUARIO/TU_REPO.git
git branch -M main
git push -u origin main
```

¿Qué hace cada línea?
- Primera: "Hey Git, el servidor remoto es este"
- Segunda: "Renombra mi rama principal a `main`"
- Tercera: "Sube todo a GitHub"

### Clonar un Repositorio
Si quieres descargar un proyecto que ya existe:

```bash
git clone git@github.com:USUARIO/PROYECTO.git
```

Y boom, tienes el proyecto completo en tu PC.

---

# Día 4: Remote (conectando mi PC con el servidor)

Después de entender SSH, el concepto de "remote" fue súper claro.

## ¿Qué es Git Remote?

Es simplemente la dirección de tu repositorio en GitHub. Como si fuera un teléfono que conecta tu PC con el servidor.

```bash
git remote -v
```

Este comando te muestra exactamente a dónde van tus cambios cuando haces `push`.

## Lo único importante aquí

Si tienes múltiples cuentas en GitHub (trabajo, personal, etc.), cada una necesita su propia llave SSH. Es como tener varias llaves para diferentes casas.

Yo aprendí esto por las malas cuando intenté pushear con la llave equivocada.

---

# Día 5: Las ramas que me salvaron la vida

Este fue el punto de quiebre donde Git pasó de "es un almacenamiento" a "es muy potente".

## ¿Qué son las ramas?

Imagina el código como un árbol:
- El **tronco** es la rama `main` (código oficial, estable)
- Las **ramas** son caminos paralelos donde trabajas sin afectar el tronco

¿Por qué es importante? Porque ahora puedo:
- Trabajar en una nueva feature sin romper el código principal
- Mi compañero puede trabajar en otro feature simultaneamente
- Si algo sale mal, la rama principal sigue intacta

## Comandos de Ramas

```bash
# Ver todas las ramas (y dónde estoy)
git branch

# Crear una nueva rama
git branch feature-login

# Borrar una rama (si no la necesito más)
git branch -D feature-login
```

## Moverse entre ramas

Hay dos formas:

**La clásica (git checkout):**
```bash
git checkout feature-login
git checkout -b feature-login  # Crea y cambia
```

**La moderna (git switch):**
```bash
git switch feature-login
git switch -c feature-login  # Crea y cambia
```

Prefiero `switch` porque es más claro y específico para ramas.

## El flujo que aprendí

Existe una metodología llamada **Git Flow** que tiene sentido:

1. **main** → Código en producción, super estable
2. **develop** → Rama de trabajo, donde integramos features
3. **feature-*** → Mis ramas temporales para tareas específicas

El flujo:
- Creo `feature-login` desde `develop`
- Hago mis cambios, commits
- Cierro la rama
- La mezclo con `develop`
- Y luego `develop` se mezcla con `main`

**Regla de oro:** NUNCA trabajo directamente en `main`. Nunca.

---

# Día 6: Merge, Fetch, Pull y Push (cuál es cuál)

Este día quería gritarle a Git. Tantos comandos similares. Pero finalmente se organizó en mi cabeza.

## Merge: Juntar las Ramas

Después de terminar una rama, necesito mezclarla con otra.

```bash
# Me muevo a la rama que recibirá los cambios
git checkout main

# Junto los cambios de la otra rama
git merge feature-login
```

Y listo. Ahora `main` tiene todos los cambios que hice en `feature-login`.

## Los Comandos del Servidor (el caos)

### Git Fetch: Mirar sin tocar
```bash
git fetch
```

Es como asomarse por la ventana para ver si está lloviendo, sin salir de casa. Descarga información del servidor pero NO cambia tus archivos. Solo te avisa si hay cosas nuevas.

### Git Pull: Traer y aplicar
```bash
git pull origin develop
```

Esto es más directo: descarga los cambios del servidor Y los aplica a tu rama. Es `fetch` + `merge` en uno.

Acá es donde puedes tener conflictos si alguien más cambió lo mismo que tú.

### Git Push: Subir tu trabajo
```bash
git push origin develop
```

Subes tus commits locales al servidor. La primera vez en una rama nueva:
```bash
git push -u origin develop
```

El `-u` crea el vínculo entre tu rama local y la remota.

## La Fórmula Visual

```
Tu PC                    GitHub
[Commits] --push--->  [Repositorio]
   ^                      |
   |                      |
   +--pull/fetch----------+
```

Todos los días:
1. Hago `pull` para traer cambios del equipo
2. Trabajo y hago commits
3. Hago `push` para subir mis cambios

---

# Día 7: Pull Requests (mi salvavidas en equipo)

Aquí es donde todo se vuelve profesional.

## ¿Qué es un Pull Request?

Es una solicitud de colaboración. Es decir:
- "Hey, termié una tarea"
- "Quiero que revisen mi código"
- "Antes de que lo mezcle con develop/main"

No es solo código. Es código + conversación + revisión de pares.

## El Flujo Profesional (que ahora uso)

### 1. Sincronizar
Primero traigo los últimos cambios:
```bash
git checkout develop
git pull origin develop
```

### 2. Crear mi rama
```bash
git checkout -b feature-autenticacion
```

### 3. Hacer mis cambios y commits
Trabajo normalmente, commmit aquí, commit allá.

### 4. Subir la rama
```bash
git push origin feature-autenticacion
```

### 5. Crear el Pull Request en GitHub
Voy a GitHub y veo un botón gigante que dice "Compare & pull request". Le hago click, escribo una buena descripción de qué cambié y por qué, y envío.

### 6. Esperar feedback
Mi jefe/compañeros revisan, comentan, piden cambios. Yo hago esos cambios localmente y hago más commits en la misma rama. El PR se actualiza automáticamente.

### 7. Merge
Cuando todos están de acuerdo, alguien (o yo) hace click en "Merge pull request" y ¡boom! Los cambios están en develop.

## ¿Por qué es tan importante?

- **Calidad:** Otros revisan el código antes de que entre a la rama principal
- **Control:** Nadie puede hacer cambios directos a `main` sin que otros lo vean
- **Historial:** Queda registro de por qué se hizo cada cambio
- **Aprendizaje:** El equipo aprende viendo el código de otros

---

# Día 8: Cuando todo se vuelve caótico (Stash & Switch)

El día 8 fue cuando realicé que a veces necesito cambiar de tareas rápidamente.

## Git Stash: El Cajón Mágico

Estoy trabajando en `feature-login`, todo bonito, cuando llega un email:

"¡URGENTE! Hay un bug en producción, necesito que lo arregles YA"

Pero tengo cambios sin guardar en `feature-login`. No quiero hacer commit a código incompleto.

Solución:
```bash
git stash
```

Esto guarda todos mis cambios en un "cajón" temporal. Mi área de trabajo queda limpia como si nada hubiese pasado.

Ahora puedo cambiar a la rama de bug:
```bash
git switch develop
git switch -c bugfix-critico
# Arreglo el bug, hago commits, push, Pull Request
```

Y luego vuelvo a mi tarea original:
```bash
git switch feature-login
git stash pop
```

¡Y boom! Mis cambios de `feature-login` están de vuelta como si nada.

## Otros comandos útiles del Stash

```bash
# Ver qué tengo guardado
git stash list

# Si tengo múltiples stash, especificar cuál sacar
git stash pop stash@{0}

# Limpiar todos los stash viejos
git stash clear
```

## Git Switch vs Git Checkout

La diferencia es simple:

- **checkout:** Multipropósito (ramas, commits, archivos)
- **switch:** Específicamente para ramas (más seguro y claro)

Yo uso `switch` porque es menos probable que me equivoque:
```bash
git switch nombre-rama
git switch -c nueva-rama
```

---

# Tabla de Referencia Rápida

Cuando tengo dudas, aquí es donde voy:

| Lo que Necesito | Comando |
| :--- | :--- |
| Configurar mi nombre | `git config --global user.name "Tu Nombre"` |
| Configurar mi correo | `git config --global user.email "tu@email.com"` |
| Ver mi configuración | `git config --global --list` |
| Crear un repo nuevo | `git init` |
| Ver el estado | `git status` |
| Añadir cambios | `git add .` |
| Guardar cambios | `git commit -m "mensaje"` |
| Ver el historial | `git log` |
| Ver mis ramas | `git branch` |
| Crear una rama | `git branch nombre` |
| Cambiar de rama | `git switch nombre` |
| Crear y cambiar rama | `git switch -c nombre` |
| Borrar una rama | `git branch -D nombre` |
| Mezclar ramas | `git merge nombre-rama` |
| Ver repos remotos | `git remote -v` |
| Subir código | `git push origin rama` |
| Subir por primera vez | `git push -u origin rama` |
| Descargar cambios | `git pull origin rama` |
| Solo revisar cambios | `git fetch` |
| Descargar un proyecto | `git clone url` |
| Guardar temporalmente | `git stash` |
| Ver qué guardé | `git stash list` |
| Recuperar guardado | `git stash pop` |
| Deshacer cambios en archivo | `git restore archivo` |
| Sacar archivo del staging | `git restore --staged archivo` |
| Ver diferencias | `git diff` |

---

## Mis Tips Después de 8 Días

✅ **Siempre sincroniza primero**
```bash
git pull origin develop
```
No quiero conflictos sorpresa.

✅ **Commits pequeños y descriptivos**
Hoy entiendo por qué es importante. En 6 meses, ese "feat: agregar login" me ahorra horas de debugging.

✅ **Nunca pusheá directamente a main**
Siempre un Pull Request. Así al menos yo me reviso a mí mismo (jaja).

✅ **Cuando todo falla, usa git status**
Es tu brújula. Te dice exactamente qué está pasando.

✅ **Lee los mensajes de error de Git**
No son tan confusos como parecen. Git intenta ayudarte, solo hay que escucharlo.

---
