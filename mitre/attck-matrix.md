# Attck Matrix

## La matrice ATT&CK

MITRE ATT&CK est une base de connaissances des tactiques et techniques adverses
Tactiques : Reconnaissance, Initial Access, Execution, Persistence, ...
Chaque technique a un ID (ex : T1059 Command and Scripting Interpreter)
C'est le langage commun entre les équipes SOC et les threat intel

## Tactique Reconnaissance (TA0043)

T1592 Gather Victim Host Information
T1595 Active Scanning : scan des ports et services
Les scans répétés depuis une IP = signal de préparation

## Tactique Initial Access (TA0001)

T1190 Exploit Public-Facing Application
T1566 Phishing : le vecteur le plus utilisé
T1078 Valid Accounts : utiliser des comptes volés
La surveillance des logins réussis anormaux couvre T1078

## Tactique Execution (TA0002)

T1059 Command and Scripting Interpreter (PowerShell, cmd, bash)
T1204 User Execution : le malware exécuté par l'utilisateur
T1053 Scheduled Task/Job pour l'exécution planifiée
Les logs 4688 (process creation) sont la clé de cette tactique

