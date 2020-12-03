# Lastenheft Docker Swarm as a Service M157

## Inhaltsverzeichnis

[Administratives](#Administratives)  
[Ausgangslage](#Ausgangslage)  
[Einleitung](#Einleitung)  
[Ist-Zustand](#Ist-Zustand)  
[Rahmenbedingungen](#Rahmenbedingungen)  
[Ziele](#Ziele)  
[Anforderungen](#Anforderungen)  
 
   
<a name="Administratives"/>
<a name="Ausgangslage"/>
<a name="Einleitung"/>
<a name="Ist-Zustand"/>
<a name="Rahmenbedingungen"/>
<a name="Ziele"/>
<a name="Anforderungen"/>



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

Alle notwendigen Dokumente (Lastenheft / Angebot) werden in diesem GitHub Repository gespeichert und laufend aktualisiert.

## Ist-Zustand
Aktuell existiert nur die VM-Infrastruktur der PDC AG. In der PDC AG wurde noch nie mit Docker gearbeitet, somit existiert Docker bisher in keiner Form bei der PDC AG. Die VM-Infrastruktur, welche für den Kunden zur Verfügung gestellt wurde, ist langsam ausgelastet. 

Der Auftragnehmer hat bereits Docker auf seinem Arbeitsgerät installiert. Er arbeitet hauptsächlich mit Git, um eine ordentliche Struktur ohne Chaos sicherzustellen. Bisher wurden keine VMs oder Container vorinstalliert. Der Auftragnehmer verwendet Oracle Virtualbox als Virtualisierunglösung. 

## Rahmenbedingungen
Die Geschäftsleitung der Firma PDC AG verlangt, dass ihre Serverinfrastruktur zu Ende des Projektes mit einem Docker Swarm Cluster ergänzt werden kann.

## Ziele
Bis zum 19.01.2021 sind folgende Ziele zu erfüllen:

- Eine Funktionierende Testumgebung für Docker
- Mehrere Container müssen parallel miteinander kommunizieren können
- Der Service wird anschliessend präsentiert und seine Funktionen demonstriert

## Anforderungen

### Funktionale Anforderungen
Der Service muss die folgenden Anforderungen erfüllen:

- Ein Docker Cluster mit mehreren Docker Containern muss laufen
- Eine Demoandwendung läuft einwandfrei auf einem der Container
- Die Container können von einem Master gesteuert werden

### Nichtfunktionale Anforderungen

- 24/7 Support falls Docker Cluster abstürzt etc. inkl. Pikett bei Notfällen
- Service muss unterbruchsfrei laufen

## Fragenkatalog

Wieso wird zur Umsetzung Docker verwendet?

> Docker ist im Vergleich zu bisher herkömmlichen Hypervisor-Virtualisierungsmethoden noch ressourcenschonender.

Was ist der Unterschied zu Hypervisor-Virtualisierung und dem Docker-Container System?

> Hypervisor-Virtualisierungsmethoden verwenden zur Erstellung meistens ISO oder OVA Files. Docker hingegen verwendet ein Dockerfile. Ein Dockerfile ist eine Konfigurationsdatei mit allen nötigen Informationen zur Erstellung eines Containers (wie bspw. CPU, RAM, und OS).

Gibt es vergleichbare Alternativen zu Docker?

> Ja diese gibt es. Ein Beispiel wäre Kubernetes, es basiert auf dem gleichen Prinzip. Es existieren auch andere ähnliche Technologien wie z.B. LXD, runC oder LXC.

