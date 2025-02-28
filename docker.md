# Instalar Docker Desktop

## Introducción
Docker es una plataforma para desarrollar, enviar y ejecutar aplicaciones en contenedores. En este apartado aprenderás a instalar Docker Desktop en Windows y Linux.

## Requisitos previos
- En Windows: Tener **WSL 2** habilitado.
- En Linux: Tener permisos de administrador.

## Instalación de Docker Desktop en Windows

### 1. Descargar Docker Desktop
Descarga el instalador desde:
[https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)

### 2. Instalar Docker Desktop
Ejecuta el instalador y sigue los pasos:
- Asegúrate de habilitar la opción **Use the WSL 2 based engine**.
- Completa la instalación y reinicia el equipo si se solicita.

### 3. Verificar la instalación
Abre una terminal y ejecuta:
```powershell
docker --version
```
Si Docker está instalado correctamente, verás la versión instalada.

## Instalación de Docker en Linux

### 1. Actualizar los paquetes del sistema
```bash
sudo apt update && sudo apt upgrade -y
```

### 2. Instalar dependencias
```bash
sudo apt install ca-certificates curl gnupg
```

### 3. Agregar el repositorio de Docker
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

### 4. Instalar Docker Engine
```bash
sudo apt update && sudo apt install docker-ce docker-ce-cli containerd.io -y
```

### 5. Agregar el usuario actual al grupo de Docker
```bash
sudo usermod -aG docker $USER
```
Cierra sesión y vuelve a iniciar sesión para aplicar los cambios.

### 6. Verificar la instalación
Ejecuta el siguiente comando:
```bash
docker --version
```

## Errores comunes y soluciones
- **Docker no arranca en Windows:** Asegúrate de que WSL 2 está habilitado y actualizado.
- **Error `permission denied` en Linux:** Agrega tu usuario al grupo `docker` y reinicia la sesión.
- **No se reconoce el comando `docker`:** Verifica que Docker está en el PATH del sistema.

## Próximos pasos
- Instalar Docker Compose para gestionar múltiples contenedores.
- Configurar volúmenes y redes para contenedores.
- Crear y ejecutar imágenes personalizadas con Dockerfiles.
