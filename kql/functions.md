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

## Exemple : datetime

print datetime("2026-01-01 10:30:00")

## Cas d'usage : datetime

En hunting avec Sentinel, datetime s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis datetime pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## todatetime

Conversion tolérante en datetime.

## Exemple : todatetime

print todatetime("2026-01-01")

## Cas d'usage : todatetime

En hunting avec Sentinel, todatetime s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis todatetime pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## totimespan

Conversion en timespan.

## Exemple : totimespan

print totimespan("1.02:03:04")

## Cas d'usage : totimespan

En hunting avec Sentinel, totimespan s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis totimespan pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## bin

Arrondit à un bucket.

## Exemple : bin

summarize count() by bin(Timestamp, 1h)

## Cas d'usage : bin

En hunting avec Sentinel, bin s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis bin pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## floor

Arrondit à l'entier inférieur.

