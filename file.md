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

# COMANDOS PRINCIPALES

## Configuración Inicial
Antes de comenzar a usar Git, es importante configurar nuestra identidad y editor predilecto. Aquí está cómo hacerlo:

| Comando                        | Descripción                                      |
| ------------------------------ | ------------------------------------------------ |
| `git config --global user.name "Tu Nombre"` | Configura el nombre que aparecerá en tus commits. |
| `git config --global user.email "tuemail@example.com"` | Configura el email para tus commits. |
| `git config --list`                                           | Muestra las configuraciones de Git para verificar cambios. |

## Crear i clonar repositorios
Ya sea comenzando un proyecto desde cero o colaborando en uno existente, estos comandos son el primer paso.
| Comando                                               | Descripción                                                        |
| ----------------------------------------------------- | ------------------------------------------------------------------ |
| `git init`                                            | Inicializa un nuevo repositorio Git localmente.                    |
| `git clone https://github.com/usuario/repositorio.git`| Clona un repositorio remoto en tu máquina local para trabajar offline. |

## Gestión de Cambios y Commits
Estos comandos nos ayudan a gestionar y registrar los cambios en tus proyectos.

| Comando                        | Descripción                                                        |
| ------------------------------ | ------------------------------------------------------------------ |
| `git status`                   | Muestra el estado del repositorio, incluyendo cambios no rastreados.|
| `git add archivo.ext`          | Añade un archivo específico al área de staging.                     |
| `git add .`                    | Añade todos los archivos modificados al área de staging.            |
| `git commit -m "mensaje"`      | Realiza un commit con un mensaje explicativo.                       |
| `git log`                      | Muestra el historial de commits.                                    |

## Sincronización con Repositorios Remotos
Estos comandos nos permiten interactuar con un repositorio remoto, facilitando la colaboración.
| Comando                            | Descripción                                                          |
| ---------------------------------- | -------------------------------------------------------------------- |
| `git pull`             | Descarga cambios de la rama principal del remoto y los integra.      |
| `git push origin main`             | Sube los cambios locales a la rama principal del repositorio remoto. |

## Desplazandonos entre commits temporalmente

| Comando                                    | Descripción                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `git log`                                  | Muestra un registro de los commits y el HEAD indica el commit actual.                                         |
| `HEAD`                                     | Es un puntero que indica el commit actual.                                                                    |
| `git checkout [hash_del_commit]`           | Sitúa el HEAD en el commit específico indicado por el hash.                                                   |
| `git log --reflog`                         | Permite ver todos los commits, incluyendo los no alcanzables desde el HEAD.                                   |
| `git checkout [hash_del_commit]`           | Mueve el HEAD al commit deseado.                                                                              |
| `git checkout main`                        | Regresa el HEAD a la rama principal (`main`).                                                                 |
