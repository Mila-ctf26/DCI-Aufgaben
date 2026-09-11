# Linux-Alltagskarte -- Rechte und Pakete

## Aufgabe 1: Rechte anzeigen

Für die Übung wurde der Ordner `rechte_training` und darin die Datei
`test.txt` erstellt.

Mit:

`ls -l`

wurden die Dateirechte angezeigt.

Ergebnis für `test.txt`:

`-rw-r--r--`

Die Rechte werden in drei Bereiche aufgeteilt:

-   **Besitzer (user):** `rw-` -- lesen und schreiben
-   **Gruppe (group):** `r--` -- nur lesen
-   **Andere (others):** `r--` -- nur lesen

Das erste Zeichen `-` zeigt, dass es sich um eine normale Datei handelt.

## Aufgabe 2: Rechte verstehen

### `r` -- read / lesen

Die Datei darf gelesen werden.

Beispiel: Der Inhalt von `test.txt` kann angezeigt werden.

### `w` -- write / schreiben

Die Datei darf verändert oder beschrieben werden.

Beispiel: Ein Benutzer mit Schreibrecht kann Text in `test.txt` ändern.

### `x` -- execute / ausführen

Eine Datei darf als Programm oder Skript ausgeführt werden.

Beispiel: Ein Shell-Skript benötigt normalerweise ein Ausführungsrecht,
wenn es direkt gestartet werden soll.

## Aufgabe 3: Rechte ändern

Die Rechte wurden nur an der eigenen Testdatei verändert.

Nach dem Test mit `chmod` zeigte `ls -l`:

`-r--r--r--`

Damit hatte die Datei anschließend für Besitzer, Gruppe und andere nur
noch Leserechte.

### Was hat sich geändert?

Vorher:

`-rw-r--r--`

Der Besitzer durfte lesen und schreiben.

Nachher:

`-r--r--r--`

Das Schreibrecht des Besitzers wurde entfernt. Die Datei wurde damit
schreibgeschützt.

`chmod` sollte nur bewusst und an den richtigen Dateien verwendet
werden. Unnötig weitreichende Rechte können Sicherheitsprobleme
verursachen.

## Aufgabe 4: Pakete prüfen

Das verwendete Ubuntu-System nutzt die Paketverwaltung **APT**.

Die Paketverwaltung wurde mit:

`apt --version`

überprüft.

Danach wurden Informationen zum ungefährlichen Paket `nano` angesehen.

Verwendeter Befehl:

`apt show nano`

### Paketinformationen

-   Paketname: `nano`
-   Version: `8.7.1-1ubuntu0.1`
-   Quelle / Origin: Ubuntu
-   Zweck: kleiner, benutzerfreundlicher Texteditor für das Terminal

Für diese Prüfung musste kein neues Paket installiert werden.

## Aufgabe 5: Linux-Alltagskarte

### 5 wichtige Befehle

`pwd` -- zeigt das aktuelle Arbeitsverzeichnis an.

`ls` -- zeigt Dateien und Ordner im aktuellen Verzeichnis.

`cd` -- wechselt das Verzeichnis.

`mkdir` -- erstellt einen neuen Ordner.

`ls -l` -- zeigt Dateien mit zusätzlichen Informationen und Dateirechten
an.

### 3 Regeln für sichere Terminalarbeit

1.  Befehle vor dem Ausführen genau prüfen.
2.  Keine unbekannten Befehle mit `sudo` ausführen.
3.  Dateien und Rechte nur ändern, wenn man weiß, was der Befehl
    bewirkt.

### 3 Hinweise zu Dateirechten

1.  `r` bedeutet lesen, `w` bedeutet schreiben und `x` bedeutet
    ausführen.
2.  Rechte können mit `chmod` geändert werden.
3.  Rechte sollten nur so weit wie notwendig vergeben werden.

## Extra 1: Zahlenwerte für Rechte

Linux-Dateirechte können auch mit Zahlen dargestellt werden.

-   **7 = rwx** = lesen + schreiben + ausführen
-   **6 = rw-** = lesen + schreiben
-   **5 = r-x** = lesen + ausführen
-   **4 = r--** = nur lesen

Dabei gelten:

-   `r = 4`
-   `w = 2`
-   `x = 1`

Die Werte werden addiert.

### Beispiel `755`

Die drei Zahlen stehen für Besitzer, Gruppe und andere:

-   Besitzer: `7 = rwx`
-   Gruppe: `5 = r-x`
-   Andere: `5 = r-x`

`755` bedeutet also:

`rwxr-xr-x`

Der Besitzer darf lesen, schreiben und ausführen. Gruppe und andere
dürfen lesen und ausführen, aber nicht schreiben.

## Extra 2: Paket genauer ansehen

Das Paket `nano` wurde mit `apt show nano` genauer untersucht.

Dokumentierte Informationen:

-   **Paket:** nano
-   **Version:** 8.7.1-1ubuntu0.1
-   **Quelle:** Ubuntu
-   **Beschreibung:** kleiner, benutzerfreundlicher Texteditor, der von
    Pico inspiriert ist

Damit konnten Paketinformationen geprüft werden, ohne ein neues Programm
installieren zu müssen.

## Reflexion

### Warum sind Rechte wichtig?

Dateirechte bestimmen, wer eine Datei lesen, verändern oder ausführen
darf. Dadurch können Dateien und das System vor unerwünschten Änderungen
geschützt werden.

### Wann kann `chmod` gefährlich sein?

`chmod` kann gefährlich sein, wenn Rechte an der falschen Datei geändert
oder unnötig viele Rechte vergeben werden. Besonders bei Systemdateien
sollte man Änderungen nur durchführen, wenn man genau weiß, welche
Auswirkungen sie haben.

### Welche Terminal-Regel merke ich mir?

Ich möchte mir besonders merken, einen Befehl vor dem Ausführen genau zu
prüfen. Bei Befehlen wie `chmod`, `rm` oder Befehlen mit `sudo` ist das
besonders wichtig.

## Fazit

In dieser Übung habe ich Dateirechte mit `ls -l` geprüft und mit `chmod`
an einer Testdatei verändert. Dabei habe ich die Bedeutung von `r`, `w`
und `x` sowie einfache Zahlenrechte kennengelernt.

Außerdem habe ich die Paketverwaltung APT geprüft und Informationen zum
Paket `nano` angesehen. Die Linux-Alltagskarte fasst wichtige Befehle
und Sicherheitsregeln für die weitere Arbeit im Terminal zusammen.
