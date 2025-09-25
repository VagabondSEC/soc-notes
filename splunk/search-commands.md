# Search Commands

## search

Recherche plein texte dans les événements indexés, première commande de presque toute requête.

## Exemple : search

index=windows EventCode=4625 | search user=admin

## Cas d'usage : search

En investigation SOC, search est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## fields

Affiche ou supprime des champs pour réduire le volume affiché.

## Exemple : fields

index=main | fields host, source, sourcetype, _time

## Cas d'usage : fields

En investigation SOC, fields est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## table

Affiche les résultats sous forme de tableau avec les colonnes choisies.

## Exemple : table

index=main | table _time, host, user, action

