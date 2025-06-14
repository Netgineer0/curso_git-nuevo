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
Un repositorio es un espacio donde Git guarda toda la información de un proyecto \
-	Los archivos del proyecto \
- Ramas (branches) \
-	Confirmaciones (commits) \
Puede ser local o remoto \
Para crear un repositorio, nos establecemos en el directorio en el que creemos la carpeta, seguidamente con el comando cd nos dirigimos hacia ella y creamos una nueva carpeta en el que se logra el repositorio. Algunos de los comandos básicos en git, son los siguientes \


**git init**                         # Inicializa un repositorio en la carpeta actual\
**git status**                       # Muestra estado de los archivos\
**git add <archivo>**                # Prepara archivo para commit\
**git commit -m "Mensaje"**          # Guarda cambios con mensaje
