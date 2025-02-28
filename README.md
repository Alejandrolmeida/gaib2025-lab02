# Workshop: Preparación de entornos de desarrollo para IA con Microsoft AI Foundry

Bienvenido a este workshop de 4 horas donde aprenderás a configurar un entorno de desarrollo optimizado para proyectos de inteligencia artificial en **Microsoft AI Foundry**. Durante el taller, seguirás una serie de pasos detallados y ejercicios prácticos para instalar, configurar y optimizar las herramientas necesarias.

## 📌 Contenidos
Cada sección contiene instrucciones paso a paso, posibles errores y sus soluciones, así como ejercicios prácticos:

1. [Instalar Linux WSL en un equipo Windows](wsl-install.md) 🖥️
2. [Desplegar una VM Linux en Azure y conectarse por SSH](azure-vm-ssh.md) ☁️
3. [Crear entornos virtuales dentro de Linux](virtual-envs.md) 🔄
4. [Instalar Miniconda en WSL y crear entornos Conda](miniconda-install.md) 🐍
5. [Instalar Python y dependencias de un proyecto con PIP](python-pip.md) 📦
6. [Personalizar la Shell con Oh My Posh](ohmyposh.md) 🎨
7. [Instalar Docker Desktop](docker-install.md) 🐳
8. [Instalar VS Code y conectar con WSL en remoto](vscode-wsl.md) 🛠️
9. [Instalar DevContainers](devcontainers-install.md) 📂
10. [Instalar Bicep y desplegar una plantilla en Azure](bicep-install.md) 📜
11. [Instalar PromptFlow](promptflow-install.md) 🤖

---

## 🏁 Requisitos previos
Antes de comenzar, asegúrate de contar con:
- **Windows 10/11** con soporte para WSL 2 habilitado.
- Una **cuenta de Azure** con permisos para crear recursos.
- Conocimientos básicos de **Linux y terminal**.
- Instalación de **VS Code** y **Docker Desktop**.

## 🔧 Instalación rápida
Si deseas preparar rápidamente tu entorno, sigue estos pasos iniciales:
1. **Habilitar WSL:**
   ```powershell
   wsl --install
   ```
2. **Instalar Docker Desktop y VS Code** desde sus sitios oficiales.
3. **Configurar Azure CLI** y autenticarse:
   ```powershell
   az login
   ```
4. **Clonar este repositorio** para acceder a las guías completas:
   ```bash
   git clone https://github.com/tuusuario/workshop-ai-foundry.git
   ```

## 📖 ¿Cómo usar este workshop?
Cada sección está documentada en su respectivo archivo `.md`. Puedes seguir el orden sugerido o explorar las secciones de forma independiente.

- Para configuraciones en Windows, sigue las instrucciones de **WSL, Docker y VS Code**.
- Si trabajas en **Azure**, revisa las guías sobre **VMs, Bicep y PromptFlow**.
- Para entornos de desarrollo de IA, instala **Python, Miniconda y DevContainers**.

## 🚀 Próximos pasos
Una vez configurado tu entorno, puedes:
- Crear y entrenar modelos de IA en **Azure AI Foundry**.
- Integrar contenedores y despliegues con **Docker y Bicep**.
- Automatizar flujos de trabajo con **PromptFlow**.

¡Listo para empezar! 💡
