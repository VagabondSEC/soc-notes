# Operators

## where

Filtre les lignes selon une condition booléenne.

## Exemple : where

StormEvents | where State == "TEXAS" and DamageProperty > 5000

## Cas d'usage : where

En hunting avec Sentinel, where s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis where pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## project

Sélectionne les colonnes à garder.

## Exemple : project

StormEvents | project EventId, State, DamageProperty

## Cas d'usage : project

En hunting avec Sentinel, project s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis project pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## project-away

Supprime des colonnes.

## Exemple : project-away

StormEvents | project-away EpisodeId

## Cas d'usage : project-away

En hunting avec Sentinel, project-away s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis project-away pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## project-rename

Renomme des colonnes.

## Exemple : project-rename

StormEvents | project-rename StateName = State

## Cas d'usage : project-rename

En hunting avec Sentinel, project-rename s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis project-rename pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## project-reorder

Réordonne les colonnes.

## Exemple : project-reorder

StormEvents | project-reorder EventId, DamageProperty, State

## Cas d'usage : project-reorder

En hunting avec Sentinel, project-reorder s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis project-reorder pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## extend

Crée de nouvelles colonnes calculées.

## Exemple : extend

StormEvents | extend TotalDamage = DamageProperty + DamageCrops

## Cas d'usage : extend

En hunting avec Sentinel, extend s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis extend pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## summarize

Agrège les lignes avec des fonctions d'agrégation.

## Exemple : summarize

StormEvents | summarize Total = sum(DamageProperty) by State

## Cas d'usage : summarize

En hunting avec Sentinel, summarize s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis summarize pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## count

Compte les lignes.

## Exemple : count

StormEvents | count

## Cas d'usage : count

En hunting avec Sentinel, count s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis count pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## dcount

Compte les valeurs distinctes d'une colonne.

## Exemple : dcount

StormEvents | summarize dcount(EventId) by State

## Cas d'usage : dcount

En hunting avec Sentinel, dcount s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis dcount pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## distinct

Retourne les combinaisons distinctes.

## Exemple : distinct

StormEvents | distinct State, EventType

## Cas d'usage : distinct

En hunting avec Sentinel, distinct s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis distinct pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## make-list

Agrège les valeurs d'une colonne en une liste JSON.

## Exemple : make-list

StormEvents | summarize make_list(EventType) by State

## Cas d'usage : make-list

En hunting avec Sentinel, make-list s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis make-list pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## make-set

Agrège les valeurs distinctes en un ensemble JSON.

## Exemple : make-set

StormEvents | summarize make_set(EventType) by State

## Cas d'usage : make-set

En hunting avec Sentinel, make-set s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis make-set pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## make-series

Crée une série temporelle agrégée.

## Exemple : make-series

StormEvents | make-series Count = count() default = 0 on StartTime step 1d by State

## Cas d'usage : make-series

En hunting avec Sentinel, make-series s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis make-series pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## bin

Arrondit les valeurs dans des buckets (utilisé avec summarize).

## Exemple : bin

StormEvents | summarize count() by bin(StartTime, 1d)

## Cas d'usage : bin

En hunting avec Sentinel, bin s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis bin pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## join

Fusionne deux tables sur des colonnes communes.

## Exemple : join

Table1 | join kind=inner (Table2) on Key

## Cas d'usage : join

En hunting avec Sentinel, join s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis join pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## union

Concatène plusieurs tables avec les mêmes colonnes.

## Exemple : union

union Table1, Table2

## Cas d'usage : union

En hunting avec Sentinel, union s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis union pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## range

Génère une table de valeurs séquentielles.

## Exemple : range

range x from 1 to 10 step 1

## Cas d'usage : range

En hunting avec Sentinel, range s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis range pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## sort

Trie les lignes.

## Exemple : sort

StormEvents | sort by DamageProperty desc

## Cas d'usage : sort

En hunting avec Sentinel, sort s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis sort pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## order

Alias de sort.

## Exemple : order

StormEvents | order by State asc, DamageProperty desc

## Cas d'usage : order

En hunting avec Sentinel, order s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis order pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## top

Retourne les N premières lignes selon un ordre.

## Exemple : top

StormEvents | top 5 by DamageProperty

## Cas d'usage : top

En hunting avec Sentinel, top s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis top pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## top-nested

Top hiérarchique multi-niveaux.

## Exemple : top-nested

StormEvents | top-nested 3 by State, top-nested 3 by EventType

## Cas d'usage : top-nested

En hunting avec Sentinel, top-nested s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis top-nested pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## mv-expand

Développe une colonne multi-valeurs en plusieurs lignes.

## Exemple : mv-expand

Table | mv-expand Tags

## Cas d'usage : mv-expand

En hunting avec Sentinel, mv-expand s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis mv-expand pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## mv-apply

Applique une sous-requête à chaque élément d'une colonne multi-valeurs.

## Exemple : mv-apply

Table | mv-apply Tags on (summarize count())

## Cas d'usage : mv-apply

En hunting avec Sentinel, mv-apply s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis mv-apply pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## parse

Extrait des champs avec un modèle de chaîne.

## Exemple : parse

Table | parse LogLine with "IP=" IP ", Port=" Port

## Cas d'usage : parse

En hunting avec Sentinel, parse s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis parse pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## parse-where

Comme parse mais ne garde que les lignes qui matchent.

## Exemple : parse-where

Table | parse-where LogLine with "IP=" IP

## Cas d'usage : parse-where

En hunting avec Sentinel, parse-where s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis parse-where pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## parse-kv

Extrait des paires clé=valeur.

## Exemple : parse-kv

Table | parse-kv LogLine as keyvalue

## Cas d'usage : parse-kv

En hunting avec Sentinel, parse-kv s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis parse-kv pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## evaluate

Appelle des plugins (autocluster, basket, diffpatterns...).

## Exemple : evaluate

Table | evaluate autocluster()

## Cas d'usage : evaluate

En hunting avec Sentinel, evaluate s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis evaluate pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## invoke

Applique une fonction de table aux lignes.

## Exemple : invoke

Table | invoke MyFunction()

## Cas d'usage : invoke

En hunting avec Sentinel, invoke s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis invoke pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## partition

Divise une table en sous-ensembles selon une clé.

## Exemple : partition

StormEvents | partition by State (summarize count())

## Cas d'usage : partition

En hunting avec Sentinel, partition s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis partition pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## serialize

Garantit l'ordre des lignes pour les opérations séquentielles.

## Exemple : serialize

StormEvents | serialize | row_cumsum(DamageProperty)

## Cas d'usage : serialize

En hunting avec Sentinel, serialize s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis serialize pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## render

Affiche les résultats sous forme de graphique.

## Exemple : render

StormEvents | summarize count() by bin(StartTime, 1d) | render timechart

## Cas d'usage : render

En hunting avec Sentinel, render s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis render pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## sample

Retourne un échantillon aléatoire de lignes.

## Exemple : sample

StormEvents | sample 100

## Cas d'usage : sample

En hunting avec Sentinel, sample s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis sample pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## sample-distinct

Échantillonne des valeurs distinctes d'une colonne.

## Exemple : sample-distinct

StormEvents | sample-distinct 50 of State

## Cas d'usage : sample-distinct

En hunting avec Sentinel, sample-distinct s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis sample-distinct pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## scan

Analyse séquentielle avec état (séquences d'événements).

## Exemple : scan

Table | scan with_match_id=id on (true) partition by User order by Time

## Cas d'usage : scan

En hunting avec Sentinel, scan s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis scan pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## search

Recherche plein texte dans toutes les colonnes.

## Exemple : search

StormEvents | search "flood"

## Cas d'usage : search

En hunting avec Sentinel, search s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis search pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## take

Alias de limit : retourne les N premières lignes.

## Exemple : take

StormEvents | take 10

## Cas d'usage : take

En hunting avec Sentinel, take s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis take pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## limit

Limite le nombre de lignes.

## Exemple : limit

StormEvents | limit 10

## Cas d'usage : limit

En hunting avec Sentinel, limit s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis limit pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## get

Récupère une table nommée (fonction get).

## Exemple : get

get ("TableName")

## Cas d'usage : get

En hunting avec Sentinel, get s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis get pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## print

Produit une table d'une seule ligne avec des expressions.

## Exemple : print

print Hello = "world", When = ago(1h)

## Cas d'usage : print

En hunting avec Sentinel, print s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis print pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## let

Définit des variables (scalaires, tables, fonctions) pour la requête.

## Exemple : let

let Threshold = 100; StormEvents | where DamageProperty > Threshold

## Cas d'usage : let

En hunting avec Sentinel, let s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis let pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## set

Définit des options de requête (set <option>).

## Exemple : set

StormEvents | set query_datascope = allscopes

## Cas d'usage : set

En hunting avec Sentinel, set s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis set pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## alias

Crée un alias de table.

## Exemple : alias

let MyTable = (StormEvents | where State == "FLORIDA"); MyTable | count

## Cas d'usage : alias

En hunting avec Sentinel, alias s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis alias pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## datatable

Déclare une table littérale en mémoire.

## Exemple : datatable

datatable (Name:string, Value:int) ["a", 1, "b", 2]

## Cas d'usage : datatable

En hunting avec Sentinel, datatable s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis datatable pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## externaldata

Interroge des données externes (blob, fichiers).

## Exemple : externaldata

externaldata (Value:string) ["https://example.com/data.csv"]

## Cas d'usage : externaldata

En hunting avec Sentinel, externaldata s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis externaldata pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## facet

Analyse une colonne selon plusieurs facettes.

## Exemple : facet

StormEvents | facet by State, EventType

## Cas d'usage : facet

En hunting avec Sentinel, facet s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis facet pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## find

Cherche une valeur dans toutes les tables du scope.

## Exemple : find

find where EventType == "Flood"

## Cas d'usage : find

En hunting avec Sentinel, find s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis find pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## fork

Duplique le flux en plusieurs branches.

## Exemple : fork

StormEvents | fork (summarize count() by State), (summarize count() by EventType)

## Cas d'usage : fork

En hunting avec Sentinel, fork s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis fork pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## materialize

Cache le résultat d'une sous-requête pour réutilisation.

## Exemple : materialize

let A = materialize(StormEvents | summarize count() by State); A | where count_ > 10

## Cas d'usage : materialize

En hunting avec Sentinel, materialize s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis materialize pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## reduce

Regroupe des valeurs similaires avec un critère de similarité.

## Exemple : reduce

Table | reduce by Message

## Cas d'usage : reduce

En hunting avec Sentinel, reduce s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis reduce pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## rn

Calcule un classement (ranking) avec rank/row_number/dense_rank.

## Exemple : rn

StormEvents | summarize Total = sum(DamageProperty) by State | rn rank = rank(Total)

## Cas d'usage : rn

En hunting avec Sentinel, rn s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis rn pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## row_cumsum

Somme cumulée sur les lignes ordonnées.

## Exemple : row_cumsum

StormEvents | serialize | row_cumsum(DamageProperty)

## Cas d'usage : row_cumsum

En hunting avec Sentinel, row_cumsum s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis row_cumsum pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## row_rank

Classement local sur une partition.

## Exemple : row_rank

StormEvents | partition by State (serialize | row_rank DamageRank = row_rank() by DamageProperty)

## Cas d'usage : row_rank

En hunting avec Sentinel, row_rank s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis row_rank pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## arg_max

Retourne la ligne avec la valeur max d'une colonne.

## Exemple : arg_max

Table | summarize arg_max(Time, *) by User

## Cas d'usage : arg_max

En hunting avec Sentinel, arg_max s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis arg_max pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## arg_min

Retourne la ligne avec la valeur min d'une colonne.

## Exemple : arg_min

Table | summarize arg_min(Time, *) by User

## Cas d'usage : arg_min

En hunting avec Sentinel, arg_min s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis arg_min pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## countif

Compte les lignes où la condition est vraie.

## Exemple : countif

Table | summarize countif(StatusCode == 500) by Host

## Cas d'usage : countif

En hunting avec Sentinel, countif s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis countif pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## sumif

Somme les valeurs où la condition est vraie.

## Exemple : sumif

Table | summarize sumif(Bytes, Bytes > 1000) by Host

## Cas d'usage : sumif

En hunting avec Sentinel, sumif s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis sumif pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## dcountif

Compte distinct où la condition est vraie.

## Exemple : dcountif

Table | summarize dcountif(User, Action == "login")

## Cas d'usage : dcountif

En hunting avec Sentinel, dcountif s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis dcountif pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## percentile

Calcule un percentile sur une colonne.

## Exemple : percentile

Table | summarize p95 = percentile(Latency, 95) by Host

## Cas d'usage : percentile

En hunting avec Sentinel, percentile s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis percentile pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## percentiles

Calcule plusieurs percentiles.

## Exemple : percentiles

Table | summarize percentiles(Latency, 50, 95, 99)

## Cas d'usage : percentiles

En hunting avec Sentinel, percentiles s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis percentiles pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## stdev

Écart-type.

## Exemple : stdev

Table | summarize stdev(Latency)

## Cas d'usage : stdev

En hunting avec Sentinel, stdev s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis stdev pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## variance

Variance.

## Exemple : variance

Table | summarize variance(Latency)

## Cas d'usage : variance

En hunting avec Sentinel, variance s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis variance pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## min

Minimum d'une colonne.

## Exemple : min

Table | summarize min(Latency)

## Cas d'usage : min

En hunting avec Sentinel, min s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis min pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## max

Maximum d'une colonne.

## Exemple : max

Table | summarize max(Latency)

## Cas d'usage : max

En hunting avec Sentinel, max s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis max pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## avg

Moyenne d'une colonne.

## Exemple : avg

Table | summarize avg(Latency)

## Cas d'usage : avg

En hunting avec Sentinel, avg s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis avg pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## pack

Crée un objet dynamique (dict) à partir de colonnes.

## Exemple : pack

Table | summarize pack("min", min(Latency), "max", max(Latency))

## Cas d'usage : pack

En hunting avec Sentinel, pack s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis pack pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## bag_unpack

Développe un objet dynamique en colonnes.

## Exemple : bag_unpack

Table | project-away d | evaluate bag_unpack(d)

## Cas d'usage : bag_unpack

En hunting avec Sentinel, bag_unpack s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis bag_unpack pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## pivot

Pivote une table (lignes en colonnes).

## Exemple : pivot

StormEvents | evaluate pivot(State, count(), sum(DamageProperty))

## Cas d'usage : pivot

En hunting avec Sentinel, pivot s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis pivot pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## sequence_detect

Détecte des séquences d'événements avec contraintes.

## Exemple : sequence_detect

Table | evaluate sequence_detect(timestamp_column, 1h, state_1, state_2)

## Cas d'usage : sequence_detect

En hunting avec Sentinel, sequence_detect s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis sequence_detect pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## autocluster

Trouve des patterns de regroupement dans les données (plugin).

## Exemple : autocluster

Table | evaluate autocluster()

## Cas d'usage : autocluster

En hunting avec Sentinel, autocluster s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis autocluster pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## basket

Trouve des itemsets fréquents (plugin).

## Exemple : basket

Table | evaluate basket()

## Cas d'usage : basket

En hunting avec Sentinel, basket s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis basket pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## diffpatterns

Compare deux populations et trouve les différences (plugin).

## Exemple : diffpatterns

Table | evaluate diffpatterns(IsAnomaly)

## Cas d'usage : diffpatterns

En hunting avec Sentinel, diffpatterns s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis diffpatterns pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## narrow

Réduit le nombre de colonnes en conservant les stats.

## Exemple : narrow

Table | narrow by State

## Cas d'usage : narrow

En hunting avec Sentinel, narrow s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis narrow pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

