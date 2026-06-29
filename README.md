# Taller Práctico: Mi Primer Repositorio Profesional y Entorno Aislado

Este repositorio contiene el desarrollo del primer taller práctico correspondiente al **Módulo 1: Ciencia de Datos, Inteligencia Artificial y Gestión de Proyectos para la Industria 4.0** de la **Fundación Universitaria de Sangil (Unisangil)**, Sede Chiquinquirá.

El objetivo del proyecto es establecer un flujo de trabajo profesional utilizando Git, GitHub, entornos virtuales de Python (`venv`) y la gestión de dependencias en un sistema operativo Linux (Arch Linux).

---

## 🛠️ Tecnologías y Herramientas Utilizadas

* **Control de Versiones:** Git & GitHub
* **Lenguaje de Programación:** Python 3
* **Gestor de Entornos:** `venv` (Python Virtual Environment)
* **Librerías Clave:** Pandas
* **Sistema Operativo:** Arch Linux

---

## 📋 Estructura del Proyecto y Pasos Realizados

### Parte 1: Creación del Repositorio en la Nube
Se creó el repositorio remoto en GitHub con las siguientes especificaciones:
* **Nombre:** `taller-data-science`
* **Visibilidad:** Público
* **Inicialización:** Archivo `README.md` y Licencia MIT.
* **Colaboración:** Se configuró un compañero como colaborador desde la pestaña de *Settings > Collaborators*.

---

### Parte 2: Clonación y Preparación del Entorno Local
Se clonó el repositorio en el equipo local utilizando la terminal de comandos:

# Clonar el repositorio remoto
git clone https://github.com/GabitooGeek/taller-data-science.git

# Acceder al directorio del proyecto
cd taller-data-science

Parte 3: Configuración del Archivo de Exclusión (.gitignore)

Para evitar el seguimiento de archivos innecesarios de Python y del entorno virtual, se configuró el archivo .gitignore antes de inicializar el entorno:

    Creación del archivo .gitignore:
    Se configuró para ignorar la carpeta del entorno virtual .venv/.
    code Bash

    nano .gitignore
    # Contenido interno: .venv/

    Creación del entorno virtual:
    code Bash

    python -m venv .venv

    Verificación y primer commit en la rama main:
    Se comprobó mediante git status que el entorno virtual .venv fuese correctamente ignorado, dejando únicamente el archivo .gitignore disponible para seguimiento.
    code Bash

    git add .gitignore
    git commit -m "Agregar archivo .gitignore"

Parte 4: Activación e Instalación de Dependencias

Se activó el entorno virtual en Linux y se instalaron las librerías de trabajo:

    Activación del entorno virtual:
    code Bash

    source .venv/bin/activate

    Instalación de Pandas:
    code Bash

    pip install pandas

    Generación del archivo requirements.txt:
    Se exportaron las versiones exactas de las dependencias para asegurar la reproducibilidad del proyecto.
    code Bash

    pip freeze > requirements.txt

Parte 5: Gestión de Ramas y Publicación en GitHub

Siguiendo las buenas prácticas de desarrollo, los cambios no se subieron directamente a la rama principal, sino a una rama de desarrollo secundaria:

    Creación y cambio a la nueva rama:
    code Bash

    git checkout -b rama1

    Registro de cambios en la rama local:
    code Bash

    git add requirements.txt
    git commit -m "Agregar requirements.txt con la libreria pandas"

    Envío de la rama al repositorio remoto:
    code Bash

    git push -u origin rama1

    Desactivación del entorno de trabajo:
    code Bash

    deactivate

🗂️ Arquitectura del Repositorio Final

El repositorio en GitHub quedó estructurado con la siguiente distribución de ramas y archivos:
Rama	Archivos Incluidos	Propósito
main	LICENSE, README.md, .gitignore	Rama principal estable con la configuración base de exclusión.
rama1	LICENSE, README.md, .gitignore, requirements.txt	Rama secundaria con las dependencias del entorno de ciencia de datos instaladas.

Este proyecto fue desarrollado como parte de las actividades prácticas del Diplomado en Ciencia de Datos, Inteligencia Artificial y Gestión de Proyectos para la Industria 4.0 - Unisangil.
code Code
