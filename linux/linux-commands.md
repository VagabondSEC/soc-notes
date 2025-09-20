# Linux Commands

## Les commandes essentielles

ls, cd, cat, less, grep, find, ps, top, netstat, ss
grep -r pour chercher dans les fichiers
find / -name "*.sh" -mtime -7 pour les scripts récents
ss -tlnp pour les ports en écoute

## Grep efficace

grep -E "pattern1|pattern2" pour plusieurs motifs
grep -i ignore la casse, grep -v inverse
grep -A 5 -B 5 donne le contexte autour
zgrep pour les fichiers compressés .gz

## Les processus

ps aux trié par CPU : ps aux --sort=-%cpu
top / htop pour le temps réel
Un processus qui consomme beaucoup de CPU = crypto ou brute force
Vérifier les processus orphelins (PPID 1)

## Le réseau en CLI

ss -tunap liste les connexions avec le process
lsof -i :443 pour ce qui écoute sur 443
curl -v pour débugger les requêtes
tcpdump -i eth0 port 80 pour capturer

