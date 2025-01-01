
# Git

in Bearbeitung

----

## Git Konto wechseln und commiten

```` bash
git init

touch .gitignore

git add .
git commit -m "Initial commit"

git branch -M main 

git remote add origin https://github.com/ugurat/git.git

git push -u origin main
````

Falls Fehler:

```` bash
PASSWORT LÖSCHEN und ERNEUT ANMELDEN

Gehe zu "Windows-Anmeldeinformationen": 
Unter Windows-Anmeldeinformationen "gespeicherte Zugangsdaten für Webseiten und Anwendungen" finden.

Suche nach gespeicherten GitHub-Einträgen: 
git:https://github.com oder Ähnliches.

Eintrag löschen und erneut versuchen: 

git push -u origin main
````
  
Aktualisiert

```` bash
git add .
git commit -m "aktualisiert"
git push -u origin main
````

Überschreiben

```` bash

git init

git add .
git commit -m "Initial commit"

git branch -M main 

git remote add origin https://github.com/ugurat/git.git


git push -u origin main --force

````

Mit dem Parameter `--force` wird Git-Repo überschrieben. 

----


## Entwickler
- **Name**: Ugur CIGDEM
- **E-Mail**: [ugurat@gmail.com](mailto:ugurat@gmail.com)

---

## Markdown-Datei (.md)

---

