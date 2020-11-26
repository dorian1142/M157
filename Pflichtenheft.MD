# Pflichtenheft Docker Swarm as a Service M157

## Inhaltsverzeichnis

[Administratives](#Administratives)  
[Ausgangslage](#Ausgangslage)  
[Einleitung](#Einleitung)  
   
<a name="Administratives"/>
<a name="Ausgangslage"/>
<a name="Einleitung"/>

## Administratives

| Input  | Output |
| ------------- | ------------- |
| Auftraggeber  | PowerDataCenter AG  |
| Auftragnehmer  | Dorian Jungi  |
| Beginndatum  | 26.11.2020  |
| Abgabedatum  | 19.01.2020  |
| Klasse  | ST17e  |
| Modul  | M157  |

## Ausgangslage
Die Ausgangslage wurde von Herrn Albrecht bereits erstellt:

Die PowerDataCenter AG betreibt für mehrere Kunden dessen Web Applikationen auf der eigenen Infrastruktur. Dafür setzen Sie im Normalfall für jeden Kunden eine VM auf und installieren dort die entsprechenden Applikationen. Wenn der Kunde mehr Leistung benötigt, dann wird der VM einfach mehr CPUs und RAM zugeteilt und das hat bisher einwandfrei funktioniert. Einer Ihrer Kunden hatte mit einer selbstentwickelten Applikation einen grossen Erfolg und hat die PowerDataCenter AG angefragt, ob diese für Sie ein «Docker Cluster» als Service bereitstellen kann. Die vom Kunden zurzeit genutzte VM ist nämlich ausgelastet und kann nicht weiter skaliert werden. Da die PowerDataCenter AG bisher keine Erfahrungen mit «Docker Clusters» machen konnte, hat die Geschäftsleitung entschieden intern eine Testanlage aufzubauen. Das Ziel ist, dass Ihre Systemtechniker die notwendigen Grundlagen erarbeiten können. Zudem sollen Sie für die restlichen Systemtechniker, die nicht mit der Testanlage zu tun haben, eine kleine Knowledge Wiki Seite, sowie eine Anleitung erstellen. Das Cluster soll im Anschluss der Geschäftsleitung präsentiert werden (Mithilfe einer Demoanwendung, die auf dem Cluster läuft).

Da die virtuelle Serverinfrastruktur der PDC AG ausgelastet ist, werde ich mich mit Docker Clusern auseinandersetzen und selbst einen Cluster zu Testzwecken erstellen und anschliessend der GL präsentieren. Ebenfalls werde ich eine Knowledge Wiki Seite erstellen, damit sich andere Mitarbeiter mit dem Thema besser auseinandersetzen können. Dazu beinhaltet das Knowledge Wiki noch eine Anleitung mit allen essentiellen Steps um den Cluster aufsetzen zu können.

## Einleitung

