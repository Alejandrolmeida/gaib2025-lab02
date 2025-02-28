# Instalar Python y las dependencias de un proyecto con PIP

## Introducción
Python es un lenguaje de programación ampliamente utilizado en inteligencia artificial y desarrollo de software. PIP es el gestor de paquetes de Python que permite instalar y administrar librerías y dependencias.

## Requisitos previos
- Tener una distribución de Linux o WSL instalada.
- Acceso a una terminal con permisos de instalación.

## Pasos para instalar Python y PIP

### 1. Verificar si Python está instalado
Ejecuta el siguiente comando en la terminal:
```bash
python3 --version
```
Si no está instalado, puedes hacerlo con:
```bash
sudo apt update && sudo apt install python3 python3-pip
```

### 2. Verificar la instalación de PIP
Una vez instalado Python, verifica si PIP está disponible con:
```bash
pip3 --version
```
Si no está instalado, usa:
```bash
sudo apt install python3-pip
```

## Instalar dependencias de un proyecto con PIP

### 1. Crear un entorno virtual (opcional pero recomendado)
Para evitar conflictos entre paquetes, usa un entorno virtual:
```bash
python3 -m venv my_project_env
source my_project_env/bin/activate
```

### 2. Instalar paquetes individuales
Puedes instalar paquetes de Python con:
```bash
pip install numpy pandas
```
Para instalar una versión específica de un paquete:
```bash
pip install numpy==1.21.0
```

### 3. Instalar dependencias desde un archivo
Si tienes un archivo `requirements.txt`, instala todas las dependencias con:
```bash
pip install -r requirements.txt
```

### 4. Listar paquetes instalados
Para ver los paquetes instalados en el entorno actual:
```bash
pip list
```

### 5. Actualizar paquetes
Para actualizar un paquete específico:
```bash
pip install --upgrade numpy
```
Para actualizar todos los paquetes:
```bash
pip list --outdated | awk '{print $1}' | xargs -n1 pip install --upgrade
```

### 6. Desinstalar paquetes
Para eliminar un paquete:
```bash
pip uninstall numpy
```

## Errores comunes y soluciones
- **PIP no reconocido como comando**: Asegúrate de usar `pip3` en lugar de `pip`.
- **Error de permisos**: Usa `sudo` o instala paquetes en un entorno virtual.
- **Fallo en la instalación de un paquete**: Ejecuta `pip install --no-cache-dir nombre_paquete`.

## Próximos pasos
- Aprender a gestionar entornos virtuales con `venv` o Conda.
- Explorar PIPENV como alternativa para la gestión de dependencias.
- Investigar sobre `pyenv` para administrar múltiples versiones de Python en un sistema.
