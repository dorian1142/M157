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

Als erstes musste ich Docker auf allen VMs installieren. Nach dem installieren habe ich den Standard Docker Hello World Befehl ausgeführt. Anschliessend habe ich mit dem Aufsetzen des Swarms begonnen. Um den Swarm zu erstellen, muss man auf dem Node, welchen man als Manager verwenden will, folgenden Befehl eingeben: `docker swarm init --advertise-addr 192.168.10.10`. So war auch schon der manager erstellt. Um mehrere Nodes noch hinzufügen zu können, muss man im worker Node den folgenden Befehl eingeben:

![no](https://github.com/dorian1142/M157/blob/main/swarmtoken.PNG)

Diesen Befehl habe ich auf beiden worker VMs ausgeführt und beide funktionierten einwandfrei:

![no](https://github.com/dorian1142/M157/blob/main/worker1join.PNG)

![no](https://github.com/dorian1142/M157/blob/main/worker2join.PNG)

Als Kontrolle habe ich auf dem manager node noch den Befehl `docker node ls` ausgeführt um zu sehen, ob die beiden workers erkannt wurden.

![no](https://github.com/dorian1142/M157/blob/main/nodes.PNG)

Wie man auf dem Bild erkennen kann, hat es funktioniert. Der nächste Schritt bestand darin, eine Applikation (vorzugsweise Python) auf einen Node zu bringen, was leider nicht funktioniert hat. Ich habe versucht, das Problem zu beheben und habe viel recherchiert, jedoch habe ich keine Lösung gefunden.

![no](https://github.com/dorian1142/M157/blob/main/fail.PNG)

## Testkonzept

Als letzten Teil des Projekts, wurde noch ein Testprotokoll durchgeführt mit einigen Testszenarien.