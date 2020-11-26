# Pflichtenheft Docker Swarm as a Service M157

## Inhaltsverzeichnis

[Administratives](#Administratives)  
[Ausgangslage](#Ausgangslage)  
[Einleitung](#Einleitung)  
[Ist-Zustand](#Ist-Zustand)  
[Rahmenbedingungen](#Rahmenbedingungen)  
[Ziele](#Ziele)  
   
<a name="Administratives"/>
<a name="Ausgangslage"/>
<a name="Einleitung"/>
<a name="Ist-Zustand"/>
<a name="Rahmenbedingungen"/>
<a name="Ziele"/>


## Administratives

| Input  | Output |
| ------------- | ------------- |
| Auftraggeber  | PowerDataCenter AG  |
| Auftragnehmer  | Dorian Jungi  |
| Beginndatum  | 26.11.2020  |
| Abgabedatum  | 19.01.2021  |
| Klasse  | ST17e  |
| Modul  | M157  |

## Ausgangslage
Die Ausgangslage wurde von Herrn Albrecht bereits erstellt:

Die PowerDataCenter AG betreibt für mehrere Kunden dessen Web Applikationen auf der eigenen Infrastruktur. Dafür setzen Sie im Normalfall für jeden Kunden eine VM auf und installieren dort die entsprechenden Applikationen. Wenn der Kunde mehr Leistung benötigt, dann wird der VM einfach mehr CPUs und RAM zugeteilt und das hat bisher einwandfrei funktioniert. Einer Ihrer Kunden hatte mit einer selbstentwickelten Applikation einen grossen Erfolg und hat die PowerDataCenter AG angefragt, ob diese für Sie ein «Docker Cluster» als Service bereitstellen kann. Die vom Kunden zurzeit genutzte VM ist nämlich ausgelastet und kann nicht weiter skaliert werden. Da die PowerDataCenter AG bisher keine Erfahrungen mit «Docker Clusters» machen konnte, hat die Geschäftsleitung entschieden intern eine Testanlage aufzubauen. Das Ziel ist, dass Ihre Systemtechniker die notwendigen Grundlagen erarbeiten können. Zudem sollen Sie für die restlichen Systemtechniker, die nicht mit der Testanlage zu tun haben, eine kleine Knowledge Wiki Seite, sowie eine Anleitung erstellen. Das Cluster soll im Anschluss der Geschäftsleitung präsentiert werden (Mithilfe einer Demoanwendung, die auf dem Cluster läuft).

Da die virtuelle Serverinfrastruktur der PDC AG ausgelastet ist, werde ich mich mit Docker Clusern auseinandersetzen und selbst einen Cluster zu Testzwecken erstellen und anschliessend der GL präsentieren. Ebenfalls werde ich eine Knowledge Wiki Seite erstellen, damit sich andere Mitarbeiter mit dem Thema besser auseinandersetzen können. Dazu beinhaltet das Knowledge Wiki noch eine Anleitung mit allen essentiellen Steps um den Cluster aufsetzen zu können. Auf einer Docker Maschine wird zusätzlich eine Demoanwendung installiert und ebenfalls bei der GL präsentiert.

## Einleitung
Die PowerDataCenter AG hat ein Problem: Ihre VM-Infrastruktur, welche sie für Kunden zur Verfügung stellt, stösst langsam an ihre Grenzen. Die Ressourcen werden knapper. Ein Kunde möchte jetzt, dank einer sehr erfolgreichen Applikation, einen Docker Cluster als Service anfordern. Docker ist eine Virtualisierungsmöglichkeit, basierend auf einem Containersystem. Docker Container sind sehr effizient, sie benötigen nur einen Bruchteil der Ressourcen die eine VM mit den gleichen Services benötigen würde. 
Da jetzt aber die Mitarbeiter der PDC AG noch nie mit Docker gearbeitet haben, müssen sie zuerst einen Test-Cluster erstellen, um darauf dann anschliessend den Cluster als Service liefern zu können. Meine Aufgabe besteht jetzt darin, diesen Cluster entsprechend den Vorgaben aufzusetzen und anschliessend Demonstrationsartig der GL und den anderen Mitarbeitern zu präsentieren. Damit andere Mitarbeiter sich auf der Umgebung nicht verlaufen, werde ich anschliessend noch ein Knowledge-Wiki inklusive einer kleinen Schritt für Schritt Anleitung erstellen und veröffentlichen.

Alle notwendigen Dokumente werden in diesem GitHub Repository gespeichert und laufend aktualisiert.

## Ist-Zustand
Aktuell existiert nur die VM-Infrastruktur der PDC AG. In der PDC AG wurde noch nie mit Docker gearbeitet, somit existiert Docker bisher in keiner Form bei der PDC AG. Die VM-Infrastruktur, welche für den Kunden zur Verfügung gestellt wurde, ist langsam ausgelastet. 

Auf meinem persönlichen Arbeitsgerät ist Docker installiert. Ebenfalls arbeite ich hauptsächlich mit Git, damit ich eine ordentliche Struktur in meinen Dokumenten / Arbeiten habe und damit die Arbeiten stets aktuell gehalten werden können. Ebenfalls sind noch keine VMs vorinstalliert worden. Zur Erstellung von VMs verwende ich Oracle Virtualbox.

## Rahmenbedingungen
Die Geschäftsleitung der Firma PDC AG verlangt, dass:

- Funktionierender Docker Container
- Eine Docker-Cluster Testumgebung
- Eine funktionierende Demoanwendung
- Ein Knowledge-Wiki
- Eine Anleitung zur Erstellung des Clusters
- Eine Präsentation des Endprodukts inkl. Demonstration

erstellt wird. Dazu gibt mir die Firma Zeit bis zum **19.01.2021**.

## Ziele
Bis zum 19.01.2021 sind folgende Ziele zu erfüllen:


Bei Nichteinhaltung eines Ziels, wird eine ausführliche Erklärung zur Situation erstellt und präsentiert.

## Funktionale Anforderungen
Der Service muss die folgenden Anforderungen erfüllen:



