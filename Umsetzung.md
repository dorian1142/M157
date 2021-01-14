# Umsetzungsdokumentation

## Inhaltsverzeichnis

[Einleitung](#Einleitung)  
[IPERKA](#IPERKA)  


<a name="Einleitung"/>
<a name="IPERKA"/>

## Einleitung
In diesem Dokument wird die Umsetzung sowie die Planung, Informationsbeschaffung und Auswertung des Projekts beschrieben. Zu jedem Projekt gehört eine angemessene Vorgehensweise, weshalb ich als Projektmethode IPERKA gewählt habe. Ich habe bereits oft mit IPERKA gearbeitet, dies vereinfacht das Vorgehen massiv.

## IPERKA

### Informieren
Als erstes muss ich mich ausführlich über die Funktionsweise und den Aufbau von Docker Swarm informieren, da ich noch nie damit gearbeitet habe. Ich habe mich auf der [offiziellen Docker Webseite](https://docs.docker.com/engine/swarm/swarm-tutorial/create-swarm/) darüber informiert. Ebenfalls werde ich mich an der vorgegebenen Anleitung orientieren, um jede mögliche Fehlerquelle ausschliessen zu können. Ein Mitarbeiter meines Betriebs hat mich ebenfalls auf [Digitalocean](https://www.digitalocean.com/community/tutorials/how-to-create-a-cluster-of-docker-containers-with-docker-swarm-and-digitalocean-on-ubuntu-16-04) aufmerksam gemacht. Ich habe diese Webseite ebenfalls zur Informationsbeschaffung verwendet.

### Planen
Die Planung der Umsetzung ist wie folgt strukturiert:
- 07.01.2021: Informationsbeschaffung, Planung, Entscheidung und Beginn der Realisation
- 14.01.2021: Realisation (Implementation)
- 21.01.2021: Kontrolle, Auswertung und Abgabe des Projekts
  
### Entscheiden
Als nächstes muss ich mich für eine Vorgehensweise und Technologie entscheiden. Ich habe die Möglichkeit, zwischen 3 verschiedenen Betriebssystemen zu arbeiten:

- Windows
- Linux
- MacOS

Ich habe mich für das Windwos OS entschieden, um alle Modulbedingten Dokumente und Technologien auf einem zentralen Gerät speichern und verwalten zu können.

Ebenfalls habe ich mich für die [offizielle Docker Webseite](https://docs.docker.com/engine/swarm/swarm-tutorial/create-swarm/) zur Umsetzungshilfe entschieden, da diese ausführlich erklärt wie vorgegangen werden muss. Da mein Zeitbudget eher knapp ist, darf ich mir keine groben Fehler erlauben.

### Realisieren
Um den Docker Swarm erstellen zu können, benötige ich zuerst eine Manager VM. Diese habe ich mittels Oracle Virtualbox erstellt und 'manager' genannt. Auf der VM läuft eine debian version, welche ich noch auf meiner Festplatte gefunden habe. Die Maschine hat etwa 1GB RAM und 15GB HD Speicher. Das OS läuft ohne GUI, da ich sowieso nur via SSH darauf arbeiten werde und eine GUI Installation viel zu lange dauern würde. Auf dem Manager Node wurde ein User namens 'manageruser' erstellt. Anschliessend habe ich noch 2 andere Debian Maschinen erstellt namens 'host1' und 'host2'. Diese werden die 'worker' des Swarms bilden.
### Kontrollieren
### Auswerten

