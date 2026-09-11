# Easy ILP: Linux in einer VM

## Aufgabe 1: Linux-Distribution auswählen

Für diese Aufgabe verwende ich meine vorhandene Linux-VM mit **Lubuntu
auf Basis von Ubuntu 24.04 LTS**.

### Gründe für meine Wahl

1.  Ubuntu/Lubuntu ist gut dokumentiert und es gibt viele Anleitungen
    und Hilfestellungen.
2.  Lubuntu benötigt vergleichsweise wenige Ressourcen und eignet sich
    deshalb gut für eine virtuelle Lern- und Testumgebung.

### Für Anfänger geeignet?

Ja. Lubuntu bietet eine grafische Benutzeroberfläche und viele
alltägliche Funktionen können ähnlich wie unter Windows über Menüs und
Programme verwendet werden. Gleichzeitig kann man schrittweise den
Umgang mit dem Linux-Terminal lernen.

## Aufgabe 2: Linux starten

Virtualisierungssoftware: **Oracle VirtualBox**

Vorhandene VM: `Lubuntu_spaß`

Die VM wurde gestartet und das Linux-System konnte erfolgreich verwendet
werden. Eine erneute Installation war für diese Aufgabe nicht notwendig,
weil bereits eine funktionsfähige Linux-VM vorhanden war.

Während früherer Starts gab es zeitweise einen schwarzen Bildschirm.
Nach erneutem Start konnte das System jedoch erfolgreich geladen werden.

**Ergebnis:** Linux startet und die Anmeldung funktioniert.

## Aufgabe 3: Systemdaten prüfen

Die Systeminformationen wurden direkt im Linux-Terminal mit
`hostnamectl` und `free -h` geprüft.

### Ergebnisse von `hostnamectl`

-   Systemname / Static hostname: `lubuntuvirtualbox`
-   Betriebssystem: Ubuntu 24.04.3 LTS
-   Kernel: Linux 7.0.0-30-generic
-   Architektur: x86-64
-   Virtualisierung: oracle
-   Hardware-Modell: VirtualBox

### Arbeitsspeicher mit `free -h`

Zum Zeitpunkt der Prüfung:

-   Arbeitsspeicher gesamt: 3,8 GiB
-   benutzt: 788 MiB
-   frei: 2,1 GiB
-   verfügbar: 3,0 GiB
-   Swap gesamt: 511 MiB
-   Swap benutzt: 0 B

In VirtualBox sind für die VM 4 GB RAM eingestellt. Das Linux-System
zeigte bei der Prüfung rund 3,8 GiB Gesamtspeicher an.

## Aufgabe 4: Linux-Oberfläche erkunden

In Lubuntu habe ich die wichtigsten Bereiche der grafischen Oberfläche
verwendet:

-   Anwendungsmenü
-   Dateimanager
-   Systemeinstellungen
-   Terminal
-   Standardprogramme

### Ähnlichkeiten zu Windows

-   Programme können über ein grafisches Menü geöffnet werden.
-   Dateien und Ordner werden mit einem Dateimanager verwaltet.
-   Es gibt Systemeinstellungen für verschiedene Bereiche des Computers.
-   Fenster können geöffnet, minimiert, maximiert und geschlossen
    werden.

### Unterschiede zu Windows

-   Die Oberfläche und die Position einiger Einstellungen unterscheiden
    sich.
-   Linux verwendet eine andere Verzeichnisstruktur.
-   Viele Verwaltungs- und Lernaufgaben lassen sich direkt im Terminal
    erledigen.
-   Linux-Befehle und Paketverwaltung unterscheiden sich von Windows.

## Aufgabe 5: Terminal verwenden

Die geforderten Befehle wurden praktisch im Terminal ausgeführt.

### `pwd`

Ergebnis:

`/home/liudmyla`

Bedeutung: `pwd` zeigt den vollständigen Pfad des aktuellen
Arbeitsverzeichnisses.

### `ls`

Der Befehl zeigte unter anderem folgende Inhalte:

`Bilder`, `Desktop`, `Dokumente`, `Downloads`, `Musik`, `Öffentlich`,
`snap`, `test.txt`, `Videos`, `Vorlagen`

Bedeutung: `ls` zeigt Dateien und Ordner im aktuellen Verzeichnis.

### `whoami`

Ergebnis:

`liudmyla`

Bedeutung: `whoami` zeigt den aktuell angemeldeten Benutzer.

### `date`

Ergebnis bei der Durchführung:

`Fr 11. Sep 17:25:12 CEST 2026`

Bedeutung: `date` zeigt Datum, Uhrzeit und Zeitzone des Systems.

## Extra 1: Zweite Linux-Distribution vergleichen

Als zweite Distribution vergleiche ich **Linux Mint** mit Lubuntu.

### Drei Unterschiede

1.  **Desktop-Oberfläche**\
    Lubuntu verwendet eine besonders leichte Desktop-Umgebung. Linux
    Mint wird häufig mit Cinnamon verwendet, dessen Oberfläche stärker
    an klassische Desktop-Systeme erinnert.

2.  **Ressourcenbedarf**\
    Lubuntu ist auf einen geringen Ressourcenverbrauch ausgerichtet.
    Deshalb eignet es sich besonders gut für kleinere VMs oder ältere
    Hardware. Eine Mint-Installation mit Cinnamon benötigt in der Regel
    etwas mehr Ressourcen.

3.  **Schwerpunkt**\
    Lubuntu legt besonderen Wert auf ein leichtgewichtiges System. Linux
    Mint legt großen Wert auf eine komfortable Desktop-Erfahrung für
    Anwender, die von anderen Desktop-Betriebssystemen wechseln.

Beide Distributionen sind grundsätzlich für Lernzwecke und
Linux-Einsteiger geeignet.

## Extra 2: Ordner im Terminal erstellen

Die Aufgabe wurde praktisch durchgeführt.

### Verwendete Befehle

`mkdir ilp_linux`

Erstellt im aktuellen Verzeichnis einen neuen Ordner mit dem Namen
`ilp_linux`.

`cd ilp_linux`

Wechselt in den neu erstellten Ordner.

`pwd`

Ergebnis:

`/home/liudmyla/ilp_linux`

Damit wurde bestätigt, dass ich mich im neu erstellten Ordner befinde.

## Reflexion

### Was war in Linux neu?

Neu war für mich besonders die Arbeit mit dem Terminal und die
Linux-Verzeichnisstruktur. Viele Aufgaben, die unter Windows über die
grafische Oberfläche erledigt werden, können unter Linux schnell mit
Befehlen durchgeführt werden.

### Welcher Terminal-Befehl war nützlich?

`pwd` finde ich besonders nützlich, weil ich damit jederzeit
kontrollieren kann, in welchem Verzeichnis ich mich gerade befinde. Auch
`ls` ist wichtig, weil ich damit den Inhalt eines Verzeichnisses sehen
kann.

### Was ist ähnlich wie bei meinem normalen System?

Ähnlich wie bei Windows gibt es eine grafische Oberfläche, einen
Dateimanager, Einstellungen und Programme. Dadurch kann man viele
grundlegende Aufgaben auch ohne Terminal erledigen.

## Fazit

Ich habe Linux in meiner vorhandenen VirtualBox-VM erkundet und reale
Systeminformationen geprüft. Das System läuft mit Ubuntu 24.04.3 LTS,
Kernel 7.0.0-30-generic und x86-64-Architektur.

Außerdem habe ich die Befehle `pwd`, `ls`, `whoami`, `date`, `mkdir` und
`cd` praktisch verwendet. Mit `mkdir ilp_linux` habe ich einen eigenen
Ordner erstellt, bin mit `cd` hineingewechselt und habe mit `pwd` den
Pfad `/home/liudmyla/ilp_linux` überprüft.
