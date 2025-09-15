# Tcp Ip

## Le modèle TCP/IP

4 couches : accès réseau, internet, transport, application
La couche transport : TCP (fiable) et UDP (rapide)
La couche internet : IP avec adressage et routage
Comprendre le modèle = comprendre où regarder dans les logs

## Le handshake TCP

SYN -> SYN-ACK -> ACK ouvre une connexion
FIN -> ACK -> FIN -> ACK ferme proprement
RST coupe la connexion immédiatement
Un SYN sans réponse = port filtré

