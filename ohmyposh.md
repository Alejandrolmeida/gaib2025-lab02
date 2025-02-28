# Personalizar la Shell con Oh My Posh

## Introducción
Oh My Posh es una herramienta que permite personalizar la apariencia de la terminal, agregando información útil y mejorando la experiencia del usuario.

## Requisitos previos
- Tener Windows Terminal, PowerShell o una distribución de Linux/WSL.
- Tener instalado un perfil de PowerShell o Bash en el sistema.

## Instalación de Oh My Posh

### 1. Instalar en Windows
Ejecuta el siguiente comando en PowerShell:
```powershell
winget install JanDeDobbeleer.OhMyPosh -s winget
```
Si no tienes `winget`, puedes descargar el ejecutable desde:
[https://ohmyposh.dev/docs/](https://ohmyposh.dev/docs/)

### 2. Instalar en Linux o WSL
Ejecuta en la terminal:
```bash
curl -s https://ohmyposh.dev/install.sh | bash
```

### 3. Verificar la instalación
Para comprobar que la instalación se realizó correctamente, ejecuta:
```bash
oh-my-posh --version
```

## Configuración de Oh My Posh

### 1. Descargar un tema
Oh My Posh incluye varios temas predefinidos. Para ver la lista de temas disponibles:
```bash
oh-my-posh print-themes
```
Para aplicar un tema específico:
```bash
oh-my-posh init bash --config ~/.poshthemes/<nombre-tema>.omp.json | tee -a ~/.bashrc
source ~/.bashrc
```
Para PowerShell:
```powershell
oh-my-posh init pwsh --config "$(oh-my-posh get-theme agnoster)" | Invoke-Expression
```

### 2. Personalizar el tema
Puedes editar el archivo de configuración `.omp.json` con un editor de texto para modificar los colores, iconos y la información mostrada en el prompt.

## Errores comunes y soluciones
- **El prompt no cambia después de aplicar el tema:** Asegúrate de reiniciar la terminal y verificar la configuración en el archivo `.bashrc` o `.profile`.
- **Fuente incorrecta o caracteres no se muestran correctamente:** Instalar una fuente con soporte para Powerline, como Cascadia Code PL o Meslo LGM NF.
- **No se reconoce el comando `oh-my-posh`:** Asegurar que el ejecutable está en el PATH.

## Próximos pasos
- Explorar temas adicionales y crear uno personalizado.
- Integrar Oh My Posh con herramientas como Git y Docker para mostrar información en el prompt.
- Configurar Oh My Posh en otras shells como Zsh o Fish.