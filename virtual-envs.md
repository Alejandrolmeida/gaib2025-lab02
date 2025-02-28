# Crear entornos virtuales dentro de Linux

## Introducción
Los entornos virtuales permiten aislar las dependencias de los proyectos en Python, evitando conflictos entre paquetes y versiones. En esta sección, aprenderás a crear y administrar entornos virtuales en Linux.

## Requisitos previos
- Tener **Python 3** instalado en el sistema.
- Acceso a una terminal en Linux o en WSL.

## Pasos para crear un entorno virtual

### 1. Verificar la instalación de Python
Ejecuta el siguiente comando para asegurarte de que Python 3 está instalado:
```bash
python3 --version
```
Si no está instalado, puedes hacerlo con:
```bash
sudo apt update && sudo apt install python3 python3-venv
```

### 2. Crear un entorno virtual
Ejecuta el siguiente comando en la carpeta donde deseas crear el entorno:
```bash
python3 -m venv my_env
```
Esto creará un directorio `my_env` que contendrá una copia aislada de Python y pip.

### 3. Activar el entorno virtual
Para activar el entorno virtual, ejecuta:
```bash
source my_env/bin/activate
```
Notarás que el prompt de la terminal cambia, indicando que el entorno virtual está activo.

### 4. Instalar paquetes dentro del entorno
Con el entorno activado, puedes instalar paquetes sin afectar el sistema global:
```bash
pip install numpy pandas
```

### 5. Desactivar el entorno virtual
Para salir del entorno virtual, usa:
```bash
deactivate
```

## Errores comunes y soluciones
- **`venv` no encontrado**: Asegúrate de que el paquete `python3-venv` está instalado.
- **El entorno virtual no se activa**: Si usas `zsh`, intenta `source my_env/bin/activate` en lugar de `activate`.
- **Paquetes no disponibles después de cerrar la terminal**: Recuerda activar el entorno antes de ejecutar comandos dentro de él.

## Próximos pasos
- Aprender a usar archivos `requirements.txt` para gestionar dependencias.
- Explorar herramientas como Conda para gestionar entornos avanzados.
- Automatizar la activación del entorno en proyectos específicos con scripts Bash.
