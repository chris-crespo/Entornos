# Git

## ¿Qué es?
Git es un sistema de control de versiones que nos permite llevar a cabo un seguimiento de la evolución 
de un projecto. Además de crear repositorios locales, también nos permite compartirlo en repositorios
remotos.

## Repositorio Local y Remoto
Un **repositorio local** es el repositorio almacenado en nuestros ordenadores. Se crean mediante `git init`, 
o tras clonar un repositorio remoto mediante `git clone`. Este es el repositorio donde realizamos las cambios que 
después publicaremos (o no) en un repositorio remoto.

Un **repositorio remoto** es un repositorio que se almacena en un servidor externo, como github o gitlab. Permite
publicar el contenido de nuestro repositorio local y que múltiples personas colaboren en un mismo proyecto.

## Index
El **index** es el archivo que usa git para saber qué archivos debe seguir y qué archivos debe añadir a un *commit*.

## Comandos
- `git init` Inicializa git, creando un repositorio en el directorio actual.
- `git clone` Clona un repositorio remoto como local.
- `git remote add` Añade un repositorio remoto al que puede ser referido mediante el nombre indicado.
- `git status` Muestra el estado de la rama actual: los *commits* realizados pero no empujados, los archivos añadidos,
los archivos con cambios no añadidos pero que git sigue, y los archivos que git no sigue.
- `git add` Añade los archivos indicados al índice, preparándolo para posteriormente realizar el *commit*.
- `git commit` Crea un nuevo *commit* con el contenido del índice y el mensaje pasado mediante `-m msg`.
	- `git commit -a` Crea un nuevo *commit* tras añadir al índice los cambios realizados a los archivos que git conoce.
- `git push` Empuja los *commits* locales a la rama de un repositorio remoto.
	- `git push -u` Indica a qué rama del repositorio remoto debe empujar los *commits*. Solo es necesario realizarlo
una vez por rama.
- `git pull` Actualiza la rama actual con los nuevos *commits* de la rama remota.
- `git branch` Muestra las ramas del repositorio. Además, marca con `*` la rama en la que nos encontramos.
	- `git branch *rama*` Crea una rama.
	- `git branch -a` Muestra todas las ramas del repositorio local y remoto.
	- `git branch -d` Elimina una rama.
	- `git branch -m` Mueve/renombra una rama a otra.
- `git checkout` Nos mueve al rama indicada.
	- `git checkout -b` Crea la rama antes de movernos a ella.
- `git diff` Muestra las diferencias entre el contenido actual de un archivo y el contenido que ha sido añadido
previamente.
- `git log` Muestra una lista detallada de los *commits* realizados.
	- `git log --oneline` Muestra una lista compacta de los *commits* realizados. 
