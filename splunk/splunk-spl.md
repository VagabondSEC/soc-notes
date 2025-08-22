# Splunk Spl

## Commande table

table affiche les champs en colonnes
Exemple : index=linux sourcetype=secure | table _time src_ip user command
Utiliser table en fin de pipeline pour la lisibilité

## Commande stats

stats agrège par groupe : stats count by src_ip
Fonctions : count, dc (distinct count), sum, avg, min, max, values, earliest, latest
Exemple : index=windows EventCode=4625 | stats count by Account
stats count by host, sourcetype donne un tableau multi-dimensions

## Commande timechart

timechart fait un stats par intervalle de temps
Exemple : index=main | timechart count by action
span=1h, span=1d ajuste la granularité
timechart count par source permet de repérer des pics d'activité

## Commande eval

eval crée ou modifie un champ avec une expression
Exemple : ... | eval risk_score = if(match(src_ip, "^10\\."), 20, 50)
Fonctions utiles : if, case, tonumber, tostring, lower, upper, strlen, replace
eval permet les calculs de score de risque maison

## Commande where

where filtre sur une expression évaluée (différent de search)
Exemple : ... | where risk_score > 30
where accepte les comparaisons numériques et les regex
search en début de pipeline, where pour les champs calculés

## Commande dedup

dedup supprime les événements en double sur un champ
Exemple : index=windows EventCode=4624 | dedup Account
dedup 5 Account garde les 5 premières occurrences par compte
Utile pour lister les utilisateurs uniques d'une connexion

## Commande transaction

transaction regroupe des événements liés par des champs communs
Exemple : index=windows | transaction UserName startswith=EventCode=4624 endswith=EventCode=4634
Attention : transaction est gourmand, préférer stats values quand possible
Utile pour reconstituer une session complète

