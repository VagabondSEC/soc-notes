# Functions

## ago

Retourne la date il y a X (soustrait un timespan).

## Exemple : ago

where Timestamp > ago(7d)

## Cas d'usage : ago

En hunting avec Sentinel, ago s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis ago pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## now

Retourne la date/heure actuelle.

## Exemple : now

print now()

## Cas d'usage : now

En hunting avec Sentinel, now s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis now pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## datetime

Convertit une chaîne en datetime.

