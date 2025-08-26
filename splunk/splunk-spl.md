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

## Commande rex

rex extrait des champs par regex
Exemple : ... | rex field=_raw "(?<ip>\d+\.\d+\.\d+\.\d+)"
rex mode=sed permet de remplacer du texte dans un champ
L'extraction inline évite de dépendre d'extraire un champ complet

## Commande lookup

lookup enrichit les événements avec une table externe
Exemple : ... | lookup asset_inventory ip OUTPUT owner, criticality
Les lookups sont définis dans Settings > Lookups
Enrichir avec le propriétaire d'un asset aide au tri des alertes

## Commande fields

fields + liste les champs à garder, fields - liste ceux à retirer
Exemple : ... | fields + src_ip, dest_ip, user
Réduire les champs accélère les recherches sur gros volumes
Utile avant un outputlookup ou un export

## Commande inputlookup / outputlookup

inputlookup lit une table CSV, outputlookup l'écrit
Exemple : ... | outputlookup suspicious_ips.csv
Permet de maintenir des listes de IOC maison
Combiner avec append pour enrichir une liste existante

## Commande sort

sort trie les résultats : sort -count (desc), sort +count (asc)
Exemple : ... | stats count by src_ip | sort - count
sort limit=10 ne garde que les 10 premiers

## Commande head / tail

head 10 garde les 10 premiers événements
tail 10 garde les 10 derniers
Exemple : index=windows EventCode=4625 | head 5

## Commande map

map exécute une sous-recherche pour chaque résultat
Très lent, à utiliser avec parcimonie
Exemple : ... | map search="search index=main src_ip=$src_ip$"

## Commande eventstats

eventstats calcule des stats SANS supprimer les événements
Exemple : ... | eventstats count by user
Utile pour compter les occurrences sans perdre le détail

