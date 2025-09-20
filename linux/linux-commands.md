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

