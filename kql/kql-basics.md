# Kql Basics

## La structure d'une requête KQL

KQL (Kusto Query Language) est le langage de Sentinel et Log Analytics
Une requête commence par une table source puis des opérateurs |
Exemple : SecurityEvent | where EventID == 4625 | summarize count() by Account

