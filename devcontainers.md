# Instalar DevContainers

## Introducción
Los DevContainers permiten crear entornos de desarrollo reproducibles dentro de contenedores Docker. Esto facilita la configuración del entorno sin afectar la máquina local.

## Requisitos previos
- Tener **Docker Desktop** instalado y funcionando.
- Tener **VS Code** instalado.
- Instalar la extensión **Dev Containers** en VS Code.

## Instalación de la extensión Dev Containers

### 1. Instalar la extensión en VS Code
Abre VS Code y presiona `Ctrl + Shift + X` para abrir el marketplace de extensiones. Busca e instala **Dev Containers**.

O instala la extensión desde la terminal de VS Code con:
```powershell
code --install-extension ms-vscode-remote.remote-containers
```

## Crear un entorno DevContainer

### 1. Abrir un proyecto en VS Code
Abre la carpeta del proyecto donde deseas configurar un DevContainer.

### 2. Crear la configuración del DevContainer
Abre la paleta de comandos con `Ctrl + Shift + P` y busca **Remote-Containers: Add Development Container Configuration Files**. Selecciona una configuración base o personalizada.

### 3. Personalizar `devcontainer.json`
Modifica el archivo `.devcontainer/devcontainer.json` según tus necesidades. Ejemplo básico:
```json
{
  "name": "Python DevContainer",
  "image": "mcr.microsoft.com/vscode/devcontainers/python:3",
  "features": {},
  "extensions": [
    "ms-python.python"
  ]
}
```

### 4. Abrir el proyecto en el DevContainer
Ejecuta:
```powershell
Ctrl + Shift + P -> Remote-Containers: Reopen in Container
```
VS Code iniciará el contenedor y cargará el entorno dentro de él.

## Errores comunes y soluciones
- **Docker no está corriendo**: Asegúrate de que Docker Desktop está iniciado.
- **No se puede conectar con el contenedor**: Reinicia Docker y vuelve a intentarlo.
- **Extensiones no se instalan en el contenedor**: Agrega las extensiones en el `devcontainer.json`.

## Próximos pasos
- Personalizar la configuración de DevContainers con herramientas específicas.
- Crear entornos de desarrollo multi-contenedor con `docker-compose.yml`.
- Integrar DevContainers con GitHub Codespaces para trabajar en la nube.
