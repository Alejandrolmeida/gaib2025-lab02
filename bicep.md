# Instalar Bicep y desplegar una plantilla en Azure

## Introducción
Bicep es un lenguaje declarativo para definir infraestructura como código en Azure. Facilita la creación y administración de recursos sin necesidad de JSON ARM templates complejos.

## Requisitos previos
- Tener **Azure CLI** instalado.
- Contar con una suscripción activa en **Microsoft Azure**.
- Tener permisos suficientes para crear recursos en Azure.

## Instalación de Bicep

### 1. Instalar Bicep con Azure CLI
Ejecuta el siguiente comando en la terminal:
```bash
az bicep install
```
Para verificar la instalación:
```bash
az bicep version
```

### 2. Instalar Bicep manualmente (opcional)
Si necesitas instalarlo manualmente, descárgalo desde:
[https://aka.ms/bicep](https://aka.ms/bicep)

## Crear y desplegar una plantilla Bicep

### 1. Crear un archivo Bicep
Crea un archivo `main.bicep` con el siguiente contenido de ejemplo:
```bicep
resource myStorageAccount 'Microsoft.Storage/storageAccounts@2022-09-01' = {
  name: 'mystorageaccount'
  location: 'eastus'
  sku: {
    name: 'Standard_LRS'
  }
  kind: 'StorageV2'
}
```

### 2. Validar la plantilla Bicep
Ejecuta el siguiente comando para comprobar que la sintaxis es correcta:
```bash
az bicep build --file main.bicep
```

### 3. Desplegar la plantilla en Azure
Ejecuta el siguiente comando para desplegar los recursos:
```bash
az deployment group create --resource-group MyResourceGroup --template-file main.bicep
```
Sustituyendo `MyResourceGroup` por el grupo de recursos donde deseas desplegar.

## Errores comunes y soluciones
- **Error de permisos:** Asegúrate de tener los permisos adecuados en la suscripción de Azure.
- **Error de sintaxis en Bicep:** Usa `az bicep build` para validar antes de desplegar.
- **Recurso ya existente:** Modifica el nombre del recurso en `main.bicep` o elimina el existente antes de volver a desplegar.

## Próximos pasos
- Explorar módulos en Bicep para reutilizar código.
- Integrar Bicep en pipelines de Azure DevOps.
- Convertir plantillas JSON ARM existentes a Bicep con `az bicep decompile`.
