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

