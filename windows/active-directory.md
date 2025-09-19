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

