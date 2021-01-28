# Umsetzungsdokumentation

In dieser Dokumenation wird die Umsetzung sowie das Testkonzept des Projekts festgehalten.

## Umsetzung
Der Start war sehr holprig. Ich hatte grosse Schwierigkeiten Fassung im Thema Docker Swarm zu finden, da es für mich ein komplett neues Thema war. Ich habe zu Beginn ebenfalls nicht verstanden, wie ich vorgehen muss, um eine Swarm Umgebung zu kreiieren. Deshalb entstand auch der eher zynisch gemeinte Arbeitsjournaleintrag des 14. Januars.

Nachdem ich mich weitgehend informiert habe, habe ich es nach 100 mal versuchen doch geschafft. Ich habe 3 Linux Ubuntu VMs auf meinem Hyper V Hypervisor erstellt und mit einer statischen IP Adresse konfiguriert. Im Angebotsdokument habe ich notiert, dass ich Oracle Virtualbox als Hypervisor verwenden werde, dies hat leider so oft nicht funktioniert, dass ich schlussendlich auf VMWare Player umgestiegen bin. Dies hat dann genauso wenig funktioniert, weshalb ich als dritte und schlussendlich funktionierende Lösung Hyper V verwendet habe.

### Übersicht

| Node | manager | worker1 | worker2 |
| ------------- | ------------- | ------------- | ------------- |
| Hostname | manager | worker1 | worker2 |
| IP Adresse | 192.168.10.10| 192.168.10.20 | 192.168.10.30 |
| User | karen | ivan | ivan |  
| CPU | 1 CPU | 1 CPU | 1 CPU |
| RAM | 1GB | 1GB | 1GB |
| Festplatte | 20GB | 20GB | 20GB |
