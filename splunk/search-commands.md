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

## Cas d'usage : table

En investigation SOC, table est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## rename

Renomme un champ pour le rendre plus lisible.

## Exemple : rename

index=main | rename src_ip as source_address

## Cas d'usage : rename

En investigation SOC, rename est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## dedup

Supprime les événements dupliqués selon un ou plusieurs champs.

## Exemple : dedup

index=main | dedup host | table host

## Cas d'usage : dedup

En investigation SOC, dedup est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## sort

Trie les résultats par ordre croissant ou décroissant.

## Exemple : sort

index=main | sort - _time | head 10

## Cas d'usage : sort

En investigation SOC, sort est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## head

Limite les résultats aux N premiers événements.

