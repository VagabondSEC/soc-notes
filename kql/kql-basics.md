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

## Opérateur mv-expand

mv-expand éclate les listes en lignes
Exemple : ... | mv-expand TargetResource
Nécessaire quand un champ contient un tableau JSON

## Fonctions de temps

TimeGenerated > ago(24h) filtre les dernières 24 heures
bin(TimeGenerated, 1h) arrondit à l'heure pour les graphiques
startofday(), endofday() pour les fenêtres de journée

## Opérateur parse

parse extrait des champs depuis une chaîne structurée
Exemple : parse _RawLog with "user=" User ";ip=" IP
Plus simple et plus rapide que les regex pour les formats fixes

## Opérateur let

let définit des variables et des fonctions
let threshold = 10; ... | where count_ > threshold
let myFunc = (x:int) { x * 2 };
Structure la requête et la rend réutilisable

