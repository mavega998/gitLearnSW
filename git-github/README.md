### ¿Qué es Git?

**GIT** es un sistema de control de versiones distribuido, rápido y escalable
cuenta con un conjunto de comandos que proporciona operaciones de alto nivel y acceso completo a los 
componentes internos

Algunas de las características a destacar de **GIT**
* Es muy potente.
* Fue diseñado por Linus Torvalds.
* Es software Libre.
* Es muy rápida.
* Tiene un sistema de trabajo con ramas que lo hace especialmente potente. 

### ¿Qué es GitHub?

**GitHub** es un sitio web y un servicio en la nube que ayuda a los desarrolladores a almacenar
y administrar su código, también puede llevar un registro y control de cualquier cambio sobre el código.

**GitHub** es una compañía sin fines de lucro que ofrece un servicio de hosting de repositorios almacenados en la nube. Esencialmente, hace que sea más fácil para individuos y equipos usar **Git** como la versión de control y colaboración.

La interfaz de **GitHub** es bastante fácil de usar para el desarrollador novato que quiera aprovechar las ventajas del **Git**. Sin **GitHub**, usar un **Git** generalmente requiere de un poco más de conocimientos de tecnología y uso de una línea de comando.
- Fuente: [¿Qué es GitHub? ](https://kinsta.com/es/base-de-conocimiento/que-es-github/)

### Comandos comúnes de Git

Algunos de los comandos mas comúnes que nos escontramos en el día a día usando git son:

* ```git --version``` Usamos este comando para verificar que version de **GIT** tengo instalada en mi ordenador.
* ```git init``` Este comando se usa para inicializar un repositorio con **GIT**.
* ```git status``` Con este comando podemos saber que archivos no les está dando seguimiento **GIT** o aquellos que han sido modificados.
* ```git add .``` Este comando prepara todos los archivos del repositorio y los sube al stage para que **GIT** les haga seguimiento.
* ```git commit -m ``` Con este comando hacemos una captura por asi llamarlo de como tenemos nuestro código hasta ese momento en el cual hacemos nuestro commit.
* ```git branch``` Este comando nos muestra todas las ramas que tengo en el repo (mas adelante estaremos viendo ¿cómo crear ramas?).
* ```git clone <link>``` Con este comando podemos descargar el código fuente desde un repositorio remoto y tenerlo en nuestro pc localmente.
* ```git push``` Este comando lo ejecutamos luego de hacer un **commit**, el siguiente paso es subir los cambios al servidor remoto. En otras palabras envia tus commits al repositorio remoto

### Versionado

En **GIT** tenemos la posibilidad de crear versiones especificas de nuestro repositorio marcando estados importantes, habitualmente es usado el manejo de releases en un proyecto, a través de comando:
* ```git tag```

#### COMO CREARME UNA VERSION DE MI PROYECTO CON GIT

##### CREAMOS UN RELEASE TAG ASI:
* ```git tag``` no regresa nada, lo cual es correcto.
* ```git tag -a v1.0.0 -m "Mi versión"``` creo una version anotada //ya se puede usar.
* ```git push --tags``` lo subimos a git finalmente.

### ¿Cómo crear ramas?
Para crear una rama en git es muy sencillo, para ellos usaremos el siguiente comando:
* ```git branch <nombre_rama>```

### Realizar commit semantico

### Pull Request

### Merge

### Solución de conflictos