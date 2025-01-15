
# Git Befehle

---- 

```` text
git init
# Dieser Befehl erstellt ein neues Git-Repository im aktuellen Verzeichnis.

git add .
# Dieser Befehl fügt alle Dateien zum Staging-Bereich hinzu.
# Mit "." werden alle Dateien im aktuellen Verzeichnis einbezogen.

git commit -m "Projekstart"
# Dieser Befehl committed die Änderungen und fügt eine Nachricht hinzu.
# Nachricht: "Projektstart".

git remote add origin <repository_url>
# Dieser Befehl verbindet das lokale Repository mit dem Remote-Repository.
# Ersetzen Sie <repository_url> durch die URL des Online-Repository.
# Beispiel: git remote add origin https://github.com/benutzername/projektname.git

git branch -M main
# Dieser Befehl ändert den Standardzweignamen in "main".
# Auf GitHub ist der Standardzweig normalerweise auf "main" eingestellt.

git push -u origin main
# Dieser Befehl pusht alle Commits in den "main"-Zweig.
# Der Parameter "-u" legt den "main"-Zweig als Standardzweig fest.
````

---

```` text
# 1. Den letzten Commit zurücksetzen, aber die Änderungen im Arbeitsbereich belassen
git reset --mixed HEAD~1
# Dieser Befehl hebt den letzten Commit auf und verschiebt die Änderungen in den Arbeitsbereich.

# 2. Den ersten Commit pushen
git push origin <branch_name>
# Hier ist <branch_name> der Name des Zweigs, an dem Sie arbeiten (z.B. main oder master).
# Dieser Vorgang sendet Ihren ersten Commit zum Remote-Repository.

# 3. Um den letzten Commit neu zu erstellen, fügen Sie die Änderungen zum Staging-Bereich hinzu
git add .
# Fügt alle Änderungen zum Staging-Bereich hinzu.

# 4. Den letzten Commit neu erstellen
git commit -m "Beschreibung des letzten Commit"
# Erstellt den letzten Commit neu.

# 5. Den letzten Commit pushen
git push origin <branch_name>
# Sendet den neu erstellten letzten Commit zum Remote-Repository.
```` 

----

```` text
# 1. Den Commit-Verlauf überprüfen
git log --oneline
# Dieser Befehl listet den Commit-Verlauf kurz und bündig auf.
# Beispiel:
# a1b2c3d Erste Commit-Beschreibung
# e4f5g6h Zweite Commit-Beschreibung
# Der oberste Commit ist der zuletzt durchgeführte Commit.

# 2. Um den letzten Commit zurückzusetzen
git reset --mixed HEAD~1
# Dieser Befehl hebt den letzten Commit auf und verschiebt die Änderungen in den Arbeitsbereich.

# 3. Um einen bestimmten Commit zurückzusetzen (unter Verwendung des Hashes)
git reset --mixed <commit_hash>
# Dieser Befehl hebt alle Commits bis zum angegebenen Hash auf
# und verschiebt die Änderungen in den Arbeitsbereich.
# Beispiel: git reset --mixed e4f5g6h

# 4. Den Commit-Verlauf erneut überprüfen
git log --oneline
# Dieser Befehl listet den Commit-Verlauf erneut auf, um die durchgeführte Aktion zu überprüfen.
# Wenn der zurückgesetzte Commit nicht mehr in der Liste erscheint, war die Aktion erfolgreich.
```` 

----

```` text
# 1. Die Details eines bestimmten Commits anzeigen
git show <commit_hash>
# Dieser Befehl zeigt die Commit-Nachricht, den Benutzer, das Datum und die vorgenommenen Änderungen (zeilenweise) an.

# 2. Die in einem Commit geänderten Dateien auflisten
git diff-tree --no-commit-id --name-only -r <commit_hash>
# Dieser Befehl listet nur die Namen der in einem Commit geänderten Dateien auf.

# 3. Den Inhalt einer bestimmten Datei in einem Commit anzeigen
git show <commit_hash>:<datei_pfad>
# Dieser Befehl zeigt den Inhalt einer bestimmten Datei im ausgewählten Commit an.
# Beispiel: git show e4f5g6h:src/index.html

# 4. Die Unterschiede zwischen zwei Commits anzeigen
git diff <commit1_hash> <commit2_hash>
# Dieser Befehl zeigt die Unterschiede zwischen zwei Commits zeilenweise an.
# Beispiel: git diff a1b2c3d e4f5g6h
```` 

----
