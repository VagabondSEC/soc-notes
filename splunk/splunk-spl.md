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

