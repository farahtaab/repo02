# Manual Básico de Git para Principiantes

Git es un sistema de control de versiones distribuido que te permite rastrear los cambios en tus archivos y colaborar con otros desarrolladores. A continuación, se presenta una guía básica que explica cómo usar Git y una tabla de comandos esenciales organizados por categorías.

## Introducción a Git

Git te permite trabajar en proyectos de software y mantener un historial de cambios. Puedes revertir cambios, trabajar en múltiples versiones del proyecto al mismo tiempo y colaborar con otros de manera eficiente. Todo esto se hace utilizando una serie de comandos que se ejecutan en la terminal o línea de comandos.

### ¿Qué es un repositorio?

Un repositorio (o repo) es un directorio que contiene todos los archivos de tu proyecto y un historial completo de todos los cambios realizados en estos archivos. Puedes tener repositorios locales (en tu computadora) y repositorios remotos (en servidores como GitHub, GitLab, etc.).

### Conceptos Básicos

- **Commit**: Una instantánea de tus archivos en un momento específico.
- **Branch** (Rama): Una versión independiente de tu código, lo que te permite trabajar en diferentes características simultáneamente.
- **Merge** (Fusión): Combina los cambios de diferentes ramas.
- **Staging Area**: Un área donde colocas cambios que deseas incluir en el próximo commit.
- **Remote**: Un repositorio alojado en un servidor, como GitHub o GitLab.

## Comandos Básicos de Git

Para empezar a usar Git, necesitas inicializar un repositorio, clonar un repositorio existente, y comprender cómo ver el historial de cambios. Aquí están los comandos básicos que necesitas conocer:

| Comando                                    | Descripción                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `git init`                                 | Inicializa un nuevo repositorio de Git.                                                                       |
| `git clone [url]`                          | Clona un repositorio existente desde la URL especificada.                                                     |
| `git log`                                  | Muestra un registro de los commits y el HEAD indica el commit actual.                                         |
| `HEAD`                                     | Es un puntero que indica el commit actual.                                                                    |
| `git show`                                 | Muestra los cambios realizados en un commit específico.                                                       |

## Comandos para Navegar entre Commits

Cuando trabajas en un proyecto, es importante poder moverte entre diferentes puntos en el historial de commits. Los siguientes comandos te permiten ver el historial y moverte entre commits:

| Comando                                    | Descripción                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `git log --reflog`                         | Permite ver todos los commits, incluyendo los no alcanzables desde el HEAD.                                   |
| `git checkout [hash_del_commit]`           | Sitúa el HEAD en el commit específico indicado por el hash.                                                   |
| `git checkout main`                        | Regresa el HEAD a la rama principal (`main`).                                                                 |
| `git reset [hash_del_commit]`              | Deshace commits, moviendo el HEAD al commit especificado.                                                     |
| `git reset --hard [hash_del_commit]`       | Deshace commits y borra todos los cambios en el área de trabajo.                                              |

## Comandos para Trabajar con Ramas

Las ramas te permiten trabajar en diferentes características o versiones de tu proyecto simultáneamente. Aquí hay algunos comandos esenciales para manejar ramas:

| Comando                                    | Descripción                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `git branch`                               | Muestra las ramas actuales.                                                                                   |
| `git branch [nombreRama]`                  | Crea una nueva rama con el nombre especificado.                                                               |
| `git checkout [nombreRama]`                | Cambia a la rama especificada.                                                                                |
| `git checkout -b [nombreRama]`             | Crea y cambia a una nueva rama con el nombre especificado.                                                    |
| `git branch -d [nombreRama]`               | Elimina la rama especificada en el repositorio local.                                                         |
| `git push origin --delete [nombreRama]`    | Elimina la rama especificada en el repositorio remoto.                                                        |
| `git merge [nombreRama]`                   | Fusiona la rama especificada con la rama actual.                                                              |
| `git merge --no-ff [nombreRama]`           | Fusiona la rama especificada con la rama actual, creando un nuevo commit de fusión.                           |

## Comandos para Gestionar Archivos

Estos comandos te ayudan a gestionar los archivos en tu proyecto, desde añadir archivos al área de staging hasta confirmar cambios y subirlos a un repositorio remoto:

| Comando                                    | Descripción                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `git status`                               | Muestra el estado de los archivos en la rama actual, incluyendo los cambios sin añadir.                       |
| `git add [archivo]`                        | Añade el archivo especificado al área de staging.                                                             |
| `git commit -m "[mensaje]"`                | Crea un commit con los cambios añadidos al área de staging, usando el mensaje especificado.                   |
| `git commit --amend -m "[mensaje]"`        | Modifica el último commit con un nuevo mensaje.                                                               |
| `git push --set-upstream origin [nombreRama]` | Sube la rama especificada al repositorio remoto y establece el upstream.                                       |
| `git push`                                 | Sube los commits locales al repositorio remoto.                                                               |
| `git pull`                                 | Descarga los cambios del repositorio remoto y los fusiona con la rama local actual.                           |
| `git stash`                                | Guarda los cambios no confirmados para limpiarlos temporalmente del área de trabajo.                          |
| `git stash apply`                          | Aplica los cambios guardados con `git stash`.                                                                 |
| `git stash pop`                            | Aplica los cambios guardados con `git stash` y los elimina de la lista de stashes.                            |
| `git stash list`                           | Muestra la lista de cambios guardados con `git stash`.                                                        |
| `git revert [hash_del_commit]`             | Crea un nuevo commit que deshace los cambios del commit especificado.                                          |

## Comandos para Gestionar Remotos

Trabajar con repositorios remotos te permite colaborar con otros y mantener tus cambios sincronizados. Aquí están los comandos clave para gestionar repositorios remotos:

| Comando                                    | Descripción                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `git remote`                               | Muestra los repositorios remotos configurados.                                                                |
| `git remote add [nombre] [url]`            | Añade un nuevo repositorio remoto con el nombre y la URL especificados.                                        |
| `git fetch [nombre]`                       | Descarga los cambios desde el repositorio remoto especificado.                                                |
| `git pull [nombre] [rama]`                 | Descarga los cambios desde el repositorio remoto y rama especificados, y los fusiona con la rama actual.       |
| `git push [nombre] [rama]`                 | Sube los commits locales a la rama especificada del repositorio remoto.                                        |

## Comandos para Etiquetas (Tags)

Las etiquetas son útiles para marcar puntos específicos en el historial del proyecto, como versiones de lanzamiento. Aquí están los comandos para trabajar con etiquetas:

| Comando                                    | Descripción                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `git tag`                                  | Muestra la lista de etiquetas en el repositorio.                                                              |
| `git tag [nombre_etiqueta]`                | Crea una nueva etiqueta ligera con el nombre especificado.                                                    |
| `git tag -a [nombre_etiqueta] -m "[mensaje]"` | Crea una nueva etiqueta anotada con el nombre y mensaje especificados.                                         |
| `git push origin [nombre_etiqueta]`        | Sube la etiqueta especificada al repositorio remoto.                                                          |
| `git push origin --tags`                   | Sube todas las etiquetas al repositorio remoto.                                                               |
| `git tag -d [nombre_etiqueta]`             | Elimina la etiqueta especificada localmente.                                                                  |
| `git push origin :refs/tags/[nombre_etiqueta]` | Elimina la etiqueta especificada en el repositorio remoto.                                                     |
