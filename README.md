# 📘 Plantilla de Tesina en LaTeX con Devcontainer
Plantilla de tesis en LaTeX, basado en [CUED PhD thesis template](https://github.com/kks32/phd-thesis-template/tree/master), con [devcontainer](https://containers.dev/).

---

## ⚙️ La utilización de devcontainers en este repositorio permite:
1. Trabajar mínimos requerimientos independientemente de software, todas las herramientas y librerías están incluidas en el contenedor
1. Actualizar su ambiente de trabajo rápidamente
1. Trabajar con on-line con [GitHub Codespaces](https://github.com/features/codespaces)

## 🚀 Inicio rápido

### 🔧 Pre-requisitos
**Para inicializar el repositorio debe tener los siguientes elementos instalados**:
- Linux Docker Engine: Debe tener alguna implementación de docker funcionando en su PC, se sugieren
    - [Docker](https://docs.docker.com/engine/install/ubuntu/) (Linux)
    - [Docker Desktop](https://docs.docker.com/desktop/) (Windows /MAC )
    - [Rancher Desktop](https://rancherdesktop.io/) (Windows /MAC ). **IMPORTANTE**: cambiar el CONTAINER ENGINE por defecto `dockerd (moby)`, por defecto rancher utiliza `containerd` que requiere ajustes para poder utilizarse
- Visual Studio Code
    - Extensión: [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)

### 🛠️ Usar la plantilla

1. Hacer un **fork** del repositorio.
2. Abrir el proyecto en VS Code.
3. Aceptar la apertura en el contenedor.
4. ¡Listo! El entorno estará listo para compilar.

---

## 📄 Archivos importantes

- `thesis.tex`: archivo principal que organiza la estructura del documento mediante `\include{}`.
- `Preamble/preamble.tex`: configuración de paquetes, márgenes, estilo, y bibliografía.
- `thesis-info.tex`: información como título, autor, director, fecha, etc.  (acá se definen los datos de la carátula) y metadatos del documento.
- `References/references.bib`: archivo de bibliografía en formato BibLaTeX.
- `Resumen/resumen.tex`: resumen en español.
- `Abstract/abstract.tex`: abstract en inglés.
- `Dedication/dedication.tex`: dedicatoria opcional.
- `ChapterX/chapterX.tex`: capítulos individuales (incluirlos desde `thesis.tex`).
- `AppendixX/appendixX.tex`: apéndices opcionales.

---

## 🔁 Compilación automática y bibliografía

- Usa `latexmk` con `biber` para compilar automáticamente y generar bibliografía con URLs y DOIs.
- El `devcontainer` instala todas las herramientas necesarias (LaTeX, `latexmk`, `biber`, etc.).
- Solo necesitás guardar el archivo para que se compile automáticamente si usás VS Code.

---

## ✏️ Personalizaciones realizadas (respecto a la plantilla original)

- Estructura adaptada a las normas de presentación de tesinas de UNAHUR.
- Inclusión de `Resumen` además del `Abstract`.
- Cambio de “Supervisor” por “Director de tesina”.
- Migración de `natbib` a `biblatex` para permitir el uso de URL y DOI en las referencias.
- Cambio de idioma de a español utilizando `babel`.
- Ajustes en títulos, índices, pie de página, nomenclatura y encabezados.
- Cambio de tablas a `longtable` que permite la paginación automática.

---

## 👁️ Previsualización de cambios

La compilación genera automáticamente un PDF en la raíz del proyecto (`thesis.pdf`). Cualquier cambio en el contenido se reflejará tras guardar el archivo `.tex`.

---

