# Easy ILP: Virtuelle Maschinen sicher nutzen

## Aufgabe 1: Zustand der VM prüfen

Für die Aufgabe verwende ich meine vorhandene virtuelle Maschine
`Lubuntu_spaß` in Oracle VirtualBox.

### Aktuelle Einstellungen

-   VM-Name: `Lubuntu_spaß`
-   Gastbetriebssystem: Ubuntu 24.04 LTS (64-bit)
-   RAM: 4096 MB (4 GB)
-   CPU: 2 vCPUs
-   Virtuelle Festplatte: 25 GB VDI
-   Speicherart: dynamisch belegt
-   Aktueller Netzwerkmodus: Host-only Adapter
-   Netzwerkadapter: aktiviert

**Ergebnis:** Die wichtigsten Einstellungen der VM wurden kontrolliert
und dokumentiert.

## Aufgabe 2: VM sicher starten

Die VM wurde bereits erfolgreich gestartet und Lubuntu konnte normal
verwendet werden.

Beim Arbeiten in der VM achte ich darauf:

-   mich normal am System anzumelden,
-   keine unbekannten Dateien zu öffnen,
-   keine unbekannten Programme zu installieren,
-   den Zustand des Systems zu beobachten,
-   Netzwerkzugriffe nur passend zur Testaufgabe zu verwenden.

### Internetverbindung

Mit dem aktuellen Netzwerkmodus **Host-only** ist die VM für eine
isolierte Testumgebung eingerichtet. Direkter Internetzugriff ist dabei
standardmäßig nicht vorgesehen.

Bei einem früheren Test mit **NAT** konnte die VM das Internet
erreichen. Dadurch kann ich den Netzwerkmodus passend zum jeweiligen
Zweck auswählen.

**Ergebnis:** Die VM läuft und der Netzwerkzustand ist bekannt.

## Aufgabe 3: Snapshot erstellen

Die Snapshot-Funktion von VirtualBox wurde bereits praktisch verwendet.

Ein Snapshot speichert einen bestimmten Zustand einer virtuellen
Maschine. Vor Änderungen oder Tests kann dadurch ein
Wiederherstellungspunkt erstellt werden.

### Warum ist ein Snapshot nützlich?

-   Der Zustand vor einem Test kann festgehalten werden.
-   Fehlerhafte Änderungen können leichter rückgängig gemacht werden.
-   Software kann in einer kontrollierten Umgebung ausprobiert werden.
-   Bei Übungen muss die VM nicht immer komplett neu eingerichtet
    werden.

Snapshots ersetzen jedoch kein vollständiges Backup. Für eine
längerfristige Sicherung sollte die VM zusätzlich gesichert oder
exportiert werden.

## Aufgabe 4: Netzwerk vorsichtig prüfen

### Aktueller Netzwerkmodus

Die VM verwendet aktuell:

**Host-only Adapter**

Dieser Modus eignet sich für eine isolierte Testumgebung, in der Host
und Test-VMs miteinander kommunizieren können, ohne die VM direkt wie
einen normalen Rechner in das externe Netzwerk einzubinden.

### Frühere Netzwerktests

Ich habe bereits verschiedene Netzwerkmodi praktisch getestet:

-   NAT
-   Netzwerkbrücke / Bridged
-   Host-only

Bei NAT konnte die VM eine Verbindung zum Internet herstellen. Beim
Host-only-Test konnte außerdem die Kommunikation zwischen virtuellen
Maschinen geprüft werden.

Ich ändere Netzwerkeinstellungen nur bewusst und passend zur jeweiligen
Aufgabe.

## Aufgabe 5: Sicherheitsregeln für virtuelle Maschinen

### Meine 5 Regeln für sichere VM-Nutzung

1.  **Vor größeren Änderungen einen Snapshot erstellen.**\
    Dadurch kann ich bei Problemen zu einem vorherigen Zustand
    zurückkehren.

2.  **Den Netzwerkmodus bewusst auswählen.**\
    Für isolierte Tests kann Host-only sinnvoll sein. Internetzugriff
    aktiviere ich nur, wenn er für die Aufgabe benötigt wird.

3.  **Keine unbekannten Dateien oder Programme öffnen.**\
    Auch eine VM sollte vorsichtig verwendet werden, weil Schadsoftware
    Risiken für Daten, Netzwerk oder gemeinsam genutzte Ressourcen
    verursachen kann.

4.  **Gastbetriebssystem und Programme aktuell halten.**\
    Updates schließen Sicherheitslücken und beheben bekannte Fehler.

5.  **Ressourcen und Zustand der VM vor der Arbeit prüfen.**\
    RAM, CPU, Festplatte und Netzwerk sollten zur Aufgabe passen.
    Änderungen nehme ich nur vor, wenn ich weiß, warum sie notwendig
    sind.

## Extra 1: Netzwerkmodi bewerten

### NAT

Die VM nutzt die Netzwerkverbindung des Hosts für den Zugriff auf
externe Netzwerke und das Internet.

**Geeignet für:**\
Tests, bei denen Internetzugriff benötigt wird.

### Host-only

Die VM befindet sich in einem getrennten virtuellen Netzwerk mit dem
Host und gegebenenfalls anderen Host-only-VMs.

**Geeignet für:**\
Isolierte Labor- und Netzwerktests.

### Welcher Modus ist für Tests sicherer?

Für Tests, die keinen Internetzugriff benötigen, ist **Host-only**
häufig die besser isolierte Variante. Die VM bleibt stärker vom externen
Netzwerk getrennt.

Wenn für die Aufgabe Internetzugriff notwendig ist, kann **NAT**
verwendet werden. Der Netzwerkmodus sollte immer nach dem tatsächlichen
Testzweck gewählt werden.

## Extra 2: Export planen

VirtualBox bietet die Möglichkeit, virtuelle Maschinen zu exportieren.

### Möglicher Ablauf

1.  VirtualBox öffnen.
2.  Die gewünschte VM sauber herunterfahren.
3.  Die Export-Funktion von VirtualBox öffnen.
4.  Die gewünschte virtuelle Maschine auswählen.
5.  Ziel und Exportformat prüfen.
6.  Einen Speicherort mit ausreichend freiem Speicher auswählen.
7.  Export starten.
8.  Nach dem Export prüfen, ob die Sicherungsdatei vorhanden ist.
9.  Die Datei bei Bedarf auf einem geeigneten externen Datenträger oder
    an einem sicheren Backup-Ort speichern.

Ein Export ist sinnvoll, wenn eine VM gesichert, archiviert oder auf
einen anderen geeigneten Rechner übertragen werden soll.

## Reflexion

### Warum sind Snapshots nützlich?

Snapshots sind besonders vor Tests und Änderungen hilfreich. Wenn etwas
nicht funktioniert, kann ein vorheriger Zustand der VM wiederhergestellt
werden.

### Welcher Netzwerkmodus ist für Tests sinnvoll?

Für isolierte Tests finde ich Host-only sinnvoll, weil die Testumgebung
vom normalen externen Netzwerk stärker getrennt bleibt. Wenn Internet
benötigt wird, ist NAT eine praktische Alternative.

### Welche VM-Regel will ich immer beachten?

Vor wichtigen Änderungen oder Experimenten möchte ich zuerst überlegen,
ob ein Snapshot notwendig ist. Außerdem möchte ich den Netzwerkmodus
immer passend zum Zweck auswählen und keine unbekannten Dateien öffnen.

## Fazit

Meine VM `Lubuntu_spaß` ist eine geeignete Testumgebung für VirtualBox.
Sie verwendet 4 GB RAM, 2 vCPUs, eine dynamische 25-GB-VDI-Festplatte
und aktuell einen Host-only Netzwerkadapter.

Durch Snapshots, einen bewusst gewählten Netzwerkmodus, regelmäßige
Updates und vorsichtigen Umgang mit Dateien kann eine virtuelle Maschine
sicher für Lern- und Testaufgaben genutzt werden.
