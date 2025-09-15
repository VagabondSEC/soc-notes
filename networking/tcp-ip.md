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

## Les ports importants

22 SSH, 80 HTTP, 443 HTTPS, 445 SMB, 3389 RDP
53 DNS (UDP/TCP), 25 SMTP, 389 LDAP, 636 LDAPS
1433 MSSQL, 3306 MySQL, 5985/5986 WinRM
Connaître les ports par coeur accélère le tri des logs

