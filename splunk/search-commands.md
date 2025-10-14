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

## Exemple : head

index=main | head 100

## Cas d'usage : head

En investigation SOC, head est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## tail

Limite les résultats aux N derniers événements (après un tri).

## Exemple : tail

index=main | sort _time | tail 5

## Cas d'usage : tail

En investigation SOC, tail est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## top

Affiche les valeurs les plus fréquentes d'un champ avec counts et pourcentages.

## Exemple : top

index=main | top limit=10 user

## Cas d'usage : top

En investigation SOC, top est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## rare

Affiche les valeurs les moins fréquentes d'un champ.

## Exemple : rare

index=main | rare host

## Cas d'usage : rare

En investigation SOC, rare est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## stats

Agrège les résultats avec des fonctions statistiques (count, sum, avg, dc...).

## Exemple : stats

index=main | stats count by action

## Cas d'usage : stats

En investigation SOC, stats est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## eventstats

Calcule des statistiques sur TOUT le dataset et les ajoute à chaque événement.

## Exemple : eventstats

index=main | eventstats avg(bytes) as avg_bytes

## Cas d'usage : eventstats

En investigation SOC, eventstats est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## streamstats

Calcule des statistiques cumulatives au fil du flux d'événements.

## Exemple : streamstats

index=main | streamstats count as running_count

## Cas d'usage : streamstats

En investigation SOC, streamstats est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## timechart

Série temporelle : agrège par buckets de temps.

## Exemple : timechart

index=main | timechart count by action span=1h

## Cas d'usage : timechart

En investigation SOC, timechart est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## chart

Agrège sous forme de tableau sans axe temporel.

## Exemple : chart

index=main | chart count by host, action

## Cas d'usage : chart

En investigation SOC, chart est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## xyseries

Transforme les résultats en tableau XY (lignes, colonnes, valeurs).

## Exemple : xyseries

index=main | chart count by host, action | xyseries host action count

## Cas d'usage : xyseries

En investigation SOC, xyseries est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## eval

Crée ou modifie des champs avec des expressions et fonctions.

## Exemple : eval

index=main | eval severity=case(risk_score>=80, "high", risk_score>=50, "medium", 1=1, "low")

## Cas d'usage : eval

En investigation SOC, eval est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## where

Filtre les événements avec une expression évaluée (plus puissant que search).

## Exemple : where

index=main | where len(command_line) > 500

## Cas d'usage : where

En investigation SOC, where est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## rex

Extrait des champs avec une expression régulière nommée.

## Exemple : rex

index=main | rex field=_raw "(?<ip>\d+\.\d+\.\d+\.\d+)"

## Cas d'usage : rex

En investigation SOC, rex est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## regex

Filtre les événements dont un champ correspond à une regex.

## Exemple : regex

index=main | regex _raw="(?i)error|fail"

## Cas d'usage : regex

En investigation SOC, regex est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## erex

Génère automatiquement une regex à partir d'exemples de valeurs.

## Exemple : erex

index=main | erex ip examples="192.168.1.1, 10.0.0.5"

## Cas d'usage : erex

En investigation SOC, erex est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## lookup

Enrichit les événements en joignant un fichier de lookup.

## Exemple : lookup

index=main | lookup asset_lookup asset_id OUTPUT asset_owner

## Cas d'usage : lookup

En investigation SOC, lookup est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## inputlookup

Lit directement un fichier de lookup comme source de la recherche.

## Exemple : inputlookup

| inputlookup firewall_blacklist

## Cas d'usage : inputlookup

En investigation SOC, inputlookup est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## outputlookup

Écrit les résultats de la recherche dans un fichier de lookup.

## Exemple : outputlookup

index=main | outputlookup suspicious_hosts

## Cas d'usage : outputlookup

En investigation SOC, outputlookup est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## join

Joint deux jeux de résultats sur des champs communs (attention aux sous-recherches).

## Exemple : join

index=main [search index=proxy | fields src_ip] | join src_ip

## Cas d'usage : join

En investigation SOC, join est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## append

Ajoute les résultats d'une recherche à la recherche principale.

## Exemple : append

index=main | append [search index=wineventlog]

## Cas d'usage : append

En investigation SOC, append est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## appendcols

Ajoute des colonnes d'une sous-recherche aux événements existants.

## Exemple : appendcols

index=main | appendcols [search index=threatintel | fields ioc]

## Cas d'usage : appendcols

En investigation SOC, appendcols est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## transaction

Regroupe des événements liés (même session, même utilisateur) en une seule entité.

## Exemple : transaction

index=main | transaction user maxspan=5m

## Cas d'usage : transaction

En investigation SOC, transaction est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

## spath

Extrait des champs depuis des données structurées (JSON, XML).

## Exemple : spath

index=main | spath path=user.name

## Cas d'usage : spath

En investigation SOC, spath est utile pour analyser les logs d'authentification et les processus. On l'utilise dans une recherche avec un index ciblé (index=windows ou index=main) et on corrèle le résultat avec d'autres sources (proxy, firewall, EDR).

