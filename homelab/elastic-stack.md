# Elastic Stack

## Le lab Elastic

Elasticsearch : le moteur de recherche et de stockage
Kibana : l'interface web (discover, dashboards, alerts)
Les agents Elastic (Winlogbeat, Filebeat, Packetbeat) envoient les logs
Une stack complète tient dans une VM avec 8 Go de RAM

## Installation Elasticsearch

Télécharger Elasticsearch depuis elastic.co et décompresser
Configurer elasticsearch.yml : network.host, cluster.name
Lancer avec bin/elasticsearch et vérifier sur le port 9200
curl localhost:9200 renvoie le JSON de statut

## Installation Kibana

Kibana se connecte à Elasticsearch via kibana.yml (elasticsearch.hosts)
L'interface est sur le port 5601
La première connexion demande un token généré par Elasticsearch

