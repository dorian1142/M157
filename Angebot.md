# Angebot Docker Swarm as a Service M157

## Inhaltsverzeichnis

[Einleitung](#Einleitung)  
[Lösungsbeschrieb](#Lösungsbeschrieb)  
[Mengengerüst](#Mengengerüst)  
[Planung](#Planung)  
[Risikoanalyse](#Risikoanalyse)  

<a name="Einleitung"/>
<a name="Lösungsbeschrieb"/>
<a name="Mengengerüst"/>
<a name="Planung"/>
<a name="Risikoanalyse"/>

## Einleitung

| Input  | Output |
| ------------- | ------------- |
| Auftraggeber  | PowerDataCenter AG  |
| Auftragnehmer  | Dorian Jungi  |  
| Beginndatum  | 26.11.2020  |
| Abgabedatum  | 19.01.2021  |

### Problemstellung

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
- Service muss unterbruchsfrei laufen
> Der Cluster wird auf einer Umgebung aufgesetzt, welche rund um die Uhr verfügbar ist. 

## Mengengerüst

Zur Umsetzung der Lösung durch den Auftragnehmer werden folgende Hardware und Software verwendet:

| Stückzahl | Produkt | Kosten |
| ------------- | ------------- | ------------- |
| 1x | HP Elitebook 840 G3 (16GB RAM, 2 Core CPU) | Kostenlos |
| 1x | Docker Software | Kostenlos |  
| 1x | Oracle Virtualbox Software | Kostenlos  |
| 1x | GitHub (zur Dokumentablage)  | Kostenlos |
| 16 Stunden | Aufwand  | 50.- CHF / Stunde |


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

