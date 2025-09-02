# Kql Basics

## La structure d'une requête KQL

KQL (Kusto Query Language) est le langage de Sentinel et Log Analytics
Une requête commence par une table source puis des opérateurs |
Exemple : SecurityEvent | where EventID == 4625 | summarize count() by Account

## Opérateur where

where filtre les lignes : where EventID == 4625
Comparateurs : ==, !=, >, <, >=, <=, contains, startswith, endswith
where Account contains "admin" trouve les comptes avec admin dans le nom

