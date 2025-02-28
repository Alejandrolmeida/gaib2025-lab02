# Instalar PromptFlow

## Introducción
PromptFlow es una herramienta de Microsoft que permite la creación, gestión y ejecución de flujos de trabajo basados en modelos de inteligencia artificial. Se integra con Azure AI y facilita la implementación de soluciones de IA generativa.

## Requisitos previos
- Tener **Azure CLI** instalado y configurado.
- Contar con una suscripción activa en **Microsoft Azure**.
- Tener **Python 3.8+** instalado en el sistema.

## Instalación de PromptFlow

### 1. Instalar el paquete de PromptFlow
Ejecuta el siguiente comando en la terminal para instalar PromptFlow mediante pip:
```bash
pip install promptflow
```

### 2. Verificar la instalación
Para comprobar que la instalación se realizó correctamente, ejecuta:
```bash
pf --version
```
Si el comando no es reconocido, asegúrate de que el directorio de `pip` está en el `PATH`.

## Configuración de PromptFlow

### 1. Autenticarse en Azure
Para conectar PromptFlow con Azure, ejecuta:
```bash
az login
```

### 2. Configurar el entorno de trabajo
Crea un nuevo directorio para almacenar tus flujos:
```bash
mkdir my_promptflow_project && cd my_promptflow_project
```
Inicializa un nuevo proyecto de PromptFlow:
```bash
pf init
```

### 3. Crear un flujo de prueba
Ejecuta el siguiente comando para crear un flujo básico:
```bash
pf create --name my_first_flow
```
Esto generará un archivo JSON con la configuración del flujo.

## Desplegar un flujo en Azure

### 1. Crear un recurso de PromptFlow en Azure
Ejecuta el siguiente comando para desplegar un flujo en Azure AI:
```bash
az promptflow create --name myPromptFlow --resource-group MyResourceGroup --location eastus
```

### 2. Ejecutar el flujo en Azure
```bash
pf run --flow my_first_flow
```

## Errores comunes y soluciones
- **Error `pf: command not found`**: Asegúrate de que la instalación de `promptflow` está en el PATH.
- **Autenticación fallida en Azure**: Verifica tu sesión con `az account show` y vuelve a iniciar sesión si es necesario.
- **Fallo en la ejecución del flujo**: Revisa la sintaxis del archivo de configuración generado con `pf create`.

## Próximos pasos
- Explorar la documentación de PromptFlow para crear flujos avanzados.
- Integrar PromptFlow con servicios de Azure AI y OpenAI.
- Configurar flujos de trabajo automáticos con CI/CD en Azure DevOps.
