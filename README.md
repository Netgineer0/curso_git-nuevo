## Configuración de Git

### Alias y Configuración por Alcance
- **Local:** Solo afecta al repositorio actual
- **Global:** Afecta a todos los repositorios del usuario
- **System:** Afecta a todos los usuarios del sistema



```bash
git config --global core.editor "code --wait"    # VS Code como editor predeterminado
git config --global color.ui true                 # Activar colores en comandos Git
git config --global core.autocrlf true            # Manejo de saltos de línea en Windows
