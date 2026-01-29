[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/-TPlsu0Q)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=22439046&assignment_repo_type=AssignmentRepo)
# 🛠️ Configuración para Instrumentación y Control / Robótica

¡Bienvenidos a la primera tarea del curso! El objetivo de esta actividad es que configures en tu computadora todas las herramientas que usaremos durante el semestre. Sigue los pasos a continuación.

Cuando termines, entra a la [Tarea 1](Instrucciones.md).

## 📦 Software Obligatorio a Instalar

**1. Para documentos y reportes técnicos (LaTeX):**
*   **MiKTeX**: Distribución principal de LaTeX. Descárgalo desde [miktex.org](https://miktex.org/download).
*   **TeXstudio**: Editor para escribir documentos LaTeX de forma más sencilla. Descárgalo desde [texstudio.org](https://www.texstudio.org/).

**2. Para el control de versiones y tareas:**
*   **Git**: Sistema de control de versiones. Descarga el instalador desde [git-scm.com](https://git-scm.com/).
*   **Cuenta de GitHub**: Regístrate de forma gratuita en [github.com](https://github.com/). Usa un correo que revises frecuentemente.
*   **GitHub Classroom**: Para acceder a las tareas, usa el enlace especial que te proporcionará tu profesor.

**3. Para programación y desarrollo:**
Abre la tienda de Windows y busca:
*  **Python Install Manager**: Al instalarse, abrelo y se va a ejecutar una terminal. Lee detalladamente y escribe "y" (yes) para aceptar o "n" (no) para denegar el proceso que te piden. Si nunca has instalado python, probablemente lo único que tengas que hacer es aceptar, ya que la tecla por defecto es la que está en MAYÚSCULAS.
*  **Arduino IDE**: Es el software que se usará para programar la tarjeta Arduino. **NO SELECCIONAR Arduino IDE 2**.
*  **Visual Studio Code**: Editor de código principal. Ábrelo e inicia sesión en el botón de la barra lateral izquierda, abajo, donde dice cuentas.

### ✅ Verifica tu instalación
Abre una terminal (`cmd` o PowerShell) y ejecuta estos comandos para confirmar que todo está listo:
```bash
git --version
python --version
code --version
```
Si cada comando devuelve un número de versión, ¡vas por buen camino!

## 🚀 Introducción a GitHub y GitHub Classroom

### 🤔 ¿Por qué usamos esto?
En este curso, no solo aprenderás los fundamentos de la instrumentación y el control, sino también las herramientas profesionales que los ingenieros usan para colaborar. GitHub es la plataforma donde gestionaremos, versionaremos y entregaremos todo nuestro trabajo (código, modelos, diagramas y reportes).

GitHub Classroom es una extensión para profesores que permite organizar y revisar tareas de manera eficiente. Cada vez que haya una nueva práctica o proyecto, recibirás un enlace que te creará un repositorio personal o de equipo para trabajar.

### :octocat: Conceptos Básicos de Git y GitHub
Git es un Sistema de Control de Versiones Distribuido (VCS). En términos simples, es como un "historial infinito de 'Guardar como'" para tus proyectos. Te permite:

- Rastrear cada cambio en tus archivos de código, modelos o documentación.
- Volver a cualquier versión anterior de tu trabajo en cualquier momento.
- Colaborar sin sobrescribir el trabajo de otros.

GitHub es la plataforma en la nube que usa Git, añadiendo una interfaz web, herramientas de colaboración (como Issues y Pull Requests) y servicios como GitHub Classroom.

### El Flujo de Trabajo Básico (Workflow)

- **Repositorio (Repo)**: Es la "carpeta del proyecto" en GitHub. Contiene todos los archivos y su historial. En este curso, Classroom creará un repo por tarea para ti.

- **Clonar (Clone)**: Descargar el repositorio remoto de GitHub a tu computadora local para poder trabajar en él. Se hace con el comando `git clone <URL>`.

- **Commit**: Es un "paquete" de cambios que guardas localmente en tu máquina. Debe incluir un mensaje claro que explique qué hiciste (ej: "Añadido modelo matemático del sensor LVDT").

- **Subir (Push)**: Enviar los commits que hiciste localmente al repositorio remoto en GitHub, para que tu profesor y compañeros de equipo los vean.

- **Ramas (Branches)**: Líneas de desarrollo paralelas. Te permiten trabajar en nuevas funciones (ej: "mejora-del-pid") sin tocar la versión principal (main). ¡Las usaremos en proyectos grandes!

- **Pull Request (PR)**: Una solicitud para fusionar los cambios de una rama en otra. Es el mecanismo para revisar código y discutir mejoras antes de integrarlas.

⚠️ Conflictos de Merge
A veces, Git no puede fusionar automáticamente porque hay cambios conflictivos. Deberás:

Abrir el archivo conflictivo en tu editor.
Resolver manualmente qué cambios mantener.
Hacer commit después de resolver.

## 🚀 Primeros Pasos

1. **Clona el repositorio:**
   ```bash
   git clone <URL-del-repositorio>
   cd <nombre-del-repositorio>
   ```

2. **Configura tu entorno de Python (si lo usas):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # En Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

2. **Realiza cambios y haz commits (puedes hacerlo desde la IDE de Visual Studio):**
   ```bash
   git add .
   git commit -m "Descripción clara de los cambios"
   git push origin main
   ```

## 📝 Notas Importantes

- **No subas archivos compilados** (PDFs, archivos .o, `__pycache__`, etc.). El `.gitignore` se encarga de esto automáticamente.
- **Usa mensajes descriptivos** en tus commits para que se entienda qué hiciste.
- **En Python**: Siempre trabaja dentro del entorno virtual (`venv`).
- **En LaTeX**: Guarda solo los archivos `.tex` y figuras; los PDFs se generan localmente.
- **En Arduino**: Cada proyecto debe estar en su propia carpeta.