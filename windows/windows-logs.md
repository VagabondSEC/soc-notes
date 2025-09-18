# Windows Logs

## Les logs Windows essentiels

Security : authentifications, droits, politique (4624, 4625, 4720...)
System : services, drivers, erreurs système
Application : logs applicatifs (crash, erreurs)
PowerShell (4104) : scripts exécutés avec bloclog
Sysmon : la couche de visibilité supplémentaire

## EventID 4624 et 4625

4624 : ouverture de session réussie
4625 : échec d'ouverture de session
Les LogonType : 2 interactif, 3 réseau, 4 batch, 5 service, 9 délégué, 10 RDP
Un 4625 suivi d'un 4624 sur le même compte = brute force réussi

