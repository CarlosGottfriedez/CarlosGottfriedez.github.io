# Git-Funktionen



`q  :q  Q  :Q  ZZ     Exit.


```
cd my-project
git init
```

```
git add project.tex
```

```
git add figures/     # Adds the figures directory
git add *.tex        # Adds all .tex files in the current directory
git add .            # Adds all of the files (. is the current directory)

```

```
git commit -m "My first commit"
```

You need to run git add whenever you change a file, not just at the beginning. This tells git that it should include these changes in the next snapshot. Alternatively you can pass the -a option to git commit to tell it to commit all changes to files that it is monitoring:

```
git commit -a -m "My second commit"
```

```
git log
```

```
git show
```

```
git checkout f69606d7e24ad45b31bb6eb4b38192bd07f274fc # Frühere verison mit dieser Nummer wird aufgerufen.
```

Another common situation is you decide that you want to undo only one set of changes from a while ago. Perhaps you’ve edited the document in three steps: 1) Adding an abstract, 2) Updating your acknowledgements, 3) Adding in a figure. At each step you’ve created a new version in git, but now you decide that you didn’t really want to update you acknowledgements. Unfortunately this is sandwiched between other changes so a simple rollback like before won’t do. Fear not, because git is clever enough to do what you want, with the revert command:

```
git revert f69606d7e24ad45b31bb6eb4b38192bd07f274fc
```

```
git push origin master
```

The other possiblity is you want to download changes made by someone else. This is a process which git calls ‘pulling’. To do this, simply run
```
git pull origin master
```

```
git status
```
