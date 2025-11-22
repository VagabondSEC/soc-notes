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

