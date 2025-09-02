# Kql Sentinel

## Hunting dans Sentinel

Les requêtes de hunting se lancent depuis l'onglet Hunting
Chaque requête a un kill chain stage et une tactique MITRE ATT&CK
Les résultats peuvent être bookmarked et transformés en alertes

## Requête échecs de connexion

SigninLogs | where ResultType == "50057" | summarize count() by UserPrincipalName
Les échecs répétés sur un compte = candidat brute force
Corréler avec les succès juste après (ResultType == 0)

