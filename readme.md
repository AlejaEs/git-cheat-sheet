# Práctica de comandos de Git.

**Puedes ver la página web [desde aqui](https://chybeat.github.io/git-cheat-sheet/)**

---

### Ten en cuenta:

-  Los comandos se deben ejecutar desde Git Bash o la terminal de Linux.
-  El texto entre llaves en los comandos lo debes cambiar según se te indique o por el texto que mejor te parezca.
   Ejemplo:
   Quieres cambiar el nombre de la carpeta 'git-cheat-sheet' por 'proyectito-git'.
   \
    En esta ayuda encontrarás un código como: `mv git-cheat-sheet {nuevo_nombre}`.
   \
   Debes escribir: `mv git-cheat-sheet proyectito-git`
   \
   El texto a cambiar estará dentro de llaves `{}` y el texto que elijas o requieras debe ir sin llaves.

---

## Crear un repositorio

1. Generar un achivo readme.md
   `echo "Mi repositorio" >> readme.md`

   > Genera un archivo readme.md con el texto 'Mi repositorio'. (Puede utilizarse cualquier texto).

1. `git init`

   > Inicialización de un repositorio local.

1. `git add readme.md`

   > Agrega a el archivo 'readme.md' para ser observado (stage) por git.

1. `git commit -m "first commit"`

   > Guarda los archivos que estan siendo 'observados' (staged).

1. `git branch -M main`

   > Cambia el nombre de la rama actual a 'main'. La rama actual generalmente es "Master".

1. `git remote add origin {repositorio_remoto}`

   > Agrega a mi repositorio local un sitio remoto desde donde llamar o enviar los archivos del repositorio. La palabra 'origin' es una sugerencia y buen práctica para el nombre, pero puede colocarse cualquier nombre. Adicionalmente existen 2 métodos para la conexión al repositorio remoto y que hay que tener en cuenta para cambiar en `{repositorio_remoto}` (sin llaves), uno si se utilizan llaves (SSH) y otro si utiliza nombre de usuario y contraseña (HTTPS).

   > **SSH**: {repositorio_remoto} cambia por: `git@github.com:{usuario}/{nombrerepositorio}.git`

   > **HTTPS**: {repositorio_remoto} cambia por:`https://github.com/{usuario}/{nombrerepositorio}.git`

   > Se debe tener en cuenta que ninguna dirección lleva llaves, ni en el usuario, ni en el nombre del repositorio. Ej: `https://github.com/chybeat/git-cheat-sheet.git` ó `git@github.com:chybeat/git-cheat-sheet.git`.

1. `git push -u origin main`
   > Envía los archivos hasta 'origin' desde la rama 'main'. La bandera -u coloca la rama 'main' como la rama predeterminada para sincronizar en el repositorio remoto.

---

## Realizar un fork para contribuir a este repositorio

1. Haz Fork desde el repositorio principal a tu cuenta en github.

   > Abrir el [repositorio principal](https://github.com/AlejaEs/git-cheat-sheet) y haz clic en el botón de 'Fork'.

1. `git clone https://github.com/{usuario}/git-cheat-sheet.git`

   > Clona el repositorio al que acabas de hacer fork desde tu cuenta de GitHub a la carpeta para proyectos de tu computador. `{usuario}` se debe reemplazar por el nombre de tu usuario en github. Las direcciónes HTTPS y SSH las puedes encontrar en el botón 'Code' del repositorio en tu cuenta de gitHub.

1. `cd git-cheat-sheet/`

   > Entra en la carpeta de tu repositorio local. Puedes renombrar la carpeta local con el comando
   > \
   > `mv git-cheat-sheet {nuevo_nombre}`
   > antes de acceder a la carpeta.

1. `git remote add upstream git@github.com:AlejaEs/git-cheat-sheet.git`

   > Agregar el [repositorio principal](https://github.com/AlejaEs/git-cheat-sheet) (el de [AljeaES](https://github.com/AlejaEs)) como el origen remoto desde donde se traerá la ultima version del código subido por todos. **Ten en cuenta que:** la dirección cambia según la conexión, sea HTTP o SSH y `upstream` es un nombre sugerido y una buena practica, pero puedes colocar cualquier nombre.

1. `git pull upstream main`

   > Obtener la última actualización de los archivos desde el [repositorio principal](https://github.com/AlejaEs/git-cheat-sheet) (el de [AljeaES](https://github.com/AlejaEs) lo mismo que `upstream`) en tu repositorio local. _¡¡Este paso se debe realizar cada vez que vayas a trabajar en el proyecto!!_.

1. Trabaja en alguno de los archivos en tu editor de código

   > Manos a la obra!. Comienza a realizar aportes, correciones, mejoras y todo lo que pueda contribuir a mejorar este proyecto!.

1. `git add .`

   > Agrega todo el nuevo contenido al staging de tu repositorio local.

1. `git commit -m "{explicar el nuevo cambio}"`

   > Realiza un commit a tu repositorio con los cambios realizados. La bandera `-m` permite escribir un mensaje para el commit. En el mensaje de modo muy resumido, cuéntanos que hiciste.

1. `git push origin main`

   > Sube tus cambios al repositorio en Github (a tu cuenta). Debes saber que 'origin' se estableció automáticamente cuando realizaste `git clone ...`

1. Solicita un Pull request!

   > En la página web de tu repositorio, busca la pestaña "Pull request", y da click en el botón "New pull request", desde allí se enviaran los cambios al repositorio principal.

   **Recuerda**: Siempre haz pull de las ultimas versiones antes de trabajar desde el repositorio principal con `git pull upstream main`

---

**Puedes ver la página web [desde aqui](https://chybeat.github.io/git-cheat-sheet/)**
