# Splunk Fields

## Champs indexés vs extraits

Les champs indexés (host, source, sourcetype, _time) sont dans l'index
Les champs extraits sont calculés à la recherche (plus flexible)
L'extraction à la recherche coûte plus cher, l'indexation au volume

## Extraction de champs automatique

Splunk extrait automatiquement les paires clé=valeur
Les formats JSON, XML et CSV sont parsés nativement
Les sourcetypes bien modélisés donnent des champs propres

## Calculated fields

Les champs calculés s'appliquent à la recherche sur un sourcetype
Définis dans Settings > Fields > Calculated fields
Exemple : score = case(match(src_ip, "^10\\."), 10, 1=1, 50)

## Field extractions (regex)

Les regex extractions s'appliquent à un sourcetype
Exemple : (?<username>\w+) a extrait le champ username
À utiliser quand le format n'est pas clé=valeur

