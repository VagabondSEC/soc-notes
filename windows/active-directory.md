# Active Directory

## Les fondamentaux AD

Active Directory centralise identités et politiques
Les objets : users, groups, computers, OU
Le domaine = la frontière de sécurité
Kerberos est le protocole d'authentification

## Kerberos en bref

Le client demande un TGT au KDC avec ses credentials
Le TGT sert à demander des TGS pour chaque service
Les tickets ont une durée de vie (10h par défaut)
Le Kerberoasting : demander un TGS pour un compte de service et cracker son hash

## Les attaques AD classiques

Kerberoasting (TGS pour comptes de service)
AS-REP roasting (comptes sans preauth)
Pass-the-Hash (réutiliser le hash NTLM)
Golden Ticket (forger un TGT avec le hash krbtgt)
BloodHound cartographie les chemins vers Domain Admins

## Les défenses AD

Activer l'audit complet des logs de sécurité
Surveiller les modifications des groupes privilégiés
Désactiver les comptes de service inutilisés
Microsoft LAPS pour les mots de passe locaux

