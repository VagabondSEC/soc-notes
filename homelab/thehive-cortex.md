# Thehive Cortex

## TheHive pour la gestion d'incidents

TheHive est un outil open source de case management (SOC)
Chaque incident devient un case avec des tâches et des observables
Les observables (hash, IP, domaines) alimentent les analyses
L'API REST permet d'automatiser la création de cases

## Cortex pour l'enrichissement

Cortex exécute des analyseurs sur les observables
VirusTotal, AbuseIPDB, Urlhaus, Shodan en analyseurs
Un hash envoyé à Cortex revient avec les verdicts des sandbox
TheHive et Cortex dialoguent via l'API

## Le workflow TheHive

Création du case depuis une alerte SIEM
Ajout des observables et lancement des analyseurs Cortex
Tâches d'investigation assignées aux analystes
Clôture avec le statut, la sévérité et le rapport

