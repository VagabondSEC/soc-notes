# Filters

## ip.addr

Filtre par adresse IP (source ou destination).

## Exemple : ip.addr

ip.addr == 192.168.1.10

## Cas d'usage : ip.addr

Sur une capture réseau, ip.addr permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## ip.src

Filtre par IP source.

