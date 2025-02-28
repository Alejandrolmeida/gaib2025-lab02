# Desplegar una VM Linux en Azure y conectarse por SSH

## Introducción
En esta sección, aprenderás a crear una máquina virtual Linux en Azure y conectarte a ella mediante SSH desde tu equipo.

## Requisitos previos
- Una cuenta en **Microsoft Azure** con permisos para crear recursos.
- **Azure CLI** instalado en tu equipo ([descargar aquí](https://aka.ms/installazurecliwindows)).
- Claves SSH generadas en tu equipo (opcional, Azure puede generarlas automáticamente).

## Pasos de instalación

### 1. Iniciar sesión en Azure
Abrir una terminal o PowerShell y ejecutar:
```powershell
az login
```
Se abrirá un navegador donde deberás ingresar tus credenciales de Azure.

### 2. Crear un grupo de recursos
```powershell
az group create --name MyResourceGroup --location eastus
```
Este comando crea un grupo de recursos en la región East US.

### 3. Crear la máquina virtual
Ejecuta el siguiente comando para desplegar una VM Ubuntu con generación automática de claves SSH:
```powershell
az vm create \
  --resource-group MyResourceGroup \
  --name MyLinuxVM \
  --image UbuntuLTS \
  --admin-username azureuser \
  --generate-ssh-keys
```
Este proceso tardará unos minutos. Al finalizar, mostrará la dirección IP pública de la VM.

### 4. Conectarse a la VM por SSH
Desde una terminal de Windows o WSL, ejecuta:
```bash
ssh azureuser@<public-ip>
```
Sustituyendo `<public-ip>` por la dirección IP pública que te proporcionó Azure.

## Errores comunes y soluciones
- **Acceso denegado al conectar por SSH**: Verificar que la clave SSH correcta está configurada.
- **No se encuentra la VM**: Confirmar que el grupo de recursos y el nombre de la VM son correctos.
- **Firewall bloqueando la conexión**: Asegurarse de que el puerto 22 está abierto en las reglas de seguridad de la VM:
  ```powershell
  az vm open-port --resource-group MyResourceGroup --name MyLinuxVM --port 22
  ```

## Próximos pasos
- Instalar herramientas en la VM como Docker, Miniconda o Python.
- Configurar autenticación con claves SSH para mayor seguridad.
- Automatizar despliegues de VM con Bicep o Terraform.
