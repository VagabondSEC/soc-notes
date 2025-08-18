# Splunk Basics

## Qu'est-ce que Splunk

Splunk est un SIEM (Security Information and Event Management) qui ingère des logs
de sources variées (Windows, Linux, firewalls, proxies, cloud) et les indexe
pour permettre la recherche, le dashboarding et les alertes en temps réel.

## Architecture

Forwarder : collecte et envoie les logs (Universal Forwarder léger)
Indexer : stocke, indexe et compresse les données
Search Head : interface de recherche et de corrélation
Deployment Server : centralise la config des forwarders

## Sources de données courantes

Windows Event Logs (Security, System, Application)
Syslog Linux (auth.log, syslog, kern.log)
Firewall / proxy (Palo Alto, Fortinet, Squid, Zscaler)
EDR (CrowdStrike, Defender for Endpoint, SentinelOne)
DNS, DHCP, Active Directory, VPN

