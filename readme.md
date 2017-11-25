- **�Qu� comando utilizaste en el paso 11? �Por qu�?**

	> Hacemos un "git reset --hard HEAD~1" (manteni�ndonos donde estamos, en la rama 'styled')
	> Porque (1) lo que queremos es "deshacer" el �ltimo cambio y eso se consigue reposicionando el HEAD en el Nodo justo anterior al Nodo en el que estamos ('HEAD~1') y (2) porque lo que tambi�n queremos es recuperar en el WORKING COPY la versi�n del GIT-NUESTRO.MD que ten�amos antes (--hard).

- **�Qu� comando o comandos utilizaste en el paso 12? �Por qu�?**

	> En el paso anterior hemos creado un 'Nodo Inalcanzable' (el que contiene los cambios sobre el archivo GIT-NUESTRO.MD). Lo que vamos a hacer en este paso es utilizar "git merge <ID del Nodo Inalcanzable>" (hay que hacer un "git reflog" para localizar ese ID)
	> Este comando nos va a permitir reabsorber dentro de la Rama 'styled' los cambios realizados en el 'Nodo Inalcanzable' y se har� un fast-forward... con lo cual con 1 s�lo comando nos volveremos a encontrar en la misma situaci�n que antes de ejecutar el "git reset --hard HEAD~1"

- **El merge del paso 13, �Caus� alg�n conflicto? �Por qu�?**

	> No causa ning�n conflicto, todo lo contrario, tras el "git merge master" (estando posicionados en la Rama 'styled') nos contesta: "Already up to date".
	> Esto es normal porque el Nodo de la Rama 'master' es padre del Nodo de la Rama 'styled' en el que estamos posicionados. Todos los cambios que intentemos incorporar de esta forma est�nya incorporados en la Rama 'styled'.

- **El merge del paso 19, �Caus� alg�n conflicto? �Por qu�?**

	> S�, causa conflicto entre las modificaciones relizadas en cada una de las Ramas, sobre el archivo GIT-NUESTRO.MD
	> Esto se debe a que las modificaciones han sido realizadas sobre las mismas l�neas del archivo y GIT 'no sabe' con qu� cambios se puede quedar

- **El merge del paso 21, �Caus� alg�n conflicto? �Por qu�?**

	> No, ning�n conflico. GIT realiz� un merge autom�ticamente
	> Esto es debido a que despu�s del �ltimo COMMIT sobre el archivo GIT-NUESTRO.MD a partir de la Rama 'styled', no se ha realizado ning�n cambio ni COMMIT sobre el mismo achivo a partir de la Rama 'master'

- **�Qu� comando o comandos utilizaste en el paso 25?**

	> Para poder sacar el diagrama de Nodos de GIT he utilizado "git log --graph --pretty=oneline"

- **El merge del paso 26, �Podr�a ser fast forward? �Por qu�?**

	> Si no pusi�ramos la directriz '--no-ff' al comando "git merge title", el 'merge' ser�a de tipo fast forward
	> Porque el Nodo de la Rama'title' est� justo a '1 paso m�s' del Nodo de la Rama 'master' sobre el que estamos

- **�Qu� comando o comandos utilizaste en el paso 27?**

	> Comando: "git reset HEAD~1"

- **�Qu� comando o comandos utilizaste en el paso 28?**

	> Comando: "git checkout -- git-nuestro.md"

- **�Qu� comando o comandos utilizaste en el paso 29?**

	> Comando: "git branch -D title"

- **�Qu� comando o comandos utilizaste en el paso 30?**

	> Comando: "git merge HEAD@{1}"

- **�Qu� comando o comandos usaste en el paso 32?**

	> Comandos:
		1. "git reflog" para localizar el ID del Nodo inicial
		2. "git checkout <ID del Nodo Inicial>"

- **�Qu� comando o comandos usaste en el punto 33?**

	> Comando: "git checkout master"

