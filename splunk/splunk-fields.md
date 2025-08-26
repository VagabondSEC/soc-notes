# Splunk Fields

## Champs indexés vs extraits

Les champs indexés (host, source, sourcetype, _time) sont dans l'index
Les champs extraits sont calculés à la recherche (plus flexible)
L'extraction à la recherche coûte plus cher, l'indexation au volume

## Extraction de champs automatique

Splunk extrait automatiquement les paires clé=valeur
Les formats JSON, XML et CSV sont parsés nativement
Les sourcetypes bien modélisés donnent des champs propres

