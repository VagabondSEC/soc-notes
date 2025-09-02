# Kql Basics

## La structure d'une requête KQL

KQL (Kusto Query Language) est le langage de Sentinel et Log Analytics
Une requête commence par une table source puis des opérateurs |
Exemple : SecurityEvent | where EventID == 4625 | summarize count() by Account

## Opérateur where

where filtre les lignes : where EventID == 4625
Comparateurs : ==, !=, >, <, >=, <=, contains, startswith, endswith
where Account contains "admin" trouve les comptes avec admin dans le nom

## Opérateur summarize

summarize agrège : summarize count() by Account
Fonctions : count(), dcount(), sum(), avg(), min(), max(), make_set(), make_list()
make_set(IPAddress) liste les IP uniques d'un compte

## Opérateur extend

extend crée des colonnes calculées
Exemple : ... | extend Risk = case(Account contains "admin", "high", "low")
Utile pour calculer des scores ou normaliser des champs

## Opérateur project

project sélectionne les colonnes : project TimeGenerated, Account, IPAddress
project-away supprime des colonnes
project-rename renomme une colonne

## Opérateur join

join fusionne deux tables sur une clé
SecurityEvent | join kind=inner (SigninLogs) on Account
kind=leftouter garde toutes les lignes de gauche
Attention aux doublons : toujours tester avec des données réelles

## Opérateur union

union combine plusieurs tables : union SecurityEvent, WindowsEvent
withsource=TableName ajoute la table d'origine
Utile pour chercher sur plusieurs sources de logs

## Opérateur top

top 10 by count_ desc prend les 10 plus gros
Exemple : ... | summarize count() by Account | top 10 by count_

