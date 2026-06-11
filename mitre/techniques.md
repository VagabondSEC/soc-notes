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

## Exemple : T1055.008 - Ptrace System Calls

Détection : auditd avec ptrace, strace sur des processus sensibles

## Cas d'usage : T1055.008 - Ptrace System Calls

Dans le mapping de détection, Ptrace System Calls sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1055.009 - Proc Memory

Injection via /proc/self/mem ou /proc/PID/mem sur Linux.

## Exemple : T1055.009 - Proc Memory

Détection : accès à /proc/*/mem par des processus inattendus

## Cas d'usage : T1055.009 - Proc Memory

Dans le mapping de détection, Proc Memory sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1055.011 - Extra Window Memory Injection

Injection dans la mémoire supplémentaire des fenêtres.

## Exemple : T1055.011 - Extra Window Memory Injection

Détection : appels SetWindowLong, SendMessage avec WM_GETTEXT sur des processus

## Cas d'usage : T1055.011 - Extra Window Memory Injection

Dans le mapping de détection, Extra Window Memory Injection sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1055.012 - Process Hollowing

Remplacement de l'image d'un processus suspendu par du code malveillant.

## Exemple : T1055.012 - Process Hollowing

Détection : 4688 avec parent-suspect, NtUnmapViewOfSection, WriteProcessMemory

## Cas d'usage : T1055.012 - Process Hollowing

Dans le mapping de détection, Process Hollowing sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1055.013 - Process Doppelganging

Processus créé depuis une image NTFS transactionnelle modifiée.

## Exemple : T1055.013 - Process Doppelganging

Détection : TxF (Transaction NTFS), NtCreateTransaction, création de processus depuis des sections

## Cas d'usage : T1055.013 - Process Doppelganging

Dans le mapping de détection, Process Doppelganging sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1055.014 - VDSO Hijacking

Détournement du VDSO Linux (zone mémoire noyau exposée).

## Exemple : T1055.014 - VDSO Hijacking

Détection : modifications de /proc/PID/auxv, EDR kernel

## Cas d'usage : T1055.014 - VDSO Hijacking

Dans le mapping de détection, VDSO Hijacking sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1055.015 - ListPlanting

Injection dans des listes de contrôles (ListView, TreeView).

## Exemple : T1055.015 - ListPlanting

Détection : appels LVM_SETITEMCOUNT, message WM_USER

## Cas d'usage : T1055.015 - ListPlanting

Dans le mapping de détection, ListPlanting sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1055.016 - Memory Mapping

Injection par mappage mémoire partagé.

## Exemple : T1055.016 - Memory Mapping

Détection : CreateFileMapping, MapViewOfFile exécutés en séquence

## Cas d'usage : T1055.016 - Memory Mapping

Dans le mapping de détection, Memory Mapping sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1566 - Phishing

Envoi d'emails malveillants (pièces jointes ou liens).

## Exemple : T1566 - Phishing

Détection : filtrage email, sandboxing des pièces jointes, analyse des URL

## Cas d'usage : T1566 - Phishing

Dans le mapping de détection, Phishing sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1566.001 - Spearphishing Attachment

Pièce jointe malveillante ciblée (Office, PDF, LNK).

## Exemple : T1566.001 - Spearphishing Attachment

Détection : macros Office, OLE objects, documents avec DDE, LNK avec powershell

## Cas d'usage : T1566.001 - Spearphishing Attachment

Dans le mapping de détection, Spearphishing Attachment sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1566.002 - Spearphishing Link

Lien malveillant dans un email ciblé.

## Exemple : T1566.002 - Spearphishing Link

Détection : sandbox URL, vérification des domaines récemment enregistrés, reputation

## Cas d'usage : T1566.002 - Spearphishing Link

Dans le mapping de détection, Spearphishing Link sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1566.003 - Spearphishing via Service

Phishing via des services tiers (LinkedIn, forums).

## Exemple : T1566.003 - Spearphishing via Service

Détection : OSINT, surveillance des fausses identités d'entreprise

## Cas d'usage : T1566.003 - Spearphishing via Service

Dans le mapping de détection, Spearphishing via Service sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1566.004 - Spearphishing Voice

Vishing : appels téléphoniques d'ingénierie sociale.

## Exemple : T1566.004 - Spearphishing Voice

Détection : sensibilisation, procédures de vérification des demandes sensibles

## Cas d'usage : T1566.004 - Spearphishing Voice

Dans le mapping de détection, Spearphishing Voice sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1078 - Valid Accounts

Utilisation de comptes légitimes compromis.

## Exemple : T1078 - Valid Accounts

Détection : anomalies de comportement, horaires inhabituels, géolocalisation, nouvelles permissions

## Cas d'usage : T1078 - Valid Accounts

Dans le mapping de détection, Valid Accounts sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1078.001 - Default Accounts

Comptes par défaut (Guest, Administrator, admin/admin).

## Exemple : T1078.001 - Default Accounts

Détection : audits des comptes par défaut, alertes sur les comptes jamais utilisés

## Cas d'usage : T1078.001 - Default Accounts

Dans le mapping de détection, Default Accounts sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1078.002 - Domain Accounts

Comptes de domaine compromis.

## Exemple : T1078.002 - Domain Accounts

Détection : corrélation logons + activités anormales, impossible travel, rarement utilisés

## Cas d'usage : T1078.002 - Domain Accounts

Dans le mapping de détection, Domain Accounts sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1078.003 - Local Accounts

Comptes locaux compromis.

## Exemple : T1078.003 - Local Accounts

Détection : logons locaux répétés, RDP depuis des IP inconnues

## Cas d'usage : T1078.003 - Local Accounts

Dans le mapping de détection, Local Accounts sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1078.004 - Cloud Accounts

Comptes cloud (Azure AD, AWS IAM) compromis.

## Exemple : T1078.004 - Cloud Accounts

Détection : nouveaux rôles, MFA bypass, logons depuis des IP cloud connues

## Cas d'usage : T1078.004 - Cloud Accounts

Dans le mapping de détection, Cloud Accounts sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1134 - Access Token Manipulation

Manipulation des tokens Windows pour élever les privilèges.

## Exemple : T1134 - Access Token Manipulation

Détection : appels OpenProcessToken, DuplicateToken, ImpersonateLoggedOnUser, SeDebugPrivilege

## Cas d'usage : T1134 - Access Token Manipulation

Dans le mapping de détection, Access Token Manipulation sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1134.001 - Token Impersonation/Theft

Impersonation ou vol de token.

## Exemple : T1134.001 - Token Impersonation/Theft

Détection : appels ImpersonateNamedPipeClient, DuplicateTokenEx, RPCSS

## Cas d'usage : T1134.001 - Token Impersonation/Theft

Dans le mapping de détection, Token Impersonation/Theft sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1134.002 - Create Process with Token

Création d'un processus avec le token d'un autre utilisateur.

## Exemple : T1134.002 - Create Process with Token

Détection : CreateProcessWithTokenW, 4688 avec TokenElevationType

## Cas d'usage : T1134.002 - Create Process with Token

Dans le mapping de détection, Create Process with Token sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1134.003 - Make and Impersonate Token

Création et impersonation de tokens (LogonUser).

## Exemple : T1134.003 - Make and Impersonate Token

Détection : LogonUser avec LOGON32_LOGON_NEW_CREDENTIALS, SeImpersonatePrivilege

## Cas d'usage : T1134.003 - Make and Impersonate Token

Dans le mapping de détection, Make and Impersonate Token sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1134.004 - Parent PID Spoofing

Spoofing du PID parent dans le PEB.

## Exemple : T1134.004 - Parent PID Spoofing

Détection : Sysmon Event 1 avec parent incohérent, 4688 avec ParentProcessId anormal

## Cas d'usage : T1134.004 - Parent PID Spoofing

Dans le mapping de détection, Parent PID Spoofing sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1134.005 - SID-History Injection

Injection de SID dans l'historique SID (migration de domaine).

## Exemple : T1134.005 - SID-History Injection

Détection : Event 4765/4766, comptes avec SIDHistory anormal

## Cas d'usage : T1134.005 - SID-History Injection

Dans le mapping de détection, SID-History Injection sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1547 - Boot or Logon Autostart Execution

Persistance via démarrage automatique au boot/logon.

## Exemple : T1547 - Boot or Logon Autostart Execution

Détection : Run/RunOnce (Event 4688 parent-explorer), services, Startup folder

## Cas d'usage : T1547 - Boot or Logon Autostart Execution

Dans le mapping de détection, Boot or Logon Autostart Execution sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1547.001 - Registry Run Keys

Persistance via les clés Run du registre.

## Exemple : T1547.001 - Registry Run Keys

Détection : Sysmon Event 13 (registry set) sur HKLM\Software\Microsoft\Windows\CurrentVersion\Run

## Cas d'usage : T1547.001 - Registry Run Keys

Dans le mapping de détection, Registry Run Keys sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1547.002 - Startup Folder

Persistance via le dossier Démarrage.

## Exemple : T1547.002 - Startup Folder

Détection : création de fichiers .lnk/.bat dans Startup, Sysmon Event 11

## Cas d'usage : T1547.002 - Startup Folder

Dans le mapping de détection, Startup Folder sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1547.004 - Winlogon Helper DLL

Persistance via les DLL de Winlogon.

## Exemple : T1547.004 - Winlogon Helper DLL

Détection : modification de HKLM\...\Winlogon\Shell, Userinit

## Cas d'usage : T1547.004 - Winlogon Helper DLL

Dans le mapping de détection, Winlogon Helper DLL sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1547.005 - Security Support Provider

Persistance via les SSP (Security Support Providers).

## Exemple : T1547.005 - Security Support Provider

Détection : modification de HKLM\SYSTEM\CurrentControlSet\Control\Lsa\Security Packages

## Cas d'usage : T1547.005 - Security Support Provider

Dans le mapping de détection, Security Support Provider sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1547.006 - Kernel Modules and Extensions

Persistance via modules noyau Linux (LKM).

## Exemple : T1547.006 - Kernel Modules and Extensions

Détection : lsmod, /proc/modules, modprobe, DKMS

## Cas d'usage : T1547.006 - Kernel Modules and Extensions

Dans le mapping de détection, Kernel Modules and Extensions sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1547.009 - Shortcut Modification

Persistance via modification de raccourcis .lnk.

## Exemple : T1547.009 - Shortcut Modification

Détection : Sysmon Event 11, modifications de .lnk vers des cibles inhabituelles

## Cas d'usage : T1547.009 - Shortcut Modification

Dans le mapping de détection, Shortcut Modification sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1547.010 - Port Monitors

Persistance via les port monitors d'impression.

## Exemple : T1547.010 - Port Monitors

Détection : modification de HKLM\...\Print\Monitors, DLL dans System32

## Cas d'usage : T1547.010 - Port Monitors

Dans le mapping de détection, Port Monitors sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1547.012 - Print Processors

Persistance via les print processors.

## Exemple : T1547.012 - Print Processors

Détection : clé HKLM\...\Control\Print\Environments\Windows x64\Print Processors

## Cas d'usage : T1547.012 - Print Processors

Dans le mapping de détection, Print Processors sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1547.013 - XDG Autostart Entries

Persistance via .desktop sur Linux (autostart).

## Exemple : T1547.013 - XDG Autostart Entries

Détection : fichiers .desktop dans ~/.config/autostart, /etc/xdg/autostart

## Cas d'usage : T1547.013 - XDG Autostart Entries

Dans le mapping de détection, XDG Autostart Entries sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1547.014 - Active Setup

Persistance via Active Setup (exécuté au logon).

## Exemple : T1547.014 - Active Setup

Détection : HKLM\SOFTWARE\Microsoft\Active Setup\Installed Components

## Cas d'usage : T1547.014 - Active Setup

Dans le mapping de détection, Active Setup sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1547.015 - Login Items

Persistance via les Login Items macOS.

## Exemple : T1547.015 - Login Items

Détection : com.apple.loginitems.plist, ~/Library/LaunchAgents

## Cas d'usage : T1547.015 - Login Items

Dans le mapping de détection, Login Items sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1543 - Create or Modify System Process

Création ou modification de services/démons pour la persistance.

## Exemple : T1543 - Create or Modify System Process

Détection : Event 7045 (nouveau service), sc.exe create, systemctl

## Cas d'usage : T1543 - Create or Modify System Process

Dans le mapping de détection, Create or Modify System Process sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1543.001 - Launch Agent

Persistance macOS via LaunchAgents/LaunchDaemons.

## Exemple : T1543.001 - Launch Agent

Détection : plist dans ~/Library/LaunchAgents, /Library/LaunchDaemons

## Cas d'usage : T1543.001 - Launch Agent

Dans le mapping de détection, Launch Agent sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1543.003 - Windows Service

Création d'un service Windows malveillant.

## Exemple : T1543.003 - Windows Service

Détection : Event 7045, instsrv, sc create, les binaires de service dans des chemins bizarres

## Cas d'usage : T1543.003 - Windows Service

Dans le mapping de détection, Windows Service sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1543.004 - Unix Init Process

Persistance via init.d, systemd, rc.local sur Linux.

## Exemple : T1543.004 - Unix Init Process

Détection : nouveaux fichiers dans /etc/init.d, /etc/systemd/system, systemctl enable

## Cas d'usage : T1543.004 - Unix Init Process

Dans le mapping de détection, Unix Init Process sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1546 - Event Triggered Execution

Persistance via des déclencheurs d'événements (WMI, Image File Execution Options...).

## Exemple : T1546 - Event Triggered Execution

Détection : modification de clés de registre de déclenchement, WMI subscriptions

## Cas d'usage : T1546 - Event Triggered Execution

Dans le mapping de détection, Event Triggered Execution sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1546.001 - Change Default File Association

Modification de l'association de fichiers par défaut.

## Exemple : T1546.001 - Change Default File Association

Détection : HKCR (UserChoice), Sysmon Event 13

## Cas d'usage : T1546.001 - Change Default File Association

Dans le mapping de détection, Change Default File Association sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1546.002 - Screensaver

Persistance via l'économiseur d'écran.

## Exemple : T1546.002 - Screensaver

Détection : HKLM\...\Control Panel\Desktop\SCRNSAVE.EXE, SCRNSAVE.exe pointant ailleurs

## Cas d'usage : T1546.002 - Screensaver

Dans le mapping de détection, Screensaver sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1546.003 - WMI Event Subscription

Persistance via les abonnements aux événements WMI.

## Exemple : T1546.003 - WMI Event Subscription

Détection : \.\root\subscription, Event 5857, wmic /namespace:\\root\subscription

## Cas d'usage : T1546.003 - WMI Event Subscription

Dans le mapping de détection, WMI Event Subscription sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1546.004 - Unix Shell Configuration

Persistance via .bashrc, .profile, .bash_profile.

## Exemple : T1546.004 - Unix Shell Configuration

Détection : modifications récentes de fichiers dot, contenu suspect

## Cas d'usage : T1546.004 - Unix Shell Configuration

Dans le mapping de détection, Unix Shell Configuration sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1546.005 - Trap

Persistance via les traps shell (bash trap).

## Exemple : T1546.005 - Trap

Détection : trap dans les scripts système, auditd

## Cas d'usage : T1546.005 - Trap

Dans le mapping de détection, Trap sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1546.007 - Netsh Helper DLL

Persistance via les helper DLL de netsh.

## Exemple : T1546.007 - Netsh Helper DLL

Détection : HKLM\...\Netsh\HelperDLLs, netsh add helper

## Cas d'usage : T1546.007 - Netsh Helper DLL

Dans le mapping de détection, Netsh Helper DLL sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1546.008 - Accessibility Features

Persistance via les fonctionnalités d'accessibilité (sethc, utilman).

## Exemple : T1546.008 - Accessibility Features

Détection : modification de Image File Execution Options pour sethc.exe, utilman.exe

## Cas d'usage : T1546.008 - Accessibility Features

Dans le mapping de détection, Accessibility Features sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1546.009 - AppInit DLLs

Persistance via les AppInit_DLLs.

## Exemple : T1546.009 - AppInit DLLs

Détection : HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Windows\AppInit_DLLs

## Cas d'usage : T1546.009 - AppInit DLLs

Dans le mapping de détection, AppInit DLLs sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1546.010 - AppCert DLLs

Persistance via AppCertDLLs (chargées au processus).

## Exemple : T1546.010 - AppCert DLLs

Détection : HKLM\SYSTEM\CurrentControlSet\Control\Session Manager\AppCertDLLs

## Cas d'usage : T1546.010 - AppCert DLLs

Dans le mapping de détection, AppCert DLLs sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1546.011 - Application Shimming

Persistance via les Application Shims.

## Exemple : T1546.011 - Application Shimming

Détection : sdbinst.exe, clés de registre de shim, Event 4688 avec sdbinst

## Cas d'usage : T1546.011 - Application Shimming

Dans le mapping de détection, Application Shimming sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

## T1546.012 - Image File Execution Options

Persistance via IFEO (Debugger).

## Exemple : T1546.012 - Image File Execution Options

Détection : HKLM\...\Image File Execution Options\<exe>\Debugger

## Cas d'usage : T1546.012 - Image File Execution Options

Dans le mapping de détection, Image File Execution Options sert de référence pour identifier les lacunes de couverture. On le confronte aux règles Sigma et aux requêtes SIEM existantes pour prioriser les améliorations de détection.

