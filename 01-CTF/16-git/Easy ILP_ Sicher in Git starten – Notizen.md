# Easy ILP: Sicher in Git starten

## Aufgabe 1: Git prüfen

Git wurde im Terminal mit folgendem Befehl geprüft:

`git --version`

**Ergebnis:** Git ist installiert.

---

## Aufgabe 2: Git konfigurieren

Der Git-Name wurde geprüft mit:

`git config --global user.name`

Die Git-E-Mail wurde geprüft mit:

`git config --global user.email`

Meine Git-Daten:

- Git-Name: `liudmyla`
- Git-E-Mail: `lvasylchuk@web.de`

Die Konfiguration wurde mit folgenden Befehlen gesetzt:

`git config --global user.name "liudmyla"`

`git config --global user.email "lvasylchuk@web.de"`

**Ergebnis:** Git kennt meinen Namen und meine E-Mail-Adresse.

---

## Aufgabe 3: Repository erstellen

Ein neuer Ordner wurde erstellt:

`mkdir git_start`

Danach wurde in den Ordner gewechselt:

`cd git_start`

Das Repository wurde initialisiert:

`git init`

Der Status wurde geprüft:

`git status`

**Ergebnis:** Der Ordner `git_start` ist jetzt ein lokales Git-Repository.

---

## Aufgabe 4: Erste Datei versionieren

Eine Datei `README.md` wurde erstellt und mit drei kurzen Sätzen gefüllt.

Danach wurde der Status geprüft:

`git status`

Die Datei wurde zur Stage hinzugefügt:

`git add README.md`

Danach wurde der Status erneut geprüft:

`git status`

Der erste Commit wurde erstellt:

`git commit -m "Erster Commit"`

**Ergebnis:** Die Datei wurde erfolgreich versioniert und der erste Commit wurde erstellt.

---

## Aufgabe 5: Git-Ablauf erklären

**Arbeitsordner:**  
Der Arbeitsordner ist der Bereich, in dem Dateien erstellt und geändert werden.

**Stage:**  
Die Stage enthält die Änderungen, die für den nächsten Commit vorbereitet wurden.

**Commit:**  
Ein Commit speichert einen festen Stand der Änderungen im Repository.

### Reihenfolge

**ändern → `git add` → `git commit`**

---

## Extra 1: Konfiguration ansehen

Die Git-Konfiguration wurde angezeigt mit:

`git config --list`

Dort sind zum Beispiel folgende Einstellungen sichtbar:

1. `user.name=liudmyla`
2. `user.email=lvasylchuk@web.de`
3. weitere Git-Einstellungen

Git kann Einstellungen global für den Benutzer oder lokal für ein bestimmtes Repository speichern.

---

## Extra 2: Zweites Repository

Ein zweiter Übungsordner wurde erstellt.

Git wurde dort mit folgendem Befehl initialisiert:

`git init`

Danach wurde eine Datei erstellt, mit `git add` hinzugefügt und mit `git commit` gespeichert.

**Ergebnis:** Ich kann ein neues Git-Repository selbstständig erstellen.

---

# Reflexion

**Was macht `git init`?**  
`git init` erstellt in einem Ordner ein neues lokales Git-Repository.

**Was macht `git add`?**  
`git add` fügt Änderungen zur Stage hinzu und bereitet sie für den nächsten Commit vor.

**Warum sind Commits nützlich?**  
Commits speichern verschiedene Arbeitsstände eines Projekts. Dadurch können Änderungen nachvollzogen und frühere Versionen wiedergefunden werden.

---

## Ergebnis

Ich habe:

- die Git-Installation geprüft
- meinen Git-Namen `liudmyla` geprüft bzw. eingerichtet
- meine Git-E-Mail `lvasylchuk@web.de` geprüft bzw. eingerichtet
- ein lokales Repository erstellt
- eine Datei versioniert
- einen ersten Commit erstellt
- den grundlegenden Git-Ablauf verstanden