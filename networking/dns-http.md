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

