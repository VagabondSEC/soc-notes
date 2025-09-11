# Soc Fundamentals

## Le parcours LetsDefend

LetsDefend simule un SOC avec un vrai SIEM (Elastic) et des alertes réelles
Le parcours SOC Analyst couvre le tri d'alertes de bout en bout
Chaque alerte doit être analysée, classée et documentée
Le format : analyste -> investigate -> contain -> report

## Le workflow de tri d'alerte

1. Lire l'alerte et les artefacts associés
2. Valider la malveillance (hash, IP, comportement)
3. Déterminer la portée (machine, user, réseau)
4. Classer : True Positive, False Positive, Benign
5. Documenter et recommander des actions

## Les emails malveillants

Analyser les pièces jointes : type, hash, macros
Les macros Office restent le vecteur n1 des malwares
Vérifier les liens avec des services de sandbox (Any.Run, Hybrid Analysis)

## L'analyse de processus

Identifier les processus anormaux dans les logs
Les chemins d'installation étranges (Temp, AppData, ProgramData)
Les processus légitimes qui tournent depuis des chemins suspects

## Les connexions réseau suspectes

Les connexions sortantes vers des IP inconnues
Les protocoles inhabituels sur des ports standards
Les domaines récemment enregistrés (WHOIS, urlhaus)

## Les faux positifs les plus courants

Les scans de vulnérabilités internes (Nessus, Qualys)
Les mises à jour Windows et les downloads Microsoft
Les outils de monitoring (ping, SNMP)
Connaître son environnement = savoir ignorer le bruit légitime

