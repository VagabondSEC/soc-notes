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

