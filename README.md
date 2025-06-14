## Configuración de Git

### Alias y Configuración por Alcance
- **Local:** Solo afecta al repositorio actual
- **Global:** Afecta a todos los repositorios del usuario
- **System:** Afecta a todos los usuarios del sistema

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/1_git.png)



**git config --global core.editor "code --wait"**  # VS Code como editor predeterminado \
**git config --global color.ui true**    # Activar colores en comandos Git \
**git config --global core.autocrlf true** # Manejo de saltos de línea en Windows
![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/2_git.png)

### Crear repositorios
Un repositorio es un espacio donde Git guarda toda la información de un proyecto 
-	Los archivos del proyecto 
- Ramas (branches) 
-	Confirmaciones (commits) 
Puede ser local o remoto 
Para crear un repositorio, nos establecemos en el directorio en el que creemos la carpeta, seguidamente con el comando cd nos dirigimos hacia ella y creamos una nueva carpeta en el que se logra el repositorio. Algunos de los comandos básicos en git, son los siguientes 


**git init**                         # Inicializa un repositorio en la carpeta actual\
**git status**                       # Muestra estado de los archivos\
**git add <archivo>**                # Prepara archivo para commit\
**git commit -m "Mensaje"**          # Guarda cambios con mensaje

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/3_git.png)
![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/4_git.png)
![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/5_git.png)

**git log --oneline** # Es una forma resumida y más limpia de ver el historial de commits en un repositorio de Git.
![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/6_git.png)

### Git diff
Muestra línea por línea qué ha cambiado entre dos versiones de un archivo o conjunto de archivos\
![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/7_git.png)

### Cambios en los archivos
**git diff --name-only** Es un comando útil para ver solo los nombres de los archivos que han cambiado, sin mostrar el contenido de los cambios\
![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/8_git.png)

### Cambios en las líneas de los archivos
Sirve para mostrar las diferencias palabra por palabra, en lugar de línea por línea. Es muy útil cuando los cambios son pequeños y dentro de la misma línea

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/9_git.png)

### Modificar y deshacer commits
Para entender de forma más clara este subtema. Fue necesario realizar otro repositorio, y hacer modificaciones dentro del archivo, se agregaron 5 commits. A continuación, se muestra el procedimiento que se siguió 

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/10_git.png)
![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/11_git.png)

Permite ajustar o corregir el historial de cambios (commits) para mejorar la claridad, corregir errores o deshacer acciones.
### Modificar un commit
•	Corregir el mensaje\
•	Agregar archivos\
•	Ajustar el contenido 

**git commit –amend:** Reescribe el último commit\

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/12_git.png)

### Historia y versiones
**git log:** Visualiza historial de commits\
**git checkout:** Retrocede o permite mover entre ramas/commits\

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/13_git.png)


### Ramas (branches)
**git branch:** Listar, crear y eliminar ramas\

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/14_git.png)

**git checkout:** Rama nueva crear y cambiar de rama en un solo comando. Fusionar con git merge rama y resolución de conflictos manuales

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/17_git.PNG)

Otra forma es **git switch**, la cual es la que se recomienda ya que es más segura

### Trabajo con repositorios remotos

**git remote add origin:** <URL> Conecta repositorio local con uno remoto
**git push origin <rama>:** Sube las ramas al repositorio remoto
**git pull:** Descarga y fusiona cambios del remoto automáticamente.

### Flujos de trabajo
#### *Modelos tipo Git Flow, GitHub Flow*

## GitFlow: Modelo más estructurado propuesto por Vincent Driessen. Usa varias ramas con propósitos específicos:
**main/master:** Código de producción
**develop:** Integración de features para próximo release
**feature/*:** Ramas para desarrollo de nuevas funcionalidades
**release/*:** Preparación para nuevos releases
**hotfix/*:** Correcciones urgentes para producción


## GitHub Flow: 
Ideal para proyectos que hacen despliegues continuos y colaboraciones ágiles

**git checkout main:** Actualiza la rama principal
**git checkout -b feature/nueva-funcionalidad:** Crea una nueva rama para una funcionalidad o cambio
**git add . git commit -m:** Hace cambios y los confirma
**git push origin feature/nueva-funcionalidad:** Sube la rama al repositorio remoto


**git push origin --delete feature/nombre:** Elimina rama remota

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/15_git.png)

## Etiquetas (tags)
**git tag:** marcar versiones específicas para releases

## Revertir y resetear cambios

**git reset --hard HEAD:** borra cambios locales no comprometidos.
**git revert <hash_commit>:** Deshace un commit de forma segur

## Merge conflicts

Oocurre cuando Git no puede combinar automáticamente los cambios de dos ramas porque hay modificaciones incompatibles en las mismas líneas de un archivo o archivos. Es una situación común cuando estás haciendo un merge (fusión) entre ramas y Git no sabe cuál de los cambios mantener.

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/18_git.PNG)

Se indica que exixten conflictos dentro del archivo

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/19_git.PNG)

En el archivo creado previamante en Visual Studio. Se pueden apreciar los comandos de conflicto, y sepuede observar de mejor manera en dónde se puede encontrar el conflicto

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/20_git.PNG)

Al aceptar los cambios en la parte superior, y escribimos de nuevo el comando para visualizar los commits. Se puede observar que se resolvió el conflicto

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/22_git.PNG)

## Git ignore

El archivo .gitignore le dice a Git qué archivos o carpetas debe ignorar, es decir, no incluir en el control de versiones (no se añadirán, rastrearán ni subirán al repositorio).
Evita que archivos temporales, sensibles o generados automáticamente se suban al repositorio

El primer paso para verificar este subtema. Se realizo un nuevo archivo de texto, se agrego a git con respectio commit, y con el comando ls-tree -r --name-only se visualizo que se había gregado recientemente

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/23_git.PNG)

Se crea un archivo llamado .gitignore. Como se muestra a continuación

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/24_git.PNG)

Se puede visualizar los archivos que estan dentro de la carpeta. Pero al ejecutar los comandos solo se observan los que no se tienen ignorados

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/25_git.PNG)
![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/26_git.PNG)

## GIT CLONE

Para clonar un repostorio en Github, existen diversas opciones. Como se puede observar en la siguiente imagen

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/27_git.PNG)

Se debe de copiar el URL que aparece en el apartado de HTTPS

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/28_git.PNG)

Nos dirigimos a la ventana de GIT, y ejecutamos lo siguiente:

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/29_git.PNG)

Para verificar el resultado simplemente nos dirigimos hacia el repositorio clonado. El resultado se muestra a continuación

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/30_git.PNG)

