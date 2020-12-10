# Angebot Docker Swarm as a Service M157

## Inhaltsverzeichnis

[Einleitung](#Einleitung)  
[Lösungsbeschrieb](#Lösungsbeschrieb)  
[Mengengerüst](#Mengengerüst)  
[Planung](#Planung)  
[Risikoanalyse](#Risikoanalyse)  
[Rahmenbedingungen](#Rahmenbedingungen)  
[Bauseitige-Anforderungen](#Bauseitige-Anforderungen)  
[Antwortkatalog](#Antwortkatalog)  

<a name="Einleitung"/>
<a name="Lösungsbeschrieb"/>
<a name="Mengengerüst"/>
<a name="Planung"/>
<a name="Risikoanalyse"/>
<a name="Rahmenbedingungen"/>
<a name="Bauseitige-Anforderungen"/>
<a name="Antwortkatalog"/>

## Einleitung

| Input  | Output |
| ------------- | ------------- |
| Auftraggeber  | PowerDataCenter AG  |
| Auftragnehmer  | Dorian Jungi  |  
| Beginndatum  | 26.11.2020  |
| Abgabedatum  | 19.01.2021  |

## Problemstellung

Die PowerDataCenter AG ist bereits Kunde des Auftragnehmers und mietet bereits eine Virtuelle Infrastruktur. Diese gelangt langsam an ihre Kapazitätsgrenzen. Nun möchte die PDC AG ihre Ressourcen auf eine andere Weise vergrössern. Die PDC AG möchte mit Docker weiterarbeiten, da Docker ressourcenschonender als Hypervisor-Infrastrukturen laufen kann und einfacher zu managen ist.

## Lösungsbeschrieb

Der Auftragnehmer Dorian Jungi kümmert sich um die Lösungsmethode. Die Anforderungen werden wie folgt gehandhabt:

### Funktionale Anforderungen

- Ein Docker Cluster mit mehreren Docker Containern muss laufen
> Der Auftragnehmer verfügt über eine Umgebung, auf welcher Docker installiert wird. Ebenfalls wird auf dieser Umgebung ein Docker Cluster erstellt und wenn nötig auch virtuelle Maschinen bereitgestellt. Zur Virtualisierung wird der Hypervisor Virtualbox von Oracle verwendet.
- Eine Demoandwendung läuft einwandfrei auf einem der Container
> Zur Demonstration der Funktion des Clusters, wird auf einem der Container die Software Python installiert. 
- Die Container können von einem Master gesteuert werden
> In einem Docker Cluster benötigt es immer einen Master, der andere Container managen kann. In diesem Fall wird ein Master und 3 Slaves erstellt.

### Nichtfunktionale Anforderungen

- 24/7 Support falls Docker Cluster abstürzt etc. inkl. Pikett bei Notfällen
> Der Auftraggeber hat bei einem Notfall garantierten Support. Der Support ist jederzeit erreichbar via Telefon. Die Telefonnummer ist dem Auftraggeber bekannt.
- Service weist eine Verfügbarkeit von 99.98% auf
> Der Cluster wird auf einer Umgebung aufgesetzt, welche rund um die Uhr verfügbar ist. 

## Mengengerüst

Zur Umsetzung der Lösung durch den Auftragnehmer werden folgende Hardware und Software verwendet:

| Stückzahl | Produkt | Kosten |
| ------------- | ------------- | ------------- |
| 1x | HP Elitebook 840 G3 (16GB RAM, 2 Core CPU) | Bereits vorhanden |
| 1x | Docker Software | Kostenlos |  
| 1x | Oracle Virtualbox Software | Kostenlos  |
| 1x | GitHub (zur Dokumentablage)  | Kostenlos |
| 16 Stunden | Aufwand  | 100.- CHF / Stunde |


Da der Auftragnehmer bereits über die benötigte Hardware verfügt, muss diese nicht mehr bezahlt werden und ist ebenfalls kostenlos.

## Planung

- **03.12.2020**
Verfassen des Angebots

- **10.12.2020**
Verfassen des Angebots, Beginn der Implementierung des Docker Clusters
> Meilenstein 1: Angebot fertig verfasst und überprüft

- **17.12.2020**
Implementierung des Docker Clusters

- **07.01.2021**
Implementierung des Docker Clusters
> Meilenstein 2: Implementation des Clusters abgeschlossen und funktionstauglich

- **14.01.2020**
Präsentation und Demonstration des Endprodukts
> Meilenstein 3: Präsentation und Abschluss des Projekts

Zwischen dem 17.12.2020 und dem 07.01.2021 sind Weihnachtsferien. Deshalb wird währenddessen auch nicht gearbeitet.

## Risikoanalyse
Zu jedem Projekt gehören auch Risiken. Allfällige Risiken des Docker Swarm Services werden hier aufgelistet.

- R1: Ausfall eines Docker Containers
- R2: Ausfall des gesamten Clusters
- R3: Ausfall der Hardware
- R4: Krankheit des Auftragnehmers
- R5: Konkurs des Arbeitgebers

![pic not found](https://github.com/dorian1142/M157/blob/main/RIsikoanalyse.PNG)

## Rahmenbedingungen
Damit keine Services vergessen gehen und damit keine unnötigen zusätzlichen Services angeboten werden, werden hier die Rahmenbedingungen notiert:

- Bestehende Grundinfrastruktur
- Büro und Arbeitsgerät stehen zur Verfügung
- Projekt muss am 14.01.2021 fertiggestellt sein

Nicht beinhaltet ist im Service:

- Getränke / Essen
- Anreise für geschäftliche Zwecke
- Hotelübernachtungen

## Bauseitige-Anforderungen
Auftragnehmer an Auftraggeber
Hier werden die Anforderungen aufgelistet, welche von der Seite des Auftraggebers erfüllt sein müssen:

- Arbeitsgerät wird zur Verfügung gestellt
- Netzwerk mit Uplink von mind. 100Mbit/s
- Zielinfrastruktur bereit


## Antwortkatalog
In diesem Abschnitt werden die im Lastenheft notierten Fragen beantwortet

Wieso wird zur Umsetzung Docker verwendet?
> Docker bietet im Vergleich zu sehr vielen anderen Technologien die Möglichkeit, auf einer Infrastruktur möglichst wenig Kapazitäten auszulasten. Somit können die Kapazitäten effizienter genutzt werden und es werden weniger Ressourcen für die Management Infrastruktur benötigt.

Was ist der Unterschied zu Hypervisor-Virtualisierung und dem Docker-Container System?
> Eine normale Hypervisor Lösung verwendet zur Virtualisierung eine aufwendigere Management Infrastruktur welche mehr Ressourcen benötigt. Docker Container hingegen sind sehr schmal gebaut und nur auf das nötigste reduziert. Stellen Sie sich Docker Container wie ein ZIP File vor, während ein Hypervisor eine einfache Ordnerstruktur bietet.

Gibt es vergleichbare Alternativen zu Docker?
> Ja es gibt mehrere verschiedene sehr ähnliche Alternativen zu Docker. Beispiele wären: Kubernetes, Core OS, LXC Linux Containers, OpenVZ etc. Es existieren etliche Alternativen. Docker hat sich mit der innovativen Container Technologie am meisten durchsetzen können.

Welche Abteilung ist am besten für die Umsetung geeignet?
> Das System Engineering der PDC AG eignet sich am besten für die Umsetzung des Projekts. Unter Leitung von Dorian Jungi ist sichergestellt, dass sich das Projekt nicht nur technisch, sondern auch menschlich in besten Händen befindet. 



