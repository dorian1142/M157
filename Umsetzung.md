# Umsetzungsdokumentation

In dieser Dokumenation wird die Umsetzung sowie das Testkonzept des Projekts festgehalten.

## Umsetzung
Der Start war sehr holprig. Ich hatte grosse Schwierigkeiten Fassung im Thema Docker Swarm zu finden, da es für mich ein komplett neues Thema war. Ich habe zu Beginn ebenfalls nicht verstanden, wie ich vorgehen muss, um eine Swarm Umgebung zu kreiieren. Deshalb entstand auch der eher zynisch gemeinte Arbeitsjournaleintrag des 14. Januars.

Nachdem ich mich weitgehend informiert habe, habe ich es nach 100 mal versuchen doch geschafft. Ich habe 3 Linux Ubuntu VMs auf meinem Hyper V Hypervisor erstellt und mit einer statischen IP Adresse konfiguriert. 

### Übersicht

| Node | manager | worker1 | worker2 |
| ------------- | ------------- | ------------- | ------------- |
| IP Adresse || Bereits vorhanden | Bereits vorhanden |
| User | Docker Software | Kostenlos | Bereits vorhanden |  
| CPU | Oracle Virtualbox Software | Kostenlos  | Bereits vorhanden |
| RAM | GitHub (zur Dokumentablage)  | Kostenlos | Bereits vorhanden |
| Festplatte | Aufwand  | 100.- CHF / Stunde | Bereits vorhanden |
