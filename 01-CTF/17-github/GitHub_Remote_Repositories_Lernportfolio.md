# Individuelle Learning Phase: GitHub-Remote-Repositories und Synchronisation in der Praxis

## Aufgabe 1 -- GitHub-Repository erstellen

Ich habe auf GitHub ein neues Repository erstellt.

**Repository:** `coretech-github-praxis`

**Beschreibung:**\
GitHub-Übungsrepository für Remote-Repositories und Synchronisation.

Das Repository wurde zunächst leer erstellt. Danach habe ich die
Bereiche **Code**, **Issues**, **Pull requests** und **Settings**
angesehen.

**Remote-Adresse:**

`git@github.com:Mila-ctf26/coretech-github-praxis.git`

## Aufgabe 2 -- Lokales Repository vorbereiten und verbinden

Ich habe ein lokales Repository erstellt:

`~/github-remote-praxis`

Darin habe ich folgende Dateien erstellt:

-   `README.md`
-   `.gitignore`
-   `notizen.txt`

Danach habe ich das Repository initialisiert:

`git init`

Die Dateien wurden zur Stage hinzugefügt:

`git add .`

**Erster Commit:**

`git commit -m "Erste Projektdateien"`

Die lokale Branch wurde auf `main` umbenannt.

Danach habe ich das lokale Repository mit GitHub verbunden.

Zur Kontrolle habe ich verwendet:

`git remote -v`

Dabei wurde `origin` für Fetch und Push angezeigt.

## Aufgabe 3 -- README, .gitignore und erster Push

Die README wurde um folgende Informationen ergänzt:

-   Projektname
-   Kurzbeschreibung
-   Inhalt des Repositories
-   Zweck

In `.gitignore` habe ich folgende Regeln eingetragen:

``` text
*.log
.vscode/
```

Danach:

``` bash
git add README.md .gitignore
git commit -m "README und Gitignore ergänzen"
```

Vor dem Push habe ich die aktuelle Branch geprüft.

Anschließend:

`git push -u origin main`

Die SSH-Verbindung zu GitHub wurde verwendet.

Der Push war erfolgreich und die Dateien sowie die Commits waren
anschließend auf GitHub sichtbar.

## Aufgabe 4 -- Klonen und Synchronisieren

Ich habe das GitHub-Repository in eine zweite lokale Arbeitskopie
geklont:

`git clone git@github.com:Mila-ctf26/coretech-github-praxis.git github-remote-praxis-clone`

Danach habe ich die Dateien und die Commit-Historie überprüft:

``` bash
ls -la
git log --oneline
```

Im ursprünglichen Repository habe ich `README.md` und `notizen.txt`
geändert.

Danach habe ich die Änderungen committed und mit GitHub synchronisiert:

``` bash
git add README.md notizen.txt
git commit -m "Synchronisation vorbereiten"
git push
```

Im geklonten Repository habe ich anschließend ausgeführt:

`git pull`

Die Änderungen wurden erfolgreich übernommen.

Mit `git log --oneline` und dem Inhalt von `notizen.txt` konnte ich
kontrollieren, dass die Änderungen lokal angekommen waren.

## Aufgabe 5 -- Branch, Pull Request und Merge-Konflikt

Ich habe eine neue Branch erstellt:

`git switch -c feature-readme-update`

In dieser Branch habe ich eine Zeile der README geändert.

Danach:

``` bash
git add README.md
git commit -m "README im Feature-Branch aktualisieren"
git push -u origin feature-readme-update
```

Auf GitHub habe ich einen Pull Request von `feature-readme-update` nach
`main` erstellt.

Danach bin ich wieder zu `main` gewechselt:

`git switch main`

In `main` habe ich dieselbe Zeile der README anders geändert.

Danach:

``` bash
git add README.md
git commit -m "README in Main aktualisieren"
git push
```

GitHub zeigte anschließend:

> This branch has conflicts that must be resolved

**Betroffene Datei:** `README.md`

Der Merge-Konflikt entstand, weil dieselbe Zeile in `main` und
`feature-readme-update` unterschiedlich geändert wurde.

## Erweiterung 1 -- README verbessern

Die README wurde zusätzlich um folgende Bereiche erweitert:

-   Voraussetzungen
-   Projektstruktur
-   Nächste Schritte

**Commit:**

`git commit -m "README um weitere Abschnitte ergänzen"`

Danach wurde die Änderung mit `git push` an GitHub übertragen.

## Erweiterung 2 -- Änderung direkt auf GitHub

Ich habe `notizen.txt` direkt auf GitHub bearbeitet und dort einen
Commit erstellt.

Danach habe ich lokal geprüft, dass ich mich in `main` befinde, und
ausgeführt:

`git pull`

Die Änderung von GitHub wurde erfolgreich in das lokale Repository
übernommen.

## Erweiterung 3 -- Workflow-Notizen

Ich habe die Datei `workflow-notizen.md` erstellt.

Darin habe ich folgende Themen dokumentiert:

-   Remote-Verbindung
-   Push
-   Pull
-   Merge-Konflikt
-   Commit und Push

Danach:

``` bash
git add workflow-notizen.md
git commit -m "Workflow-Notizen hinzufügen"
git push
```

# Reflexion

## 1. Woran erkennst du, dass dein lokales Repository mit einem Remote-Repository verbunden ist?

Mit `git remote -v` kann ich prüfen, ob mein lokales Repository mit
einem Remote-Repository verbunden ist. Dort sehe ich den Namen `origin`
und die Remote-Adresse für Fetch und Push.

## 2. Woran erkennst du, dass ein Push erfolgreich war?

Ein erfolgreicher Push wird im Terminal angezeigt. Zum Beispiel zeigt
`main -> main`, dass die lokalen Commits erfolgreich an GitHub
übertragen wurden. Zusätzlich kann ich die Änderungen im
GitHub-Repository sehen.

## 3. Woran erkennst du, dass Änderungen vom Remote-Repository lokal angekommen sind?

Mit `git pull` kann ich Änderungen vom Remote-Repository herunterladen.
Im Terminal sehe ich, welche Dateien aktualisiert wurden. Danach kann
ich mit `git log --oneline` oder direkt in den Dateien prüfen, ob die
Änderungen lokal angekommen sind.

## 4. Wofür ist ein Pull Request praktisch, auch wenn du allein arbeitest?

Ein Pull Request ist auch bei alleiniger Arbeit praktisch, weil ich
Änderungen vor dem Zusammenführen überprüfen und vergleichen kann.
Außerdem sehe ich, welche Dateien geändert wurden und ob Merge-Konflikte
vorhanden sind.

## 5. Was verursacht einen einfachen Merge-Konflikt?

Ein einfacher Merge-Konflikt kann entstehen, wenn dieselbe Zeile einer
Datei in zwei verschiedenen Branches unterschiedlich geändert wurde. Git
kann dann nicht automatisch entscheiden, welche Version übernommen
werden soll.

## 6. Welche Informationen in einer README helfen dir am meisten?

Am hilfreichsten finde ich eine kurze Projektbeschreibung, den Zweck des
Projekts, die Voraussetzungen, die Projektstruktur und die nächsten
Schritte. Dadurch kann ich schnell verstehen, worum es im Projekt geht
und wie ich damit arbeiten kann.

# Abschlusskontrolle

Am Ende habe ich `git status` ausgeführt.

**Ergebnis:**

``` text
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

Damit sind die lokalen Änderungen committed und `main` ist mit
`origin/main` synchronisiert.

Der Pull Request mit dem Merge-Konflikt wurde für die Übung bewusst
offen gelassen.
