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

