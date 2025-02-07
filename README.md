# LaTeX devcontainer template
PLantilla de tesis en LaTeX, basado en [CUED PhD thesis template](https://github.com/kks32/phd-thesis-template/tree/master), con [devcontainer](https://containers.dev/).

La utilización de devcontainers en este repositorio le permite
- Trabajar mínimos requerimientos independientemente de software, todas las herramientas y bibliotecas están incluidas en el contenedor
- Actualizar su ambiente de trabajo rápidamente
- Trabajar con on-line con [GitHub Codespaces](https://github.com/features/codespaces)

## Inicio rápido

### Pre-requisitos (solo local)
Para inicializar el repositorio debe tener los siguientes elementos instalados
- Linux Docker Engine: Debe tener alguna implementación de docker funcionando en su PC, se sugieren
    - [Docker](https://docs.docker.com/engine/install/ubuntu/) (Linux)
    - [Docker Desktop](https://docs.docker.com/desktop/) (Windows /MAC )
    - [Rancher Desktop](https://rancherdesktop.io/) (Windows /MAC ). **IMPORTANTE**: cambiar el CONTAINER ENGINE por defecto `dockerd (moby)`, por defecto rancher utiliza `containerd` que requiere ajustes para poder utilizarse
- Visual Studio Code
    - Extension: [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)


### Clonar la plantilla
La mejor forma de utilizar la plantilla es hacer un fork de este repositorio. Haciendo esto podrá actualizar su repositorio con los cambios aquí incluidos.

- [Hacer fork](https://github.com/yuudj/latex-devcontainer-demo)
- Clonar el repositorio resultante en su PC
- Verificar que tiene algún Docker Engine corriendo (vea los pre-requisitos)

### Utilizar la plantilla

En forma local (recuerde los pre requisitos)
- Abrir el repositorio con Visual Studio Code
- Selecciona la opción `Clone In Volume` o `Reopen in Container`. 

![Clone In Volume](https://sarti.dev/blog-images/vscode-clone-in-volume.png)


> [!IMPORTANT]  
> Es importante destacar que en entorno Windows la opción  `Clone In Volume` es mucho mas performante. 

### Agregando cambios
Puede cambiar cualquier archivos. Recuerde que si cambia algún archivo del repositorio original existe la posibilidad de que luego tenga conflictos de Merge.

El devcontainer tiene instalada la extension [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) de @James-Yu que permite la pre-visualización de los cambio a medida que pasan. 

Es importante recalcar que LaTeX compila en PDF y ño que se pre.visualiza es el archivo PDF resultante. Si hay errores de compilación dicho archivo puede quedar en blanco o trunco.

Para mas información sobre este extension se puede consultar la documentación en el [repositorio](https://github.com/James-Yu/LaTeX-Workshop) 

### Compilación manual
Para compilar el documento 

```bash
./compile-thesis.sh compile thesis
```

Si alguna imagen no se actualiza pruebe ejecutar el comando y luego volver a compilar
```bash
./compile-thesis.sh clean thesis
```

### Actualizar plantilla
Desde el repositorio generado por el fork puede hacer una sincronización. 
![Fork Repo](https://docs.github.com/assets/cb-75605/mw-1440/images/help/repository/sync-fork-dropdown.webp)

Para mas información puede [consultar la documentación de GitHub](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork).








