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

## Exemple : floor

print floor(3.7)

## Cas d'usage : floor

En hunting avec Sentinel, floor s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis floor pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## ceiling

Arrondit à l'entier supérieur.

## Exemple : ceiling

print ceiling(3.2)

## Cas d'usage : ceiling

En hunting avec Sentinel, ceiling s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis ceiling pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## round

Arrondit avec précision.

## Exemple : round

print round(3.14159, 2)

## Cas d'usage : round

En hunting avec Sentinel, round s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis round pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## strcat

Concatène des chaînes.

## Exemple : strcat

extend FullName = strcat(FirstName, " ", LastName)

## Cas d'usage : strcat

En hunting avec Sentinel, strcat s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis strcat pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## strcat_array

Concatène un tableau en chaîne avec séparateur.

## Exemple : strcat_array

print strcat_array(dynamic(["a", "b"]), "-")

## Cas d'usage : strcat_array

En hunting avec Sentinel, strcat_array s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis strcat_array pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## split

Sépare une chaîne en tableau.

## Exemple : split

extend Parts = split(Path, "\\")

## Cas d'usage : split

En hunting avec Sentinel, split s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis split pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## substring

Extrait une sous-chaîne.

## Exemple : substring

extend Sub = substring(UserAgent, 0, 20)

## Cas d'usage : substring

En hunting avec Sentinel, substring s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis substring pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## toupper

Met en majuscules.

## Exemple : toupper

extend Upper = toupper(User)

## Cas d'usage : toupper

En hunting avec Sentinel, toupper s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis toupper pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## tolower

Met en minuscules.

## Exemple : tolower

extend Lower = tolower(User)

## Cas d'usage : tolower

En hunting avec Sentinel, tolower s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis tolower pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## trim

Supprime les espaces (ou caractères) en début/fin.

## Exemple : trim

extend Clean = trim(Message)

## Cas d'usage : trim

En hunting avec Sentinel, trim s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis trim pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## replace

Remplace une sous-chaîne (regex).

## Exemple : replace

extend Fixed = replace(Path, @"\\+", "/")

## Cas d'usage : replace

En hunting avec Sentinel, replace s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis replace pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## indexof

Position d'une sous-chaîne.

## Exemple : indexof

print indexof("abcabc", "b")

## Cas d'usage : indexof

En hunting avec Sentinel, indexof s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis indexof pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## startswith

Teste le début d'une chaîne.

## Exemple : startswith

where UserAgent startswith "Mozilla"

## Cas d'usage : startswith

En hunting avec Sentinel, startswith s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis startswith pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## endswith

Teste la fin d'une chaîne.

## Exemple : endswith

where File endswith ".exe"

## Cas d'usage : endswith

En hunting avec Sentinel, endswith s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis endswith pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## contains

Teste la présence d'une sous-chaîne (opérateur).

## Exemple : contains

where CommandLine contains "powershell"

## Cas d'usage : contains

En hunting avec Sentinel, contains s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis contains pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## iif

Conditionnel en ligne (ancien iff).

## Exemple : iif

extend Status = iif(Code == 200, "OK", "Error")

## Cas d'usage : iif

En hunting avec Sentinel, iif s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis iif pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## iff

Alias de iif (nouvelle syntaxe).

## Exemple : iff

extend Status = iff(Code == 200, "OK", "Error")

## Cas d'usage : iff

En hunting avec Sentinel, iff s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis iff pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## case

Conditionnel multi-branches.

## Exemple : case

extend Level = case(Risk > 80, "High", Risk > 50, "Medium", "Low")

## Cas d'usage : case

En hunting avec Sentinel, case s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis case pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## coalesce

Première valeur non nulle.

## Exemple : coalesce

extend IP = coalesce(IPv4, IPv6, "unknown")

## Cas d'usage : coalesce

En hunting avec Sentinel, coalesce s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis coalesce pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## isnull

Teste si une valeur est nulle.

## Exemple : isnull

where isnull(User)

## Cas d'usage : isnull

En hunting avec Sentinel, isnull s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis isnull pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## isempty

Teste si une chaîne est vide.

## Exemple : isempty

where isempty(CommandLine)

## Cas d'usage : isempty

En hunting avec Sentinel, isempty s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis isempty pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## format_datetime

Formate une date selon un modèle.

## Exemple : format_datetime

extend Date = format_datetime(Timestamp, "yyyy-MM-dd HH:mm")

## Cas d'usage : format_datetime

En hunting avec Sentinel, format_datetime s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis format_datetime pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## parse_json

Parse une chaîne JSON en objet dynamique.

## Exemple : parse_json

extend Obj = parse_json(RawData)

## Cas d'usage : parse_json

En hunting avec Sentinel, parse_json s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis parse_json pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## tostring

Convertit en chaîne.

