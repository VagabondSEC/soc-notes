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

## Exemple : tostring

extend Str = tostring(Count)

## Cas d'usage : tostring

En hunting avec Sentinel, tostring s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis tostring pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## toint

Convertit en entier.

## Exemple : toint

extend N = toint(Size)

## Cas d'usage : toint

En hunting avec Sentinel, toint s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis toint pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## tolong

Convertit en long.

## Exemple : tolong

extend L = tolong(Size)

## Cas d'usage : tolong

En hunting avec Sentinel, tolong s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis tolong pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## toreal

Convertit en réel (double).

## Exemple : toreal

extend R = toreal(Value)

## Cas d'usage : toreal

En hunting avec Sentinel, toreal s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis toreal pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## tobool

Convertit en booléen.

## Exemple : tobool

extend B = tobool(Flag)

## Cas d'usage : tobool

En hunting avec Sentinel, tobool s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis tobool pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## hash

Hash SHA256 d'une chaîne.

## Exemple : hash

extend H = hash("s3cr3t", "sha256")

## Cas d'usage : hash

En hunting avec Sentinel, hash s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis hash pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## base64_encode

Encode en base64.

## Exemple : base64_encode

extend B64 = base64_encode(Data)

## Cas d'usage : base64_encode

En hunting avec Sentinel, base64_encode s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis base64_encode pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## base64_decode

Décode du base64.

## Exemple : base64_decode

extend Plain = base64_decode_tostring(B64)

## Cas d'usage : base64_decode

En hunting avec Sentinel, base64_decode s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis base64_decode pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## uri_parse

Décompose une URL en parties.

## Exemple : uri_parse

extend U = uri_parse(Url)

## Cas d'usage : uri_parse

En hunting avec Sentinel, uri_parse s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis uri_parse pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## url_decode

Décode une URL encodée.

## Exemple : url_decode

extend Decoded = url_decode(EncodedUrl)

## Cas d'usage : url_decode

En hunting avec Sentinel, url_decode s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis url_decode pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## strlen

Longueur d'une chaîne.

## Exemple : strlen

extend Len = strlen(CommandLine)

## Cas d'usage : strlen

En hunting avec Sentinel, strlen s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis strlen pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## reverse

Inverse une chaîne.

## Exemple : reverse

print reverse("abc")

## Cas d'usage : reverse

En hunting avec Sentinel, reverse s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis reverse pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## count_distinct

Compte distinct (ancien style dcount).

## Exemple : count_distinct

summarize count_distinct(User)

## Cas d'usage : count_distinct

En hunting avec Sentinel, count_distinct s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis count_distinct pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## make_string

Construit une chaîne depuis plusieurs colonnes.

## Exemple : make_string

extend S = make_string(A, "-", B)

## Cas d'usage : make_string

En hunting avec Sentinel, make_string s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis make_string pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## zip

Combine plusieurs tableaux en un tableau de tuples.

## Exemple : zip

print zip(dynamic([1,2]), dynamic(["a","b"]))

## Cas d'usage : zip

En hunting avec Sentinel, zip s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis zip pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## array_length

Taille d'un tableau.

## Exemple : array_length

extend N = array_length(Parts)

## Cas d'usage : array_length

En hunting avec Sentinel, array_length s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis array_length pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## array_slice

Tranche d'un tableau.

## Exemple : array_slice

extend S = array_slice(Parts, 0, 2)

## Cas d'usage : array_slice

En hunting avec Sentinel, array_slice s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis array_slice pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## pack_array

Construit un tableau à partir de valeurs.

## Exemple : pack_array

extend Arr = pack_array(A, B, C)

## Cas d'usage : pack_array

En hunting avec Sentinel, pack_array s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis pack_array pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## range_array

Génère un tableau de nombres.

## Exemple : range_array

print range_array(1, 10, 2)

## Cas d'usage : range_array

En hunting avec Sentinel, range_array s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis range_array pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## repeat

Répète une valeur.

## Exemple : repeat

print repeat("ab", 3)

## Cas d'usage : repeat

En hunting avec Sentinel, repeat s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis repeat pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## tostring_guid

Formate un GUID.

## Exemple : tostring_guid

print tostring_guid(guid)

## Cas d'usage : tostring_guid

En hunting avec Sentinel, tostring_guid s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis tostring_guid pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## format_bytes

Formate une taille en unités lisibles.

## Exemple : format_bytes

print format_bytes(1536)

## Cas d'usage : format_bytes

En hunting avec Sentinel, format_bytes s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis format_bytes pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## parse_version

Parse une version en comparable.

## Exemple : parse_version

where parse_version(Version) >= parse_version("1.2.0")

## Cas d'usage : parse_version

En hunting avec Sentinel, parse_version s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis parse_version pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## datetime_diff

Différence entre deux dates en unité donnée.

## Exemple : datetime_diff

extend DiffMin = datetime_diff("minute", Timestamp, now())

## Cas d'usage : datetime_diff

En hunting avec Sentinel, datetime_diff s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis datetime_diff pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## datetime_add

Ajoute une durée à une date.

## Exemple : datetime_add

extend Later = datetime_add("hour", 2, Timestamp)

## Cas d'usage : datetime_add

En hunting avec Sentinel, datetime_add s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis datetime_add pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## month_of_year

Mois d'une date (1-12).

## Exemple : month_of_year

extend Mois = month_of_year(Timestamp)

## Cas d'usage : month_of_year

En hunting avec Sentinel, month_of_year s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis month_of_year pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## day_of_week

Jour de la semaine (1-7).

## Exemple : day_of_week

extend Jour = day_of_week(Timestamp)

## Cas d'usage : day_of_week

En hunting avec Sentinel, day_of_week s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis day_of_week pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## hour_of_day

Heure d'une date (0-23).

## Exemple : hour_of_day

extend Heure = hour_of_day(Timestamp)

## Cas d'usage : hour_of_day

En hunting avec Sentinel, hour_of_day s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis hour_of_day pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## startofday

Début de journée.

## Exemple : startofday

extend Jour = startofday(Timestamp)

## Cas d'usage : startofday

En hunting avec Sentinel, startofday s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis startofday pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## startofweek

Début de semaine.

## Exemple : startofweek

extend Semaine = startofweek(Timestamp)

## Cas d'usage : startofweek

En hunting avec Sentinel, startofweek s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis startofweek pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## startofmonth

Début de mois.

## Exemple : startofmonth

extend Mois = startofmonth(Timestamp)

## Cas d'usage : startofmonth

En hunting avec Sentinel, startofmonth s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis startofmonth pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## endofday

Fin de journée.

## Exemple : endofday

extend Fin = endofday(Timestamp)

## Cas d'usage : endofday

En hunting avec Sentinel, endofday s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis endofday pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## part_of_day

Partie de la journée (matin, après-midi...).

## Exemple : part_of_day

extend Part = part_of_day(Timestamp)

## Cas d'usage : part_of_day

En hunting avec Sentinel, part_of_day s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis part_of_day pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## getmonth

Nom du mois.

## Exemple : getmonth

extend Mois = getmonth(Timestamp)

## Cas d'usage : getmonth

En hunting avec Sentinel, getmonth s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis getmonth pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## getday

Nom du jour.

## Exemple : getday

extend Jour = getday(Timestamp)

## Cas d'usage : getday

En hunting avec Sentinel, getday s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis getday pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## bin_at

Bucket avec point d'ancrage.

## Exemple : bin_at

summarize count() by bin_at(Timestamp, 1d, datetime(2026-01-01))

## Cas d'usage : bin_at

En hunting avec Sentinel, bin_at s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis bin_at pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## todynamic

Convertit en type dynamique.

## Exemple : todynamic

extend D = todynamic(Raw)

## Cas d'usage : todynamic

En hunting avec Sentinel, todynamic s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis todynamic pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

## parse_command_line

Parse une ligne de commande en arguments structurés.

## Exemple : parse_command_line

extend P = parse_command_line(CommandLine, "windows")

## Cas d'usage : parse_command_line

En hunting avec Sentinel, parse_command_line s'intègre dans une requête KQL typique : SecurityEvent | where TimeGenerated > ago(24h) puis parse_command_line pour agréger ou filtrer. Utile pour les investigations d'identité et les anomalies de connexion.

