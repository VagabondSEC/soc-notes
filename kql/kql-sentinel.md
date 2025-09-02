# Kql Sentinel

## Hunting dans Sentinel

Les requêtes de hunting se lancent depuis l'onglet Hunting
Chaque requête a un kill chain stage et une tactique MITRE ATT&CK
Les résultats peuvent être bookmarked et transformés en alertes

## Requête échecs de connexion

SigninLogs | where ResultType == "50057" | summarize count() by UserPrincipalName
Les échecs répétés sur un compte = candidat brute force
Corréler avec les succès juste après (ResultType == 0)

## Requête comptes sensibles

SecurityEvent | where AccountType == "User" and Account contains "admin"
Suivre les modifications des groupes privilégiés (EventID 4728, 4732)
Alertes sur l'ajout d'un membre à Domain Admins

## Requête PowerShell suspect

SecurityEvent | where EventID == 4104 | where ScriptBlockText contains "IEX"
Détecter les download cradle : IEX (New-Object Net.WebClient).DownloadString
Corréler avec les processus parents (EventID 4688 avec ParentProcessName)

## Requête mouvements latéraux

Event 4624 LogonType 3 depuis des machines sensibles
Event 4624 LogonType 9 (NewCredentials) souvent utilisé pour le pass-the-hash
Corréler les connexions réseau avec les authentifications

