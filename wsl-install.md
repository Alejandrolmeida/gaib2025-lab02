# Instalar Linux WSL en un equipo Windows

## Introducción
WSL (Windows Subsystem for Linux) permite ejecutar un entorno Linux dentro de Windows sin necesidad de una máquina virtual. Es ideal para desarrolladores que desean trabajar con herramientas de Linux sin salir del entorno Windows.

## Requisitos previos
- Windows 10 versión 2004 o superior (Build 19041 y posteriores) o Windows 11.
- Acceso con privilegios de administrador en el equipo.

## Pasos de instalación
### 1. Habilitar WSL
Abrir **PowerShell** como administrador y ejecutar el siguiente comando:
```powershell
wsl --install
```
Este comando instalará WSL junto con la distribución por defecto de Linux (generalmente Ubuntu).

### 2. Reiniciar el equipo
Una vez completada la instalación, es recomendable reiniciar el equipo para aplicar los cambios.

### 3. Configurar la distribución de Linux
Al iniciar WSL por primera vez, se abrirá automáticamente la configuración de la distribución de Linux instalada. Se deberá crear un usuario y contraseña.

### 4. Verificar la instalación
Ejecutar en PowerShell o en la terminal de WSL:
```powershell
wsl --list --verbose
```
Este comando mostrará las distribuciones instaladas y su estado.

## Configuración adicional
Para asegurarse de estar utilizando la versión más reciente de WSL, se puede ejecutar:
```powershell
wsl --update
```
Si se desea habilitar WSL 2 y cambiar la versión predeterminada:
```powershell
wsl --set-default-version 2
```

## Errores comunes y soluciones
- **WSL no se instala:** Verificar que la virtualización esté habilitada en la BIOS.
- **Error `wsl --install` no reconocido:** Asegurarse de que Windows está actualizado y PowerShell se está ejecutando como administrador.
- **Problemas de red:** Si la distribución de Linux no tiene acceso a Internet, probar con:
  ```powershell
  netsh winsock reset
  ```

## Próximos pasos
Una vez instalado WSL, puedes proceder con la instalación de herramientas adicionales como Docker, Miniconda y Visual Studio Code para un entorno de desarrollo completo.
