## Configuración de Git

### Alias y Configuración por Alcance
- **Local:** Solo afecta al repositorio actual
- **Global:** Afecta a todos los repositorios del usuario
- **System:** Afecta a todos los usuarios del sistema

![git](https://github.com/Netgineer0/curso_git-nuevo/blob/main/1_git.png)



**git config --global core.editor "code --wait"**  # VS Code como editor predeterminado \
**git config --global color.ui true**    # Activar colores en comandos Git \
**git config --global core.autocrlf true** # Manejo de saltos de línea en Windows \


##Crear repositorios

**git init**                         # Inicializa un repositorio en la carpeta actual\
**git status**                       # Muestra estado de los archivos\
**git add <archivo>**                # Prepara archivo para commit\
**git commit -m "Mensaje"**          # Guarda cambios con mensaje
