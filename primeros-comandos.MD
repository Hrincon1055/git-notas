## Primeros comandos Git.

---

### git --version

Indica la version instalada de git.

### git help

Mostra el listado de comandos disponibles para nuestro uso.

### git clone

Clona un repositorio dentro de un nuevo directorio.

_Puedes clonar este repo para estudiar git._

```
git clone https://github.com/Hrincon1055/git-notas.git
```

---

### git init

Inicializa el proyecto para empesar a trabajar con git y darle seguimiento al proyecto.

### git status

Muestra el esttus de los archivos.
_En este ejemplo nos muestra las carpetas no segidas para el seguimiento_

```sh
PS D:\proyectos\git\01-bases> git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .DS_Store
        css/
        fonts/
        images/
        index.html
        js/
        main.html
        scss/

nothing added to commit but untracked files present (use "git add" to track)
PS D:\proyectos\git\01-bases>
```

### git add

Permite dar segimiento a los archivos, indicando la propiedad `"." punto` para indicar todos los archivos o in dicando el nombre de cada archivo.

```sh
git add index.html
git add .
```

`git add index.html`

```sh
PS D:\proyectos\git\01-bases> git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .DS_Store
        css/
        fonts/
        images/
        js/
        main.html
        scss/

PS D:\proyectos\git\01-bases>
```

`git add .`

```sh
PS D:\proyectos\git\01-bases> git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   .DS_Store
        new file:   css/.DS_Store
        new file:   css/bootstrap.min.css
        new file:   css/bootstrap/.DS_Store
        new file:   css/bootstrap/_media.css
        new file:   css/bootstrap/mixins/.DS_Store


PS D:\proyectos\git\01-bases>
```

Si ejecutamos el comando status podemos ver los archivos que se estaran marcados para subir en el siguiente commit, pero si desamos retirar algun archivo ejecutaremos el comando `git reset .DS_Store`

### git commit

Agregara al state los cambios propuesto en la adicion de archivos con el comando `git add .`

```sh
git commit -m
```

podemos indicar el parametro `-m` para colocar un mensaje que indentifica el grupo de cambios propuesto.
