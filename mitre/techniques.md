# Techniques

## T1059 - Command and Scripting Interpreter

Exécution de commandes via des interpréteurs (cmd, PowerShell, bash, Python).

## Exemple : T1059 - Command and Scripting Interpreter

Détection : surveiller Event ID 4688 (process creation) avec CommandLine contenant powershell.exe -enc

## Cas d'usage : T1059 - Command and Scripting Interpreter

Dans le mapping de détection, Command and Scripting Interpreter sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1059.001 - PowerShell

PowerShell utilisé de manière malveillante, souvent avec encodage.

## Exemple : T1059.001 - PowerShell

Détection : ScriptBlock Logging (Event 4104), Module Logging (4103), commandes -enc, -e, IEX

## Cas d'usage : T1059.001 - PowerShell

Dans le mapping de détection, PowerShell sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1059.003 - Windows Command Shell

cmd.exe utilisé pour exécuter des commandes.

## Exemple : T1059.003 - Windows Command Shell

Détection : 4688 avec cmd.exe /c, chaînes suspectes (whoami, net user, certutil)

## Cas d'usage : T1059.003 - Windows Command Shell

Dans le mapping de détection, Windows Command Shell sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1059.004 - Unix Shell

Shell Unix (bash, sh) pour exécuter des commandes.

## Exemple : T1059.004 - Unix Shell

Détection : auditd execve, EDR sur /bin/sh -c

## Cas d'usage : T1059.004 - Unix Shell

Dans le mapping de détection, Unix Shell sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1059.006 - Python

Python utilisé pour exécuter du code malveillant.

## Exemple : T1059.006 - Python

Détection : python.exe -c, -c exec, pip install depuis des repos suspects

## Cas d'usage : T1059.006 - Python

Dans le mapping de détection, Python sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1059.007 - JavaScript

JavaScript exécuté hors navigateur (Node.js, WScript).

## Exemple : T1059.007 - JavaScript

Détection : wscript.exe, cscript.exe, node.exe avec scripts suspects

## Cas d'usage : T1059.007 - JavaScript

Dans le mapping de détection, JavaScript sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1059.008 - Network Device CLI

CLI d'équipements réseau (routeurs, switches) utilisé par l'attaquant.

## Exemple : T1059.008 - Network Device CLI

Détection : logs AAA, commandes enable, configuration changes

## Cas d'usage : T1059.008 - Network Device CLI

Dans le mapping de détection, Network Device CLI sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1055 - Process Injection

Injection de code dans des processus légitimes.

## Exemple : T1055 - Process Injection

Détection : 4688 + appels API (VirtualAllocEx, WriteProcessMemory, CreateRemoteThread), Sysmon Event 8 (CreateRemoteThread)

## Cas d'usage : T1055 - Process Injection

Dans le mapping de détection, Process Injection sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1055.001 - DLL Injection

Injection d'une DLL dans un processus distant.

## Exemple : T1055.001 - DLL Injection

Détection : Sysmon Event 7 (ImageLoaded) avec DLL inattendue dans un processus

## Cas d'usage : T1055.001 - DLL Injection

Dans le mapping de détection, DLL Injection sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1055.002 - Portable Executable Injection

Injection d'un PE complet dans un processus.

## Exemple : T1055.002 - Portable Executable Injection

Détection : Sysmon Event 8, anomalies de taille mémoire

## Cas d'usage : T1055.002 - Portable Executable Injection

Dans le mapping de détection, Portable Executable Injection sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1055.003 - Thread Execution Hijacking

Détournement de l'exécution d'un thread existant.

## Exemple : T1055.003 - Thread Execution Hijacking

Détection : appels SetThreadContext, SuspendThread sur des processus critiques

## Cas d'usage : T1055.003 - Thread Execution Hijacking

Dans le mapping de détection, Thread Execution Hijacking sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1055.004 - Asynchronous Procedure Call

Injection via APC dans des threads.

## Exemple : T1055.004 - Asynchronous Procedure Call

Détection : QueueUserAPC, Sysmon Event 8

## Cas d'usage : T1055.004 - Asynchronous Procedure Call

Dans le mapping de détection, Asynchronous Procedure Call sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1055.005 - Thread Local Storage

Injection via TLS callbacks.

## Exemple : T1055.005 - Thread Local Storage

Détection : modules avec TLS callbacks modifiés

## Cas d'usage : T1055.005 - Thread Local Storage

Dans le mapping de détection, Thread Local Storage sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1055.008 - Ptrace System Calls

Injection via ptrace sur Linux.

