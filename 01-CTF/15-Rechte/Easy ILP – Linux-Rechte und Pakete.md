# Easy ILP: Linux-Rechte und Pakete

## Aufgabe 1: Rechte anzeigen

Ich habe den Ordner `rechte_training` erstellt und darin die Datei `test.txt`.

Verwendete Befehle:

```bash
mkdir rechte_training
cd rechte_training
touch test.txt
ls -l
```

Ergebnis:

```text
-rw-r--r-- 1 liudmyla liudmyla 0 Sep 7 07:56 test.txt
```

Die Rechte bedeuten:

- Besitzer: `rw-`
- Gruppe: `r--`
- Andere: `r--`

Der Besitzer kann die Datei lesen und schreiben.  
Die Gruppe und andere Benutzer können die Datei nur lesen.

## Aufgabe 2: Rechte verstehen

`r` = lesen (read)  
Beispiel: Der Inhalt einer Datei kann gelesen werden.

`w` = schreiben (write)  
Beispiel: Der Inhalt einer Datei kann geändert werden.

`x` = ausführen (execute)  
Beispiel: Eine ausführbare Datei oder ein Skript kann gestartet werden.

## Aufgabe 3: Rechte ändern

Zuerst hatte die Datei folgende Rechte:

```text
-rw-r--r--
```

Ich habe dem Besitzer das Schreibrecht entzogen:

```bash
chmod u-w test.txt
```

Danach waren die Rechte:

```text
-r--r--r--
```

Änderung: Dem Besitzer wurde das Schreibrecht entzogen.

Danach habe ich das Schreibrecht wieder hinzugefügt:

```bash
chmod u+w test.txt
```

Ergebnis:

```text
-rw-r--r--
```

Ich habe die Rechte nur an meiner Testdatei geändert.

## Aufgabe 4: Pakete prüfen

Mein Ubuntu-System verwendet die Paketverwaltung APT.

```bash
apt --version
```

Ergebnis:

```text
apt 3.2.0 (amd64)
```

Ich habe Informationen über das Paket `nano` gesucht, ohne etwas zu installieren.

```bash
apt show nano
```

Paketname: `nano`  
Version: `8.7.1-1ubuntu0.1`  
Zweck: Nano ist ein einfacher Texteditor für das Terminal.  
Origin: Ubuntu

## Aufgabe 5: Linux-Alltagskarte

Ich habe die Datei `linux-karte.md` erstellt.

### 5 wichtige Befehle

`pwd` – zeigt das aktuelle Arbeitsverzeichnis an.  
`ls` – zeigt Dateien und Ordner an.  
`cd` – wechselt das Verzeichnis.  
`mkdir` – erstellt einen neuen Ordner.  
`ls -l` – zeigt Dateien und ihre Rechte an.

### 3 Regeln für sichere Terminalarbeit

1. Befehle vor dem Ausführen genau prüfen.
2. Keine unbekannten Befehle mit `sudo` ausführen.
3. Dateien und Rechte nur ändern, wenn man weiß, was der Befehl macht.

### 3 Hinweise zu Dateirechten

1. `r` bedeutet lesen, `w` bedeutet schreiben und `x` bedeutet ausführen.
2. Rechte können mit `chmod` geändert werden.
3. Rechte sollten nur so weit wie nötig vergeben werden.

## Extra 1: Zahlenwerte für Rechte

Die Zahlenwerte sind:

`r = 4`  
`w = 2`  
`x = 1`

Daraus ergibt sich:

`7 = rwx` = lesen, schreiben und ausführen  
`6 = rw-` = lesen und schreiben  
`5 = r-x` = lesen und ausführen  
`4 = r--` = nur lesen

### Beispiel: 755

`755` bedeutet:

Besitzer: `rwx` = lesen, schreiben und ausführen  
Gruppe: `r-x` = lesen und ausführen  
Andere: `r-x` = lesen und ausführen

Als Rechte-Anzeige entspricht das:

```text
rwxr-xr-x
```

## Extra 2: Paket genauer ansehen

Ich habe das Paket `nano` genauer angesehen.

Verwendeter Befehl:

```bash
apt show nano
```

Ergebnis:

Paket: `nano`  
Version: `8.7.1-1ubuntu0.1`  
Beschreibung: small, friendly text editor inspired by Pico  
Quelle / Origin: Ubuntu

## Reflexion

### Warum sind Rechte wichtig?

Dateirechte sind wichtig, weil sie festlegen, wer eine Datei lesen, ändern oder ausführen darf. Sie schützen Dateien vor unerlaubten Änderungen.

### Wann kann chmod gefährlich sein?

`chmod` kann gefährlich sein, wenn man die Rechte wichtiger Dateien falsch ändert oder zu viele Rechte vergibt.

### Welche Terminal-Regel merkst du dir?

Ich merke mir: Bevor ich einen Befehl ausführe, prüfe ich, was der Befehl macht.