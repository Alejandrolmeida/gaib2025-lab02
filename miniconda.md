# Instalar Miniconda en WSL y crear entornos Conda

## Introducción
Miniconda es una distribución ligera de Conda, un gestor de paquetes y entornos para Python. Es ideal para proyectos de ciencia de datos e inteligencia artificial, ya que facilita la instalación y gestión de dependencias.

## Requisitos previos
- Tener **WSL** (Windows Subsystem for Linux) instalado y configurado.
- Una distribución de Linux instalada en WSL.

## Pasos para instalar Miniconda en WSL

### 1. Descargar el instalador de Miniconda
Ejecuta el siguiente comando en la terminal de WSL para descargar el instalador más reciente:
```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```

### 2. Ejecutar el instalador
Ejecuta el siguiente comando para instalar Miniconda:
```bash
bash Miniconda3-latest-Linux-x86_64.sh
```
Sigue las instrucciones en pantalla y acepta los términos de la licencia cuando se te solicite.

### 3. Inicializar Conda
Después de la instalación, inicializa Conda ejecutando:
```bash
source ~/.bashrc
conda init
```
Reinicia la terminal para aplicar los cambios.

## Crear y gestionar entornos Conda

### 1. Crear un nuevo entorno
Para crear un entorno con Python 3.9, usa:
```bash
conda create -n my_env python=3.9
```

### 2. Activar el entorno
Para activar el entorno creado, usa:
```bash
conda activate my_env
```

### 3. Instalar paquetes dentro del entorno
Para instalar paquetes dentro del entorno, usa:
```bash
conda install numpy pandas
```

### 4. Listar entornos disponibles
Para ver los entornos disponibles, ejecuta:
```bash
conda env list
```

### 5. Desactivar y eliminar un entorno
Para desactivar el entorno actual:
```bash
conda deactivate
```
Para eliminar un entorno:
```bash
conda env remove -n my_env
```

## Errores comunes y soluciones
- **`conda: command not found`**: Asegúrate de que Miniconda está en el PATH ejecutando `source ~/.bashrc`.
- **El entorno no se activa**: Intenta reiniciar la terminal y ejecutar `conda init` nuevamente.
- **Fallo en la instalación de paquetes**: Prueba a ejecutar `conda clean --all` y luego reinstalar los paquetes.

## Próximos pasos
- Usar archivos `environment.yml` para definir entornos reproducibles.
- Aprender sobre Conda Forge y cómo instalar paquetes desde diferentes canales.
- Explorar la integración de Conda con Jupyter Notebooks y otras herramientas.
