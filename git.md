# GIT

git init: creates a new local repository in the current directory

git clone: copies an existing remote repository to your local machine

git status: shows the state of your working directory and staging área

git add: add changes in your working directory to he staging área, which is a temporary área where you can prepare your next commit

git commit -m "mensaje": records the changes in the staging área as a new snapshot in he local repository, along with  message describing the changes

git commit --allow-empty -m "Listo para sincronizar"

git checkout: switches your working directory to a different Branch or commit, discarding any uncommitted changes
git checkout -b nombre1-apellido1/rb

Git branch

git merge: combines the changes from one Branch into another Branch, creating a new commit if there are no conflicts

git diff: shows the differences two commits, branches, flies, or the working directory and the staging área

git log: shows the history of commits in the current brach, along with their messages, authors and dates

git log -1 --oneline

Git log --oneline --all

Git remote -v

git push -u origin main

Git fetch (solo trae la info)

Git pull (hace fetch + merge) puede haber errores

## Deshacer commits en local

git reset --soft HEAD~2

## Git fork manual

1. Crear un nuevo repositorio en GitHub vacío: no marques opciones como incluir un README, .gitignore o licencia.

2. Clonar el repositorio original a tu local:

3. En el repo local configura upstream en lugar de origin:
    
    Renombra el remoto origin (que apunta al repositorio original) como upstream:

    git remote rename origin upstream
    
    Comprueba que el cambio se hizo correctamente:

    git remote -v

4. Añade en el repo local otro repositorio remoto (origin):

    git remote add origin https://github.com/<tu-usuario>/t5-numpy-mnist-nombre1-apellido1.git

    Vuelve a verificar los remotos:

    git remote -v

5. Subir el contenido al nuevo repositorio (origin):
    
    git push -u origin master

    Este comando establece la rama master como la rama por defecto para futuros pushes.

6. A futuro, traer cambios del repositorio original (upstream):

    git pull upstream master
    