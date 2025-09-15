# Dns Http

## Le protocole DNS

Les requêtes DNS partent en UDP 53, les grosses réponses en TCP
Un domaine -> un ou plusieurs enregistrements (A, AAAA, CNAME, MX, TXT)
Le DNS est un vecteur d'exfiltration et de C2 très utilisé
Surveiller les requêtes vers des domaines récents (WHOIS)

## Les enregistrements DNS

A : IPv4, AAAA : IPv6, CNAME : alias, MX : mail, TXT : texte libre
Les TXT records servent au SPF, DKIM et DMARC
Un TXT record suspect peut cacher une exfiltration

## Le protocole HTTP

Méthodes : GET, POST, PUT, DELETE, HEAD, OPTIONS
Les codes : 2xx succès, 3xx redirection, 4xx client, 5xx serveur
Les en-têtes : Host, User-Agent, Referer, Cookie, Authorization
HTTP est en clair, HTTPS le chiffre (mais pas le SNI)

## Analyse des User-Agents

Un User-Agent curl ou python-requests sur un poste = suspect
Les User-Agents de bot connus (Googlebot) doivent matcher les IP Google
Les malwares utilisent souvent des User-Agents génériques

## HTTP vs HTTPS pour le tri

En HTTP, on voit tout : URL, body, en-têtes
En HTTPS, on voit l'hôte (SNI) et les tailles de flux
Le proxy déchiffré (SSL inspection) redonne la visibilité

