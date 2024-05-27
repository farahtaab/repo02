# Principales comandos en GIT

Guía detalla los pasos para crear un repositorio local en tu máquina y cómo configurar un repositorio en GitHub.

## Crear un Repositorio Local

- **Abrir la Terminal**:
  - Abre la siguiente terminal de git en tu sistema.
  - 
   ![Imagen](imagenes/imagen3%20(2).png)

- **Navegar al Directorio Deseado**:
  - Cambia al directorio donde deseas establecer tu repositorio usando:
    ```bash
    cd path/to/directory
    ```
  - Si el directorio no existe, crea uno con:
    ```bash
    mkdir NombreDelProyecto
    cd NombreDelProyecto
    ```

- **Inicializar el Repositorio**:
  - Una vez en el directorio correcto, ejecuta:
    ```bash
    git init
    ```
  - Este comando crea un nuevo subdirectorio `.git` que almacena todos los archivos necesarios del repositorio Git.

## Crear un Repositorio en GitHub

- **Iniciar Sesión en GitHub**:
  - Vamos a [GitHub](https://github.com/) y nos aseguramos de estar consctados con nuestra cuenta.

- **Crear Nuevo Repositorio**:
  - Haz clic en el ícono `+` en la esquina superior derecha de la página y selecciona "New repository".

- **Configurar el Repositorio**:
  - Proporciona la siguiente información para tu nuevo repositorio:
    - **Repository name**: El nombre de tu repositorio.
    - **Description** (opcional): Una breve descripción de tu repositorio.
    - **Visibility**: Elige si el repositorio será público o privado.
    - Opcionalmente, puedes inicializar el repositorio con un archivo `README`.

- **Crear el Repositorio**:
  - Hacemos clic en "Create repository" para finalizar la configuración en GitHub.

## Clonar el Repositorio GitHub a Local

- **Clonar Repositorio**:
  - Si deseamos trabajar con nuestro repositorio de GitHub localmente, lo clonamos utilizando:
    ```bash
    git clone https://github.com/tu_usuario/tu_repositorio.git
    ```
  - Sustituye `tu_usuario/tu_repositorio.git` con tu nombre de usuario y el nombre del repositorio.

Estos pasos te permiten manejar eficientemente la creación y configuración de repositorios en Git y GitHub.

# Comandos Básicos de Git

| Comando                                    | Descripción                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `git init`                                 | Inicializa un nuevo repositorio de Git.                                                                       |
| `git clone [url]`                          | Clona un repositorio existente desde la URL especificada.                                                     |
| `git log`                                  | Muestra un registro de los commits y el HEAD indica el commit actual.                                         |
| `HEAD`                                     | Es un puntero que indica el commit actual.                                                                    |
| `git show`                                 | Muestra los cambios realizados en un commit específico.                                                       |

# Comandos para Navegar entre Commits

| Comando                                    | Descripción                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `git log --reflog`                         | Permite ver todos los commits, incluyendo los no alcanzables desde el HEAD.                                   |
| `git checkout [hash_del_commit]`           | Sitúa el HEAD en el commit específico indicado por el hash.                                                   |
| `git checkout main`                        | Regresa el HEAD a la rama principal (`main`).                                                                 |
| `git reset [hash_del_commit]`              | Deshace commits, moviendo el HEAD al commit especificado.                                                     |
| `git reset --hard [hash_del_commit]`       | Deshace commits y borra todos los cambios en el área de trabajo.                                              |

# Comandos para Trabajar con Ramas

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

# Comandos para Gestionar Archivos

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

# Comandos para Gestionar Remotos

| Comando                                    | Descripción                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `git remote`                               | Muestra los repositorios remotos configurados.                                                                |
| `git remote add [nombre] [url]`            | Añade un nuevo repositorio remoto con el nombre y la URL especificados.                                        |
| `git fetch [nombre]`                       | Descarga los cambios desde el repositorio remoto especificado.                                                |
| `git pull [nombre] [rama]`                 | Descarga los cambios desde el repositorio remoto y rama especificados, y los fusiona con la rama actual.       |
| `git push [nombre] [rama]`                 | Sube los commits locales a la rama especificada del repositorio remoto.                                        |

# Comandos para Etiquetas (Tags)

| Comando                                    | Descripción                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `git tag`                                  | Muestra la lista de etiquetas en el repositorio.                                                              |
| `git tag [nombre_etiqueta]`                | Crea una nueva etiqueta ligera con el nombre especificado.                                                    |
| `git tag -a [nombre_etiqueta] -m "[mensaje]"` | Crea una nueva etiqueta anotada con el nombre y mensaje especificados.                                         |
| `git push origin [nombre_etiqueta]`        | Sube la etiqueta especificada al repositorio remoto.                                                          |
| `git push origin --tags`                   | Sube todas las etiquetas al repositorio remoto.                                                               |
| `git tag -d [nombre_etiqueta]`             | Elimina la etiqueta especificada localmente.                                                                  |
| `git push origin :refs/tags/[nombre_etiqueta]` | Elimina la etiqueta especificada en el repositorio remoto.                                                     |
