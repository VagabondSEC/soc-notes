# Kali Setup

## VM Kali pour l'attaquant

Kali Linux en VM isolée sur le réseau du lab
Les outils : nmap, metasploit, burp, hashcat, responder
Kali attaque, Elastic et TheHive détectent, on apprend des deux côtés

## Scénarios d'attaque dans le lab

Brute force RDP et SSH pour générer des alertes 4625
Mimikatz sur une machine Windows jointe au domaine
Phishing simulé avec une pièce jointe dropper
Chaque attaque génère des logs à analyser dans Elastic

## hashcat dans le lab

hashcat -m 1000 hash.txt wordlist.txt pour les hash NTLM
Les wordlists : rockyou, seclists, custom
Comprendre les formats de hash : NTLM, Kerberos, NetNTLMv2

