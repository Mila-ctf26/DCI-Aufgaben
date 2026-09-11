# Easy ILP: Linux-Shell sicher nutzen

## Aufgabe 1: Orientierung im Terminal

Für die Aufgabe habe ich das Terminal in meiner Linux-VM verwendet.

Mit `pwd` kann ich prüfen, in welchem Verzeichnis ich mich gerade
befinde. Mein Home-Verzeichnis ist:

`/home/liudmyla`

Mit `ls` kann ich die Dateien und Ordner im aktuellen Verzeichnis
anzeigen.

Danach habe ich in den Übungsordner gewechselt und meinen Standort
erneut mit `pwd` kontrolliert.

**Ergebnis:** Ich kann mich im Terminal orientieren und meinen aktuellen
Pfad überprüfen.

## Aufgabe 2: Ordner erstellen

Ich habe den Übungsordner erstellt:

`mkdir shell_training`

Danach sollte ich mit `cd shell_training` in den Ordner wechseln.

Beim ersten Versuch habe ich den Namen falsch geschrieben. Dadurch blieb
ich im Home-Verzeichnis und erstellte `docs`, `tests` und `backup`
zunächst an der falschen Stelle.

Ich habe die Ordner anschließend mit folgendem Befehl in
`shell_training` verschoben:

`mv docs tests backup shell_training/`

Danach zeigte `ls` im richtigen Ordner:

-   `backup`
-   `docs`
-   `tests`

Die fertige Struktur lautet:

shell_training/ - backup/ - docs/ - tests/

## Aufgabe 3: Dateien erstellen und anzeigen

Ich habe die Datei `notizen.txt` erstellt und Text hineingeschrieben:

`echo "Meine ersten Shell-Notizen" > notizen.txt`

Danach habe ich den Inhalt angezeigt:

`cat notizen.txt`

Ausgabe:

`Meine ersten Shell-Notizen`

Die zweite Datei habe ich mit folgendem Befehl erstellt:

`touch todo.txt`

Mit `ls` konnte ich prüfen, dass beide Dateien vorhanden waren.

## Aufgabe 4: Dateien kopieren und verschieben

Ich habe `notizen.txt` in den Ordner `backup` kopiert:

`cp notizen.txt backup/`

Die Kontrolle mit:

`ls backup`

zeigte:

`notizen.txt`

Danach habe ich `todo.txt` in den Ordner `docs` verschoben:

`mv todo.txt docs/`

Die Kontrolle mit:

`ls docs`

zeigte:

`todo.txt`

### Unterschied zwischen `cp` und `mv`

`cp` kopiert eine Datei. Das Original bleibt am ursprünglichen Ort
erhalten und eine Kopie wird erstellt.

`mv` verschiebt eine Datei an einen anderen Ort. Der ursprüngliche
Speicherort wird dabei geändert.

## Aufgabe 5: Vorsichtig aufräumen

Zuerst habe ich eine Testdatei erstellt:

`touch test_loeschen.txt`

Vor dem Löschen habe ich mit `ls` geprüft, ob die Datei vorhanden ist
und ob der Dateiname stimmt.

Danach habe ich nur diese Testdatei gelöscht:

`rm test_loeschen.txt`

Mit einem weiteren `ls` habe ich kontrolliert, dass `test_loeschen.txt`
nicht mehr vorhanden ist. Die anderen Dateien und Ordner blieben
erhalten.

### Sicherheitsregel für `rm`

Vor dem Löschen immer den Dateinamen und den aktuellen Pfad genau
prüfen. Mit `rm` gelöschte Dateien werden normalerweise nicht einfach in
den Papierkorb verschoben.

## Extra 1: Pfadtraining

Ich bin zwischen mehreren Ordnern gewechselt und habe jedes Mal mit
`pwd` meinen Standort geprüft.

### Drei geprüfte Pfade

1.  `/home/liudmyla/shell_training/docs`
2.  `/home/liudmyla/shell_training/backup`
3.  `/home/liudmyla/shell_training`

Verwendete Befehle waren unter anderem:

`cd docs`

`cd ../backup`

`cd ..`

`pwd`

Dabei habe ich gelernt, dass `..` für das übergeordnete Verzeichnis
steht.

## Extra 2: Fehler finden

Während der Aufgabe ist tatsächlich ein Tippfehler passiert.

Ich wollte in den Ordner `shell_training` wechseln, schrieb den
Ordnernamen aber zunächst falsch.

Linux meldete:

`Datei oder Verzeichnis nicht gefunden`

Dadurch wusste ich, dass der angegebene Pfad bzw. Ordnername nicht
stimmt.

Ich habe anschließend den richtigen Ordnernamen verwendet und die
versehentlich im Home-Verzeichnis erstellten Ordner mit `mv` an die
richtige Stelle verschoben.

**Ergebnis:** Ich habe gelernt, Fehlermeldungen zu lesen und zuerst
Schreibweise und Pfad zu kontrollieren.

## Befehlsliste

`pwd` -- zeigt den vollständigen Pfad des aktuellen Verzeichnisses.

`ls` -- zeigt Dateien und Ordner im aktuellen Verzeichnis.

`cd ORDNER` -- wechselt in einen Ordner.

`cd ..` -- wechselt eine Ebene nach oben.

`mkdir ORDNER` -- erstellt einen neuen Ordner.

`touch DATEI` -- erstellt eine leere Datei.

`echo "TEXT" > DATEI` -- schreibt Text in eine Datei.

`cat DATEI` -- zeigt den Inhalt einer Textdatei im Terminal.

`cp QUELLE ZIEL` -- kopiert eine Datei oder einen Ordner an ein Ziel.

`mv QUELLE ZIEL` -- verschiebt oder benennt Dateien bzw. Ordner um.

`rm DATEI` -- löscht eine Datei. Dieser Befehl muss vorsichtig verwendet
werden.

## Reflexion

### Welcher Befehl hilft dir am meisten?

`pwd` hilft mir besonders, weil ich jederzeit prüfen kann, in welchem
Verzeichnis ich mich gerade befinde. Das ist wichtig, bevor ich Dateien
verschiebe oder lösche.

### Wann musst du besonders vorsichtig sein?

Besonders vorsichtig muss ich bei `rm` sein. Vor dem Löschen sollte ich
immer den Dateinamen und meinen aktuellen Pfad kontrollieren. Auch bei
`mv` muss ich darauf achten, dass Quelle und Ziel richtig angegeben
sind.

### Was bedeutet ein Pfad?

Ein Pfad beschreibt die Position einer Datei oder eines Ordners im
Dateisystem. Zum Beispiel zeigt `/home/liudmyla/shell_training/docs`, wo
sich der Ordner `docs` befindet.

## Fazit

Ich habe im Linux-Terminal eine eigene Ordnerstruktur erstellt und mit
Dateien gearbeitet. Dabei habe ich die Befehle `pwd`, `ls`, `cd`,
`mkdir`, `touch`, `echo`, `cat`, `cp`, `mv` und `rm` praktisch
verwendet.

Außerdem habe ich einen echten Eingabefehler erkannt und korrigiert.
Besonders wichtig war für mich die Erkenntnis, vor Dateioperationen
immer den aktuellen Pfad und die Namen der Dateien oder Ordner zu
kontrollieren.
