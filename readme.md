- **¿Qué comando utilizaste en el paso 11? ¿Por qué?**

	> Hacemos un "git reset --hard HEAD&#126;1" (manteniéndonos donde estamos, en la rama 'styled')
	> Porque (1) lo que queremos es "deshacer" el último cambio y eso se consigue reposicionando el HEAD en el Nodo justo anterior al Nodo en el que estamos ('HEAD&#126;1') y (2) porque lo que también queremos es recuperar en el WORKING COPY la versión del GIT-NUESTRO.MD que teníamos antes (--hard).

- **¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**

	> En el paso anterior hemos creado un 'Nodo Inalcanzable' (el que contiene los cambios sobre el archivo GIT-NUESTRO.MD). Lo que vamos a hacer en este paso es utilizar "git merge <ID del Nodo Inalcanzable>" (hay que hacer un "git reflog" para localizar ese ID)
	> Este comando nos va a permitir reabsorber dentro de la Rama 'styled' los cambios realizados en el 'Nodo Inalcanzable' y se hará un fast-forward... con lo cual con 1 sólo comando nos volveremos a encontrar en la misma situación que antes de ejecutar el "git reset --hard HEAD~1"

- **El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**

	> No causa ningún conflicto, todo lo contrario, tras el "git merge master" (estando posicionados en la Rama 'styled') nos contesta: "Already up to date".
	> Esto es normal porque el Nodo de la Rama 'master' es padre del Nodo de la Rama 'styled' en el que estamos posicionados. Todos los cambios que intentemos incorporar de esta forma estánya incorporados en la Rama 'styled'.

- **El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?**

	> Sí, causa conflicto entre las modificaciones relizadas en cada una de las Ramas, sobre el archivo GIT-NUESTRO.MD
	> Esto se debe a que las modificaciones han sido realizadas sobre las mismas líneas del archivo y GIT 'no sabe' con qué cambios se puede quedar

- **El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**

	> No, ningún conflico. GIT realizó un merge automáticamente
	> Esto es debido a que después del último COMMIT sobre el archivo GIT-NUESTRO.MD a partir de la Rama 'styled', no se ha realizado ningún cambio ni COMMIT sobre el mismo achivo a partir de la Rama 'master'

- **¿Qué comando o comandos utilizaste en el paso 25?**

	> Para poder sacar el diagrama de Nodos de GIT he utilizado "git log --graph --pretty=oneline"

- **El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**

	> Si no pusiéramos la directriz '--no-ff' al comando "git merge title", el 'merge' sería de tipo fast forward
	> Porque el Nodo de la Rama'title' está justo a '1 paso más' del Nodo de la Rama 'master' sobre el que estamos

- **¿Qué comando o comandos utilizaste en el paso 27?**

	> Comando: "git reset HEAD~1"

- **¿Qué comando o comandos utilizaste en el paso 28?**

	> Comando: "git checkout -- git-nuestro.md"

- **¿Qué comando o comandos utilizaste en el paso 29?**

	> Comando: "git branch -D title"

- **¿Qué comando o comandos utilizaste en el paso 30?**

	> Comando: "git merge HEAD@{1}"

- **¿Qué comando o comandos usaste en el paso 32?**

	> Comandos:
		1. "git reflog" para localizar el ID del Nodo inicial
		2. "git checkout <ID del Nodo Inicial>"

- **¿Qué comando o comandos usaste en el punto 33?**

	> Comando: "git checkout master"

