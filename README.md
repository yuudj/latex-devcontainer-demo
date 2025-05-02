# LaTeX devcontainer template
Plantilla de tesis en LaTeX, basado en [CUED PhD thesis template](https://github.com/kks32/phd-thesis-template/tree/master), con [devcontainer](https://containers.dev/).

La utilización de devcontainers en este repositorio le permite
- Trabajar mínimos requerimientos independientemente de software, todas las herramientas y librerías están incluidas en el contenedor
- Actualizar su ambiente de trabajo rápidamente
- Trabajar con on-line con [GitHub Codespaces](https://github.com/features/codespaces)

## Inicio rápido

### Pre-requisitos
Para inicializar el repositorio debe tener los siguientes elementos instalados
- Linux Docker Engine: Debe tener alguna implementación de docker funcionando en su PC, se sugieren
    - [Docker](https://docs.docker.com/engine/install/ubuntu/) (Linux)
    - [Docker Desktop](https://docs.docker.com/desktop/) (Windows /MAC )
    - [Rancher Desktop](https://rancherdesktop.io/) (Windows /MAC ). **IMPORTANTE**: cambiar el CONTAINER ENGINE por defecto `dockerd (moby)`, por defecto rancher utiliza `containerd` que requiere ajustes para poder utilizarse
- Visual Studio Code
    - Extensión: [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)

### Utilización de la plantilla
- Hacer un FORK de este repositorio

### Agregando cambios

### Actualizar plantilla

### Previsualización de los cambios

---

## Información adicional

### Cambios realizados
- La estructura del documento —índices, títulos, encabezados, pie de página, bibliografía, nomenclatura, resumen y abstract— respeta las normas establecidas para la presentación de tesinas de la Licenciatura en Informática de la Universidad Nacional de Hurlingham (UNAHUR).
- Se migró el sistema de referencias a biblatex con soporte para APA y compilación automática con biber.
- Se corrigieron errores de compilación por rutas relativas y permisos de escritura en archivos .aux.

### Compilación automática y uso de `biber`
- Esta plantilla utiliza `biblatex` + `biber` para el manejo de bibliografía.
- El entorno `devcontainer` ya instala automáticamente `biber` y todas las dependencias requeridas.
- La compilación se realiza con `latexmk`, que detecta automáticamente si debe ejecutar `biber` o no.

### Archivos importantes
- `thesis.tex`: archivo principal de la tesis.
- `References/references.bib`: archivo de bibliografía en formato BibTeX.
- `.latexmkrc`: archivo de configuración que fuerza el uso de `biber`.
