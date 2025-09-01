# Splunk Alerts

## Types d'alertes

Par événement : déclenchée à chaque résultat
Par résultat : une fois par fenêtre de recherche
Par intervalle : à chaque exécution planifiée si la condition est vraie

## Throttling

Le throttling évite les alertes en rafale
Exemple : ne pas re-alerter sur le même src_ip pendant 1h
Configurer une fenêtre de suppression des doublons

## Actions d'alerte

Email, webhook, script, ticket (TheHive, Jira)
Le webhook vers TheHive permet de créer un case automatiquement
Inclure le lien vers la recherche dans le contenu de l'alerte

## Bonnes pratiques alertes

Un seuil bas avec beaucoup de bruit détruit la confiance dans le SOC
Documenter chaque alerte : description, playbook, fausse positive connue
Revue mensuelle des alertes qui ne déclenchent jamais

