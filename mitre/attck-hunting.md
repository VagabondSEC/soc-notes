# Attck Hunting

## Hunting sur T1059 PowerShell

Rechercher les commandes encodées : powershell -enc
Surveiller les scripts avec IEX, Invoke-Expression, DownloadString
Les bloclogs PowerShell (EventID 4104) donnent le script complet

## Hunting sur T1003 LSASS

Accès à lsass.exe par un processus non standard
Sysmon EventID 10 avec TargetImage contenant lsass.exe
Les outils comme mimikatz ouvrent lsass avec des droits de lecture

