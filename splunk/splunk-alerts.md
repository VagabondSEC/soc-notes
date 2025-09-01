# Splunk Alerts

## Types d'alertes

Par événement : déclenchée à chaque résultat
Par résultat : une fois par fenêtre de recherche
Par intervalle : à chaque exécution planifiée si la condition est vraie

## Throttling

Le throttling évite les alertes en rafale
Exemple : ne pas re-alerter sur le même src_ip pendant 1h
Configurer une fenêtre de suppression des doublons

