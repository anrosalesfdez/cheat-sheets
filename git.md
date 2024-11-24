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

