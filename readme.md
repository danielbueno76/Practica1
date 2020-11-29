- ¿Qué comando utilizaste en el paso 11? ¿Por qué? 
Utilicé el comando git reset --hard HEAD~1. Porque este comando permite mover el puntero head que apunta a la rama styled(en este caso) al commit padre y con la opción --head modificamos el working copy.
- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué? 
Utilicé los comando git reflog y git reset --hard <id_commit>. Con el comando git reflog pude ver el id del commit al que estabamos antes de desahecerlo. Luego con git reset --hard <id_commit> pude mover el puntero head que apuntaba a nuestra rama actual al commit donde estabamos.
- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
No causó ningún conflicto, ya que se realizó un merge fast-forward ya que es la opción por defecto. Además de que este merge permitió realizarlo de manera fast-forward por la configuracion de las ramas(No se dejaba ningún commit "inaccesible", es decir, teniendo que acceder al commit en modo detached head).
- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Si causó algún conflicto. Se realizó un merge sin fast-forward debido a la configuración de ramas, ya que se dejaba algún commit en modo detached head si no. Este merge creó un nuevo commít en el que dió conflicto debido a que en la mismas líneas del fichero cada rama había escrito un contenido diferentes.
- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No causó ningún conflicto, ya que se realizó un merge fast-forward ya que es la opción por defecto. Además de que este merge permitió realizarlo de manera fast-forward por la configuracion de las ramas
- ¿Qué comando o comandos utilizaste en el paso 25?
Utilicé el comando git log --graph --oneline para dibujar el diagrama.
- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
Si podría ser fast-forward ya que la configuración de ramas lo permite(No se dejaba ningún commit "inaccesible", es decir, teniendo que acceder al commit en modo detached head).
- ¿Qué comando o comandos utilizaste en el paso 27?
Utilicé git reset HEAD~1 para situarme en el commit previo al merge sin cambiar mi working copy.
- ¿Qué comando o comandos utilizaste en el paso 28?
Utilicé git restore git-nuestro.md para descartar los cambios del fichero.
- ¿Qué comando o comandos utilizaste en el paso 29?
Utilicé git branch -D title para borrar la rama ya que dejaba un commit inaccesible(Solo se puede acceder en modo detached head)
- ¿Qué comando o comandos utilizaste en el paso 30?
Primero averigué el id del commit tras haber realizado el merge no fast-forward con git reflog. Luego me situé en la rama master con git checkout master. Finalmente me situé en el commit creado con el merge no fast-forward con git reset --hard commit ya que HEAD apuntaba a master y de esta manera conseguía que master apuntase al commit deseado.
- ¿Qué comando o comandos usaste en el paso 32?
Primero usé el comando git log para ver el commit inicial ya que al estar situado en la rama master y como cada commit ve a su commit padre pude realizar un git reset --hard id_commit_inicial.
- ¿Qué comando o comandos usaste en el punto 33?
Primero utilicé git reflog para ver el id del último commit, el cual añadió el título al poema. Entonces realicé git reset --hard id_commit_final para situarme en el.