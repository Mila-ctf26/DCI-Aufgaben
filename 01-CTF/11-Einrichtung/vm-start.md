# Easy ILP: Erste virtuelle Maschine starten

## Aufgabe 1: Voraussetzungen prüfen

-   Virtualisierungssoftware kann auf dem Computer verwendet werden.
-   Auf dem Computer ist ausreichend Speicher für eine virtuelle
    Maschine vorhanden.
-   Eine ISO-Datei für Lubuntu wurde für die Installation verwendet.
-   Die Voraussetzungen für die Einrichtung einer VM waren erfüllt.

**Ergebnis:** Die virtuelle Maschine konnte eingerichtet und gestartet
werden.

## Aufgabe 2: Software installieren

Als Virtualisierungssoftware verwende ich **Oracle VirtualBox**.

-   Programm: Oracle VirtualBox
-   Version: 7.2.16 r174877
-   Hersteller: Oracle
-   Die Software wurde installiert und startet erfolgreich.

VirtualBox ermöglicht es, virtuelle Maschinen auf meinem Windows-PC zu
erstellen, zu konfigurieren und auszuführen.

## Aufgabe 3: VM erstellen

Für die praktische Übung wurde folgende virtuelle Maschine eingerichtet:

-   Name der VM: `Lubuntu_spaß`
-   Gastbetriebssystem: Ubuntu 24.04 LTS (Noble Numbat), 64-bit
-   RAM: 4096 MB (4 GB)
-   CPUs: 2 vCPUs
-   Virtuelle Festplatte: 25 GB
-   Festplattenformat: VDI
-   Speicherart: dynamisch belegt
-   Installationsmedium: Lubuntu-ISO-Datei

Die VM wurde in VirtualBox angelegt und gespeichert.

## Aufgabe 4: VM starten

Die virtuelle Maschine `Lubuntu_spaß` wurde erfolgreich gestartet.

Das Betriebssystem wurde installiert und konnte anschließend normal
verwendet werden. Während der früheren praktischen Arbeit gab es
zeitweise Probleme mit einem schwarzen Bildschirm beim Start. Nach
erneutem Starten konnte Lubuntu jedoch erfolgreich geladen werden.

Danach konnte ich unter anderem:

-   Lubuntu verwenden,
-   das Terminal öffnen,
-   Befehle ausführen,
-   Netzwerkeinstellungen testen,
-   Dateien innerhalb der VM bearbeiten.

**Ergebnis:** Der Start der VM funktioniert.

## Aufgabe 5: Start dokumentieren

### VM-Start

-   VM-Name: `Lubuntu_spaß`
-   Betriebssystem: Ubuntu 24.04 LTS (64-bit)
-   RAM: 4 GB
-   CPU: 2 vCPUs
-   Virtuelle Festplatte: 25 GB VDI, dynamisch belegt
-   Netzwerkadapter: aktiviert
-   Aktueller Netzwerkmodus: Host-only Adapter
-   Start erfolgreich: Ja

### Zwei Dinge, die ich gelernt habe

1.  Eine virtuelle Maschine verwendet virtuelle Hardware, deren
    Ressourcen von der physischen Hardware des Host-Computers
    bereitgestellt werden.
2.  Der Netzwerkmodus bestimmt, wie die VM mit dem Host, anderen Geräten
    oder dem Internet kommunizieren kann.

## Extra 1: Netzwerkmodus vergleichen

### Host-only Adapter

Bei Host-only entsteht ein separates virtuelles Netzwerk zwischen dem
Host und den angeschlossenen virtuellen Maschinen. Dieser Modus eignet
sich gut für isolierte Testumgebungen.

### NAT

Bei NAT verwendet die VM die Netzwerkverbindung des Hosts, um auf
externe Netzwerke bzw. das Internet zuzugreifen. Die VM ist dabei nicht
wie ein eigenständiger Rechner direkt im lokalen Netzwerk sichtbar.

### Vergleich

-   **Host-only:** gut für isolierte Kommunikation und Testnetzwerke.
-   **NAT:** praktisch, wenn die VM Internetzugriff benötigt.

Ich habe in meiner praktischen Arbeit außerdem bereits den
Bridged-/Netzwerkbrücken-Modus getestet.

## Extra 2: Ressourcen anpassen

Die Ressourcen einer VM können in VirtualBox angepasst werden, wenn die
VM ausgeschaltet ist.

Bei meiner VM sind aktuell eingestellt:

-   2 vCPUs
-   4 GB RAM

Bei der Ressourcenverteilung muss darauf geachtet werden, dass auch für
das Host-System genügend CPU und RAM übrig bleiben. Zu wenig RAM oder
CPU kann die VM langsam machen. Eine zu hohe Zuweisung kann dagegen den
Host verlangsamen.

## Reflexion

### Was war beim Einrichten leicht?

Nachdem ich die grundlegende Bedienung von VirtualBox verstanden hatte,
waren das Auswählen der VM und das Öffnen der Einstellungen einfach.
RAM, CPU und Festplattengröße lassen sich übersichtlich kontrollieren.

### Wo gab es Probleme?

Beim praktischen Arbeiten gab es zeitweise Probleme beim Start der VM,
zum Beispiel einen schwarzen Bildschirm. Auch die verschiedenen
Netzwerkmodi und die Kommunikation zwischen Host und virtuellen
Maschinen benötigten etwas mehr Übung.

### Welche Einstellung ist für eine VM besonders wichtig?

Mehrere Einstellungen sind wichtig. Besonders wichtig sind RAM, CPU und
Netzwerkmodus. Die VM braucht genügend Ressourcen, ohne den Host zu
überlasten. Der Netzwerkmodus muss außerdem zum jeweiligen Einsatzzweck
passen.

## Fazit

Meine erste virtuelle Umgebung wurde erfolgreich mit Oracle VirtualBox
eingerichtet. Die VM `Lubuntu_spaß` läuft mit Ubuntu 24.04 LTS, 2 vCPUs,
4 GB RAM und einer dynamischen virtuellen Festplatte mit 25 GB. Durch
die praktische Arbeit habe ich gelernt, eine VM zu starten, ihre
Ressourcen zu kontrollieren und unterschiedliche Netzwerkmodi
einzuordnen.
