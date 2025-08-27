# Splunk Correlation

## Pourquoi corréler

Un événement seul est rarement une preuve
La corrélation relie plusieurs sources pour confirmer un scénario
Exemple : échec de connexion + succès juste après = brute force réussie

## Scénario brute force

Détecter > 10 échecs 4625 puis un succès 4624 sur le même compte
index=windows EventCode=4625 | stats count by Account, src_ip | where count > 10
Cross-corréler avec le 4624 : index=windows EventCode=4624 | search Account=$compte$

## Scénario exfiltration

Volume sortant anormal vers une IP unique
index=proxy | stats sum(bytes_out) by dest_ip | sort - sum(bytes_out)
Corréler avec les logs DNS pour identifier le domaine

## Correlation searches

Les correlation searches sont des recherches planifiées qui génèrent des notables
Elles vivent dans Enterprise Security ou dans des apps dédiées
Chaque correlation search a une périodicité et un time range

## Notable events

Un notable event est un résultat de corrélation avec un statut
Workflow : New -> In Progress -> Resolved / False Positive
Les notables doivent contenir le contexte (user, host, IOC)

