# Wireshark Filters

## Filtres d'affichage de base

ip.src == 10.0.0.5 filtre sur l'IP source
ip.dst == 8.8.8.8 filtre sur l'IP destination
tcp.port == 443 filtre sur le port TCP
Les filtres se combinent avec and, or, not

## Filtres HTTP

http.request filtre les requêtes HTTP
http.response.code == 500 filtre les erreurs serveur
http.host == "example.com" filtre par hôte
http.user_agent contient "curl" détecte les clients curl

## Filtres DNS

dns.qry.name contient "pastebin"
dns.flags.response == 0 pour les requêtes uniquement
dns.resp.type == 1 pour les réponses A
Utile pour repérer les exfiltrations DNS

## Filtres TLS

tls.handshake.type == 1 pour les ClientHello
tls.handshake.extensions_server_name pour le SNI (le domaine demandé)
Le SNI est en clair même en TLS, précieux pour le tri

## Filtres sur les flags TCP

tcp.flags.syn == 1 et tcp.flags.ack == 0 pour les SYN seuls
tcp.flags.reset == 1 pour les RST
Une rafale de SYN sans ACK = scan de ports

## Filtres par protocole

arp, icmp, smb, smb2, kerberos, ldap, ftp, ssh
icmp.type == 8 pour les ping request
smb2.cmd == 5 (SMB2_CREATE) pour les ouvertures de fichiers

## Filtres sur le contenu

frame contains "password" cherche une chaîne dans le payload
data.data contient 3a:3a:3a recherche des données hexadécimales
Attention : frame contains est lent sur les grosses captures

## Filtres par conversation

tcp.stream == 0 isole la première conversation TCP
Suivre un flux complet : clic droit sur un paquet > Follow > TCP Stream
Utile pour reconstituer une attaque complète

