# Soc Level1

## Parcours SOC Level 1

TryHackMe propose un parcours SOC Level 1 structuré
Il couvre les fondamentaux : cyber defense, SIEM, phishing, log analysis
Le parcours combine des rooms théoriques et des challenges pratiques
Objectif : maîtriser le tri d'alertes dans un environnement simulé

## Room : Intro to SIEM

Comprendre le rôle du SIEM : collecte, normalisation, corrélation, alertes
Les composants : agents, collecteurs, moteur de corrélation, dashboard
Splunk, Elastic et Wazuh vus en pratique

## Room : Benign or Malicious

Analyse de fichiers et de flux pour décider si un événement est malveillant
Vérifier les hash sur VirusTotal et les bases de IOC
Analyser le comportement : où le fichier se lance, que contacte-t-il

## Room : Phishing Analysis

Analyser un email de phishing : en-têtes, SPF, DKIM, DMARC
Extraire les liens et vérifier les domaines
Analyser les pièces jointes dans un environnement isolé
Les en-têtes X-Originating-IP et Received trahissent le vrai expéditeur

## Room : Wireshark 101

Prendre et analyser une capture réseau
Filtres d'affichage et suivi de flux
Reconnaître les protocoles : HTTP, DNS, TCP, TLS

## Room : Splunk Basics

Recherche, time range, champs, sourcetypes
Les commandes essentielles : table, stats, timechart, eval
Construire un dashboard simple de monitoring

## Room : Network Security

Modèles OSI et TCP/IP, les attaques réseau classiques
ARP spoofing, MITM, SYN flood
Les défenses : segmentation, filtrage, inspection

