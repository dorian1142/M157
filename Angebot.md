# Angebot Docker Swarm as a Service M157

## Inhaltsverzeichnis

[Einleitung](#Einleitung)  
[Lösungsbeschrieb](#Lösungsbeschrieb)  
[Mengengerüst](#Mengengerüst)  

<a name="Einleitung"/>
<a name="Lösungsbeschrieb"/>
<a name="Mengengerüst"/>

## Einleitung

| Input  | Output |
| ------------- | ------------- |
| Auftraggeber  | PowerDataCenter AG  |
| Auftragnehmer  | Dorian Jungi  |  
| Beginndatum  | 26.11.2020  |
| Abgabedatum  | 19.01.2021  |

### Problemstellung

> Die PowerDataCenter AG ist bereits Kunde des Auftragnehmers und mietet bereits eine Virtuelle Infrastruktur. Diese gelangt langsam an ihre Kapazitätsgrenzen. Nun möchte die PDC AG ihre Ressourcen auf eine andere Weise vergrössern. Die PDC AG möchte mit Docker weiterarbeiten, da Docker ressourcenschonender als Hypervisor-Infrastrukturen laufen kann und einfacher zu managen ist.

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

| Produkt | Kosten |
| ------------- | ------------- |
| HP Elitebook 840 G3 (16GB RAM, 2 Core CPU) | Kostenlos |
| Docker  | Kostenlos |  
| Oracle Virtualbox  | Kostenlos  |
| GitHub (zur Dokumentablage)  | Kostenlos |
| Aufwand  | 50.- CHF / Stunde |


Da der Auftragnehmer bereits über die benötigte Hardware verfügt, muss diese nicht mehr bezahlt werden und ist ebenfalls kostenlos.

