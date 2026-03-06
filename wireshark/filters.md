# Filters

## ip.addr

Filtre par adresse IP (source ou destination).

## Exemple : ip.addr

ip.addr == 192.168.1.10

## Cas d'usage : ip.addr

Sur une capture réseau, ip.addr permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## ip.src

Filtre par IP source.

## Exemple : ip.src

ip.src == 10.0.0.5

## Cas d'usage : ip.src

Sur une capture réseau, ip.src permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## ip.dst

Filtre par IP destination.

## Exemple : ip.dst

ip.dst == 8.8.8.8

## Cas d'usage : ip.dst

Sur une capture réseau, ip.dst permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## ip.ttl

Filtre par TTL (détection d'OS fingerprinting).

## Exemple : ip.ttl

ip.ttl <= 64

## Cas d'usage : ip.ttl

Sur une capture réseau, ip.ttl permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## ip.proto

Filtre par protocole IP (6=TCP, 17=UDP, 1=ICMP).

## Exemple : ip.proto

ip.proto == 6

## Cas d'usage : ip.proto

Sur une capture réseau, ip.proto permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.port

Filtre par port TCP (source ou destination).

## Exemple : tcp.port

tcp.port == 443

## Cas d'usage : tcp.port

Sur une capture réseau, tcp.port permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.srcport

Filtre par port TCP source.

## Exemple : tcp.srcport

tcp.srcport == 4444

## Cas d'usage : tcp.srcport

Sur une capture réseau, tcp.srcport permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.dstport

Filtre par port TCP destination.

## Exemple : tcp.dstport

tcp.dstport == 22

## Cas d'usage : tcp.dstport

Sur une capture réseau, tcp.dstport permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.flags.syn

Paquets avec flag SYN (début de connexion).

## Exemple : tcp.flags.syn

tcp.flags.syn == 1

## Cas d'usage : tcp.flags.syn

Sur une capture réseau, tcp.flags.syn permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.flags.ack

Paquets avec flag ACK.

## Exemple : tcp.flags.ack

tcp.flags.ack == 1

## Cas d'usage : tcp.flags.ack

Sur une capture réseau, tcp.flags.ack permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.flags.reset

Paquets avec flag RST (connexion reset).

## Exemple : tcp.flags.reset

tcp.flags.reset == 1

## Cas d'usage : tcp.flags.reset

Sur une capture réseau, tcp.flags.reset permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.flags.fin

Paquets avec flag FIN (fin de connexion).

## Exemple : tcp.flags.fin

tcp.flags.fin == 1

## Cas d'usage : tcp.flags.fin

Sur une capture réseau, tcp.flags.fin permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.flags.push

Paquets avec flag PSH.

## Exemple : tcp.flags.push

tcp.flags.push == 1

## Cas d'usage : tcp.flags.push

Sur une capture réseau, tcp.flags.push permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.stream

Filtre par flux TCP (numéro de stream).

## Exemple : tcp.stream

tcp.stream eq 42

## Cas d'usage : tcp.stream

Sur une capture réseau, tcp.stream permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.seq

Filtre par numéro de séquence.

## Exemple : tcp.seq

tcp.seq == 1000

## Cas d'usage : tcp.seq

Sur une capture réseau, tcp.seq permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.window_size

Filtre par taille de fenêtre (anomalies).

## Exemple : tcp.window_size

tcp.window_size < 1024

## Cas d'usage : tcp.window_size

Sur une capture réseau, tcp.window_size permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.analysis.flags

Paquets avec des problèmes d'analyse (retransmissions...).

## Exemple : tcp.analysis.flags

tcp.analysis.flags

## Cas d'usage : tcp.analysis.flags

Sur une capture réseau, tcp.analysis.flags permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.analysis.retransmission

Retransmissions TCP.

## Exemple : tcp.analysis.retransmission

tcp.analysis.retransmission

## Cas d'usage : tcp.analysis.retransmission

Sur une capture réseau, tcp.analysis.retransmission permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.analysis.zero_window

Fenêtre zéro (hôte submergé).

## Exemple : tcp.analysis.zero_window

tcp.analysis.zero_window

## Cas d'usage : tcp.analysis.zero_window

Sur une capture réseau, tcp.analysis.zero_window permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.analysis.duplicate_ack

ACK dupliqués (perte de paquets).

## Exemple : tcp.analysis.duplicate_ack

tcp.analysis.duplicate_ack

## Cas d'usage : tcp.analysis.duplicate_ack

Sur une capture réseau, tcp.analysis.duplicate_ack permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## udp.port

Filtre par port UDP.

## Exemple : udp.port

udp.port == 53

## Cas d'usage : udp.port

Sur une capture réseau, udp.port permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## udp.length

Filtre par longueur UDP.

## Exemple : udp.length

udp.length > 1000

