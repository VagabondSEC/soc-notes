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

## Tactique Persistence (TA0003)

T1547 Boot or Logon Autostart Execution (registry Run, startup folder)
T1053 Scheduled Task : très utilisé par les malwares
T1543 Create or Modify System Process (services)
Détecter : surveiller les modifications de Run keys (EventID 13)

## Tactique Privilege Escalation (TA0004)

T1068 Exploitation for Privilege Escalation
T1078 Valid Accounts avec des droits admin
T1548 Abuse Elevation Control Mechanism (UAC bypass)
Le pass-the-hash et l'exploitation de tokens sont les classiques

## Tactique Defense Evasion (TA0005)

T1027 Obfuscated Files or Information
T1112 Modify Registry
T1070 Indicator Removal : effacer les logs (wevtutil cl)
T1562 Impair Defenses : désactiver l'EDR ou Windows Defender

## Tactique Credential Access (TA0006)

T1003 OS Credential Dumping (LSASS, mimikatz)
T1558 Steal or Forge Kerberos Tickets (Golden/Silver ticket)
T1110 Brute Force
Surveiller l'accès à lsass.exe (EventID 10 de Sysmon)

## Tactique Discovery (TA0007)

T1083 File and Directory Discovery
T1057 Process Discovery (tasklist, Get-Process)
T1018 Remote System Discovery (net view, ping sweep)
Les commandes de discovery sont souvent le premier bruit après compromission

## Tactique Lateral Movement (TA0008)

T1021 Remote Services (SMB, RDP, WinRM)
T1550 Use Alternate Authentication Material (pass-the-hash)
T1570 Lateral Tool Transfer
Les logons de type 3 et 10 vers de nouvelles machines sont les indicateurs

## Tactique Collection (TA0009)

T1005 Data from Local System
T1114 Email Collection (dumping des boîtes mail)
T1560 Archive Collected Data (zip avant exfiltration)
La création de zip sur des données sensibles est un signal

## Tactique Command and Control (TA0011)

T1071 Application Layer Protocol (HTTP, HTTPS, DNS)
T1573 Encrypted Channel
T1090 Proxy (utilisation de la machine comme pivot)
Les connexions sortantes régulières vers des domaines récents = signal

## Tactique Exfiltration (TA0010)

T1041 Exfiltration Over C2 Channel
T1048 Exfiltration Over Alternative Protocol (DNS, HTTP vers IP)
T1567 Exfiltration Over Web Service (pastebin, transfer.sh)
Le volume sortant anormal reste le meilleur indicateur

## Tactique Impact (TA0040)

T1486 Data Encrypted for Impact (ransomware)
T1489 Service Stop
T1490 Inhibit System Recovery (suppression des shadow copies)
vssadmin delete shadows est une commande à alerter immédiatement

