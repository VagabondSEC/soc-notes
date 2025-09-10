# Attck Hunting

## Hunting sur T1059 PowerShell

Rechercher les commandes encodées : powershell -enc
Surveiller les scripts avec IEX, Invoke-Expression, DownloadString
Les bloclogs PowerShell (EventID 4104) donnent le script complet

## Hunting sur T1003 LSASS

Accès à lsass.exe par un processus non standard
Sysmon EventID 10 avec TargetImage contenant lsass.exe
Les outils comme mimikatz ouvrent lsass avec des droits de lecture

## Hunting sur T1070 suppression de logs

wevtutil cl, wevtutil clear-log dans les lignes de commande
Clear-EventLog, Remove-EventLog en PowerShell
L'absence soudaine de logs sur une machine = événement en soi

## Hunting sur T1547 registry Run

EventID 13 (registry value set) sur les Run keys
HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Run
HKCU\...\Run et les Startup Approved
Corréler avec la création du fichier exécutable référencé

## Hunting sur T1021 RDP sortant

Logons RDP sortants depuis une machine de bureau
EventID 4624 avec LogonType 10 vers des IP internes
Les connexions RDP multiples depuis un seul compte = pivot probable

