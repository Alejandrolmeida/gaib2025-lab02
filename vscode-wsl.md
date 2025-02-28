# Instalar VS Code y conectar con WSL en remoto

## Introducción
Visual Studio Code (VS Code) es un editor de código ligero pero potente. Con la extensión Remote - WSL, podemos desarrollar dentro de un entorno Linux directamente desde Windows.

## Requisitos previos
- Tener **WSL** instalado y configurado en Windows.
- Una distribución de Linux instalada en WSL.

## Instalación de VS Code en Windows

### 1. Descargar e instalar VS Code
Descarga el instalador desde:
[https://code.visualstudio.com/](https://code.visualstudio.com/)

Ejecuta el instalador y sigue las instrucciones en pantalla.

### 2. Instalar la extensión Remote - WSL
Abre VS Code y presiona `Ctrl + Shift + X` para abrir el marketplace de extensiones. Busca e instala **Remote - WSL**.

O instala la extensión desde la terminal de VS Code con:
```powershell
code --install-extension ms-vscode-remote.remote-wsl
```

## Conectar VS Code con WSL

### 1. Abrir una terminal WSL
Ejecuta el siguiente comando en la terminal de Windows (PowerShell o CMD):
```powershell
wsl
```

### 2. Iniciar VS Code desde WSL
Desde la terminal de WSL, ejecuta:
```bash
code .
```
Esto abrirá VS Code en el directorio actual, pero ejecutándose dentro de WSL.

### 3. Verificar la conexión con WSL
En la esquina inferior izquierda de VS Code, debería aparecer `WSL: Ubuntu` o la distribución de Linux que estés usando.

## Errores comunes y soluciones
- **VS Code no se abre desde WSL**: Asegúrate de que la instalación de VS Code está en el PATH de Windows.
- **Extensiones no se instalan en WSL**: Asegúrate de que estás instalando las extensiones dentro del entorno WSL.
- **WSL no se conecta correctamente**: Ejecuta `wsl --shutdown` y vuelve a abrir la terminal.

## Próximos pasos
- Configurar Git dentro de WSL para gestionar proyectos desde VS Code.
- Personalizar VS Code con temas y plugins específicos para desarrollo en Linux.
- Integrar Docker con WSL para ejecutar contenedores directamente en el entorno Linux.
