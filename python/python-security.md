# Python Security

## Parser un CSV d'alertes

import csv et DictReader pour lire les exports
Filtrer et agréger avec des compteurs
Exporter les résultats en CSV pour Excel

## Parser des logs avec regex

re.search pour extraire IP, user, timestamp
Les patterns : r"(?P<ip>\d+\.\d+\.\d+\.\d+)"
Tester les regex sur un échantillon avant de tout parser

## Requêter une API de threat intel

requests.get avec une clé API (AbuseIPDB, VirusTotal)
Gérer les rate limits avec time.sleep
Enrichir un CSV d'IP avec les verdicts

## Automatiser VirusTotal

POST /api/v3/files pour soumettre un hash
GET /api/v3/files/{id} pour le rapport
Agréger les verdicts : malicious, suspicious, harmless

