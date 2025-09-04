# Wireshark Analysis

## Analyse des flux TCP

Statistics > Conversations pour le top des échanges
Statistics > Endpoints pour les machines les plus actives
Le tri par octets révèle les exfiltrations potentielles

## Export d'objets HTTP

File > Export Objects > HTTP permet de récupérer les fichiers transférés
Permet d'extraire un malware ou un document exfiltré
Vérifier les hash des objets exportés sur VirusTotal

## Détection de scan réseau

Une machine qui envoie des SYN vers beaucoup de ports = scan
Statistics > Flow Graph pour visualiser
tshark -r capture.pcap -Y "tcp.flags.syn==1 and tcp.flags.ack==0"

