<p align="center">
  <a href="https://github.com/" target="blank"><img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" width="200" alt="Git Logo" /></a>
</p>

# __GIT__

## Listado de comandos para __git__
A continuación encontraras un listado de comando usuales y poco usales que te serviran en el día a día usando Git.

- `git --version` : Sirve para saber que version de __git__ tengo instalada en mi pc.
- `git help` : Nos muestra los diferentes comandos que podemos usar con git.
- `git help commit` : Saber mas acerca del comando `commit` .

Para configurar git en nuestro pc localmente
- `git config --global user.name "usuario_ejemplo"` : Establece el usuario de git localmente.
- `git config --global user.email "correo_ejemplo@gmail.com"` : Establece el email localmente.
- `git config --global -e` : Lista mis usuarios.

Inicializar repositorios
- `git init` : Inicializar un repositorio.
- `git status` : Saber que archivos han sido modificados o no se les esta dando segumiento por parte de __git__. O tambien podemos verlo como un resumen breves de los cambios.
- `git add nombre_archivo` : Le dice a git que le haga seguimiento a ese archivo en especifíco.
- `git add .` : Prepara todos los archivos y los sube al __stage__ para darles seguimiento.
- `git reset nombre_archivo` : Remueve archivos para no darles seguimiento.
- `git commit -m ""` : Toma la fotografía de como está el repositorio hasta ese momento.
- `git checkout -- .` : Restaura todos los archivos a como los tenia antes del último commit.
- `git branch` : Muestra todas las ramas que tengo en el repositorio.
- `git branch -m master main` : Renombrar una rama en este caso la rama __master__ la renombramos como __main__.
- `git config --global init.defaultbranch <main>` : Para que todos mis repositorios se inicien con la rama __main__ en este caso, _los símbolos *<>* no van__.
- `git commit -am "mi mensaje"` : Con este comando nos ahorramos el comando `git add .` ya que la bandera `-am` añade y los archivos y también el mensaje sirve para cuando __git__ ya está dando seguimiento a los archivos.
- `git log` : Nos muestra los log's de nuestro repositorio, nos muestra información sobre los __commits__ como autor mensaje, entre otros.
- `git add *.html` : Para agregar al __stage__ todos los archivos que terminan en __.html__.
- `git add /carpeta` : Toma todo lo que esta dentro de la carpeta y lo pone en el __stage__ para darle seguimiento.

Alias en git
- `git config --global alias.s status --short` : Crea un alias llamado __"S"__ y lo que hace es hacer el comando `git status` mas corto quedando así: `git s` y hace lo mismo.
- `git config --global -e` : Hacer modificaciones de un alias.
- `git log --oneline` : Muestra cada uno de los commits que hayamos realizado en el repositorio.
- `git log --oneline --decorate --all --graph` : Muestra todo el árbol tanto de commits como de ramas absolutamente todo **(código de commit, hace cuanto se hizo, commit, auor, rama)**. Ejemplo:
```
* da6b666 (HEAD -> main, origin/main) Sitio Web Listo
* 3feee0e Update issue templates
* 44f9d4d Update issue templates
* 46c0b9f Update issue templates
| * d49ffa3 (rama-web) Sitio Web Listo
|/
* 6f6f3c2 Fixes #4: Hecho, borre a la capitan marvel
* 2d80aec Agregamos a Nick Fury
| * ce80c80 (tag: V1.0.0, origin/rama-kitkat, rama-kitkat) Capitan america goesmad
|/
*   a7d46aa Merge pull request #2 from rondrea2021/rama-misiones
|\
| * d7a3249 Misiones Actualizadas
| * f93b7cf Create misiones.md
|/
*   6043614 Merge pull request #1 from rondrea2021/rama-villanos
|\
| * e9f68a9 Dr Herrera agregado
| * 9aff64c villanos.md agregado
|/
* 1172319 (tag: V0.0.1) Solución de la tarea curso-git
```
Fuente: [Curso Git - Fernando Herrera](https://cursos.devtalles.com/courses/git-github-control-versiones)

Para hacer el alias del comando anterior ejecutamos el siguiente comando:
- `git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"` : Crea el alias llamado __lg__ donde podemos ver lo mismo que el comando anterior. Y nos queda mas corto asi: `git lg`.
Ejemplo de salida:
```
>terminal: git lg
* da6b666 - (20 hours ago) Sitio Web Listo - Ronaldo (HEAD -> main, origin/main)
* 3feee0e - (6 weeks ago) Update issue templates - Ronaldo Torres C
* 44f9d4d - (6 weeks ago) Update issue templates - Ronaldo Torres C
* 46c0b9f - (6 weeks ago) Update issue templates - Ronaldo Torres C
| * d49ffa3 - (20 hours ago) Sitio Web Listo - Ronaldo (rama-web)
|/
* 6f6f3c2 - (6 weeks ago) Fixes #4: Hecho, borre a la capitan marvel - Ronaldo
* 2d80aec - (6 weeks ago) Agregamos a Nick Fury - Ronaldo
| * ce80c80 - (6 weeks ago) Capitan america goesmad - Ronaldo (tag: V1.0.0, origin/rama-kitkat, rama-kitkat)
|/
*   a7d46aa - (6 weeks ago) Merge pull request #2 from rondrea2021/rama-misiones - Ronaldo Torres C
|\
| * d7a3249 - (6 weeks ago) Misiones Actualizadas - Ronaldo
| * f93b7cf - (6 weeks ago) Create misiones.md - Ronaldo Torres C
|/
*   6043614 - (6 weeks ago) Merge pull request #1 from rondrea2021/rama-villanos - Ronaldo Torres C
|\
| * e9f68a9 - (6 weeks ago) Dr Herrera agregado - Ronaldo
| * 9aff64c - (6 weeks ago) villanos.md agregado - Ronaldo
|/
* 1172319 - (6 weeks ago) Solución de la tarea curso-git - Ronaldo (tag: V0.0.1)
```
- `git diff` : Me indica que modificaciones he realizado. Si ejecutamos `git diff --help` me lleva al navegador y me da mas información acerca del comando.
- `git commit --amend -m "mensaje actualizado"` : Actualiza el mensaje anterior en la linea de tiempo de los __commits__.
- `git reset --soft` : Revierte el commit. importante hacer antes de que se haya echo __push__(mas adelante hablaremos sobre el comando __push__).
- `git reset --soft HEAD^` : Revisar un __commit__.
- `git reset --soft a122e4` : Volver en el tiempo a un commit en especifico usando el identificador del __commit__. ejemplo de indentificador o hash del __commit__ `f93b7cl`.
- `git reset --mixed a122e4` : Volver en el tiempo eliminando commits pero manteniendo los cambios.
- `git reser --hard a122e4` : Deja el repositorio como estaba en el punto al que se revierte o se hace reset.
- `git reflog` : Nos muestra todo lo que ha sucedido en orden cronológico.

Con __git__ tambien podemos renombrar nuestros archivos o eliminarlos.

- `git mv nombre_antiguo.js nombre_nuevo.js` : Cambiar el nombre del archivo.
- `git rm -f nombre_archivo.py` : Eliminar un archivo mediante __git__.

# Ramas en __Git__
- `git branch "nombre_rama"` : Crear una nueva rama(sin las __""__).
- `git branch` : Para mostrar todas las ramas.
- `git checkout "nombre_rama"` : Para cambiarme a otra rama.
- `git merge "nombre_rama"` : Para unir dos ramas, __importante*__(debo estar posicionado en la rama donde quiero que se unan).
- `git branch -d "nombre_rama"` : Eliminar la rama.
- `git branch -d "nombre_rama" -f` : Eliminar la rama de manera forzada.

#### Merge: Unión Automática
- `git checkout -b "nombre_rama"` : Crear una nueva rama y cambiarme automaticamente a ella, la bandera `-b` es de __branch__.

### Conflictos
Las confictos en __git__ nos salen cuando intentamos unir dos ramas que han sufrido cambios, __git__ nos dice donde están los conflictos y los **solucionamos manuelmente**.

## Tags
- `git tag "super-release"` : Crea una etiqueta de mi código.
- `git tag` : Ver todas las tags o etiquetas que tengo.
- `git tag -d "nombre_tag"` : Eliminar un tag.
- `git tag -a V1.0.0 -m "Versión 1.0.0 Lista"`: Crear un tag o etiqueta de una version en esté caso modo semantica, la bandera `-a`= _anotada_ y la bandera `-m` = _para colocar el mensaje en la eqtiqueta o tag_.
- `git tag -a V0.1.0 -m "versión alpha" -9506846` : Crear un tag basado en el hash de un __commit__.
- `git show V1.0.0` : Para ver mas información sobre el __tag__.

#### Nota: WIP : Working progress

# Git Stash
[Más información](https://git-scm.com/docs/git-stash) o [aquí](https://www.atlassian.com/es/git/tutorials/saving-changes/git-stash)
- `git stash` : Poner cambios en __stash__, que todavía no están listos para ser subidos. El __stash__ de __git__ almacena tamporalmente.
- `git stash list` : Ver las referencias del __stash__.
- `git stash pop` : Recuperar nuestro __stash__. Lo deja como estaba y mantienen los cambios o el último.
- `git stash clear` : Limpiar el __stash__ sin que me afecte el repositorio con conflictos.
- `git stash apply "stash@{2}"` : Recuperar un __stash__ en particular-especifico. **OJO** depende de la terminal puede ir o no en __""__.
- `git stash drop 'stash@{0}'`: Eliminar un __stash__ específico.
- `git stash show 'stash@{1}'` : Ver información del __stash__ en particular.
- `git stash save "Mensaje indentificador"` : Colocar un mensaje al __stash__ para mayor comodidad.
- `git stash list --stat` : Ver más información sobre lo que tengo en mi __stash__.

### Git rebase
[Más Información](https://git-scm.com/docs/git-rebase)

- `git rebase master` : Hacer __rebase__ de los __commits__ de mi rama master a otra rama, debo de estar posicionado en la rama donde quiero recuperar los __commits__.

#### __Nota__: hacer rebase si los cambios están locales en tu equipo. No después de hacer __push__.

#### Squash: Fusionar dos ramas (rebase)
**~ = Virgulilla**
- `git rebase -i HEAD~3` : Combinar dos commits, una vez ejecutamos el comando nos abrira el editor, presionamos `a` para insertar y remplazamos _pick_ por `s` o `squash` solo en el __commit__ que queremos combiar, luego damos `esc` seguidamente colocamos `:wq` que significa escribir y salir, luego nos aparece otro editor lo podemos dejar asi y nuevamente `esc` y seguidamente colocamos `:wq` y enter para finalizar nos debe salir asi: 
```
Successfully rebased and updated refs/heads/main.
```
#### Rewor: Renombrar un commit
- `git rebase -i HEAD~4` : También nos permite renombrar un __commit__ tocamos `a` para editar, cambiamos _pick_ por r de __reword__ luego `esc` y finamente ``:wq` y enter(mismo proceso anterior).
#### Edit: Editar un rebase interactivo
- `git rebase -i HEAD~3` : También nos permite editar el commit de manera manual con __rebase__. En el editor cambiar pick por `e` o `edit` de editar y segumos los pasos. Luego:
- `git rebase continue` : Para continuar con el __rebase__ interactivo.
- `git reset HEAD^` : Bajar del __stage__ los cambios.
- `git rebase --continue` : Termina el rebase interactivo.

# __Git Hub__
Acá ya hablaremos del __push__
- `git remote add origin <link_repo>` : Con esté comando tenemos acceso remoto al repositorio en la nube.
- `git push origin main` : Subir los archivos al repositorio remoto.
- `git push --tag` : Para subir todas las tags o etiquetas que hemos creado.
- `git pull` para traer los datos que están en el origen setados por defecto.
- `git pull origin main` : Para epecificar la rama y traer los datos de dicha rama.
- `git remote -v` : Para ver el path donde se encuentra nuestro repositorio.

#### Configuracion para ``git pull``
- `git config --global pull.ff only` : Para cuando haga el pull, tambien haga el forward de los cambios o si no solucionamos los conflictos manualmente.
- `git clone <link_repo>` : Clonar nuestro repositorio tal cual como está.
- `git config --global pull.rebase true` : Para dejar de forma global el rebase con los conflictos.

#
- `git fetch` : Para actualizar mi repositorio pero no hace merge como tal.
- `git pull` : Para unificar luego del `fetch`.
- `git checkout hash nombre_archivo` : Revertir cambios en un único archivo.
- `git push --set-upstream origin <nombre_rama>` : Para subir la rama al repositorio.
- `git pull --all` : Para traer todas las ramas.
- `git branch -a` : Ver todas las ramas que he creado, eliminado y bajado.

## Limpiar las ramas
- `git push origin "nombre_rama"` : Para subir la rama tanto local como de github. Solo si existen el remoto.
- `git remote prune origin` : Revisa las ramas que en el remoto ya no existen y si no existen las limpia de mis referencias locales.
- `git commit -am "fixes #4: mensaje"` : Para cerrar un Iusse Automaticamente

# Créditos
[Fernado Herrra](https://fernando-herrera.com/)