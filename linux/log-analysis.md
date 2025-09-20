# Log Analysis

## Les logs Linux

/var/log/auth.log : authentifications (Debian/Ubuntu)
/var/log/secure : authentifications (RHEL/CentOS)
/var/log/syslog : messages système
/var/log/apache2/ et /var/log/nginx/ : accès web

## Analyse de auth.log

grep "Failed password" /var/log/auth.log pour les brute forces
grep "Accepted" pour les succès
Un brute force réussi : Failed puis Accepted depuis la même IP
journalctl _COMM=sshd pour les logs sshd

## journalctl

journalctl -u service pour un service
journalctl --since "2 hours ago"
journalctl -p err pour les erreurs
Les logs systemd centralisés facilitent l'analyse

## Analyse des logs web

Les lignes d'accès : IP, timestamp, requête, code, taille
grep " 404 " pour les erreurs, " 500 " pour les pannes
Les patterns d'exploitation : sqlmap, nikto, curl POST inhabituels
awk '{print $1}' access.log | sort | uniq -c | sort -rn pour le top IP

## Les shells suspects

bash -i, sh -c, les reverse shells dans les processus
Les connexions sortantes vers des IP étrangères depuis des daemons
Vérifier les fichiers dans /tmp et /dev/shm

