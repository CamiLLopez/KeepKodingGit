#### - ¿Qué comando utilizaste en el paso 11? ¿Por qué?
    git reset --hard HEAD~1
Porque necesitabamos perder los cambios del repositorio y haciendo lo hard, sucede esto y nuestro staiging area queda vacio

#### - ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
    git reflog
    git reset 6b3c4e1
Primero git reflog poder detectar el commit al que quiero volver y luego git reset para volver al commit que se había desecho.

    git add git-nuestro.md
    git commit

git add y git commit para volver a tener el "commit" en el working area.

#### - El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
No la rama styled esta "already up to date" porque se creó la rama desde master, se modifico el Git nuestro pero no hubo cambios en las mismas lineas del archivo en master, por lo que no se genera conflicto. 

#### - El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Si causa conflicto porque la rama htmlfy parte de master (que no tiene los cambios de style), luego se hacen modificaciones en htmlify. Si desde styled quiero mergear htmlify ahora si se hicieron cambios sobre las mismas lineas y produce un conflicto. Para evitarlo primero tendría que haber mergeado style en htmlify y luego hacer los cambios en el archivo.

#### El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No causa conflicto. Es lo mismo que anteriormente, no hubo cambios en master por lo que aún cuando el archivo cambio, desde master no fueron modificadas esas lineas, por lo que no hay conflicto.
Es decir, master no tiene un commit que no exista previamente en styled, por lo que no genera conflicto.
 
#### - ¿Qué comando o comandos utilizaste en el paso 25?
    git log --graph

#### - El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
Si porque title fue creado desde master y no existen commits en master, por lo que no hubiese sido necesario generar un commit extra para traer el contenido del commit o commits de title. 

#### - ¿Qué comando o comandos utilizaste en el paso 27?
    git reset HEAD~1

#### - ¿Qué comando o comandos utilizaste en el paso 28?
    git restore git-nuestro.md

#### - ¿Qué comando o comandos utilizaste en el paso 29?
    git branch -D title

#### - ¿Qué comando o comandos utilizaste en el paso 30?
    git reflog
    git checkout 844475f
    git status
    git restore git-nuestro.md
    cat git-nuestro.md
    git checkout master
    git reset 844475f

#### - ¿Qué comando o comandos usaste en el paso 32?
    git reflog
    git reset ccccf14
    git restore git-nuestro.md

#### - ¿Qué comando o comandos usaste en el punto 33? 
    git reflog
    git reset 844475f
    git restore git-nuestro.md
