# Techniques

## T1059 - Command and Scripting Interpreter

Exécution de commandes via des interpréteurs (cmd, PowerShell, bash, Python).

## Exemple : T1059 - Command and Scripting Interpreter

Détection : surveiller Event ID 4688 (process creation) avec CommandLine contenant powershell.exe -enc

