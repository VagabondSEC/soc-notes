# Filters

## ip.addr

Filtre par adresse IP (source ou destination).

## Exemple : ip.addr

ip.addr == 192.168.1.10

## Cas d'usage : ip.addr

Sur une capture réseau, ip.addr permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## ip.src

Filtre par IP source.

## Exemple : ip.src

ip.src == 10.0.0.5

## Cas d'usage : ip.src

Sur une capture réseau, ip.src permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## ip.dst

Filtre par IP destination.

## Exemple : ip.dst

ip.dst == 8.8.8.8

## Cas d'usage : ip.dst

Sur une capture réseau, ip.dst permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## ip.ttl

Filtre par TTL (détection d'OS fingerprinting).

## Exemple : ip.ttl

ip.ttl <= 64

## Cas d'usage : ip.ttl

Sur une capture réseau, ip.ttl permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## ip.proto

Filtre par protocole IP (6=TCP, 17=UDP, 1=ICMP).

## Exemple : ip.proto

ip.proto == 6

## Cas d'usage : ip.proto

Sur une capture réseau, ip.proto permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.port

Filtre par port TCP (source ou destination).

## Exemple : tcp.port

tcp.port == 443

## Cas d'usage : tcp.port

Sur une capture réseau, tcp.port permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.srcport

Filtre par port TCP source.

## Exemple : tcp.srcport

tcp.srcport == 4444

## Cas d'usage : tcp.srcport

Sur une capture réseau, tcp.srcport permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.dstport

Filtre par port TCP destination.

## Exemple : tcp.dstport

tcp.dstport == 22

## Cas d'usage : tcp.dstport

Sur une capture réseau, tcp.dstport permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.flags.syn

Paquets avec flag SYN (début de connexion).

## Exemple : tcp.flags.syn

tcp.flags.syn == 1

## Cas d'usage : tcp.flags.syn

Sur une capture réseau, tcp.flags.syn permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.flags.ack

Paquets avec flag ACK.

## Exemple : tcp.flags.ack

tcp.flags.ack == 1

## Cas d'usage : tcp.flags.ack

Sur une capture réseau, tcp.flags.ack permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.flags.reset

Paquets avec flag RST (connexion reset).

## Exemple : tcp.flags.reset

tcp.flags.reset == 1

## Cas d'usage : tcp.flags.reset

Sur une capture réseau, tcp.flags.reset permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.flags.fin

Paquets avec flag FIN (fin de connexion).

## Exemple : tcp.flags.fin

tcp.flags.fin == 1

## Cas d'usage : tcp.flags.fin

Sur une capture réseau, tcp.flags.fin permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.flags.push

Paquets avec flag PSH.

## Exemple : tcp.flags.push

tcp.flags.push == 1

## Cas d'usage : tcp.flags.push

Sur une capture réseau, tcp.flags.push permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.stream

Filtre par flux TCP (numéro de stream).

## Exemple : tcp.stream

tcp.stream eq 42

## Cas d'usage : tcp.stream

Sur une capture réseau, tcp.stream permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.seq

Filtre par numéro de séquence.

## Exemple : tcp.seq

tcp.seq == 1000

## Cas d'usage : tcp.seq

Sur une capture réseau, tcp.seq permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.window_size

Filtre par taille de fenêtre (anomalies).

## Exemple : tcp.window_size

tcp.window_size < 1024

## Cas d'usage : tcp.window_size

Sur une capture réseau, tcp.window_size permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.analysis.flags

Paquets avec des problèmes d'analyse (retransmissions...).

## Exemple : tcp.analysis.flags

tcp.analysis.flags

## Cas d'usage : tcp.analysis.flags

Sur une capture réseau, tcp.analysis.flags permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.analysis.retransmission

Retransmissions TCP.

## Exemple : tcp.analysis.retransmission

tcp.analysis.retransmission

## Cas d'usage : tcp.analysis.retransmission

Sur une capture réseau, tcp.analysis.retransmission permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.analysis.zero_window

Fenêtre zéro (hôte submergé).

## Exemple : tcp.analysis.zero_window

tcp.analysis.zero_window

## Cas d'usage : tcp.analysis.zero_window

Sur une capture réseau, tcp.analysis.zero_window permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tcp.analysis.duplicate_ack

ACK dupliqués (perte de paquets).

## Exemple : tcp.analysis.duplicate_ack

tcp.analysis.duplicate_ack

## Cas d'usage : tcp.analysis.duplicate_ack

Sur une capture réseau, tcp.analysis.duplicate_ack permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## udp.port

Filtre par port UDP.

## Exemple : udp.port

udp.port == 53

## Cas d'usage : udp.port

Sur une capture réseau, udp.port permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## udp.length

Filtre par longueur UDP.

## Exemple : udp.length

udp.length > 1000

## Cas d'usage : udp.length

Sur une capture réseau, udp.length permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## http.request

Requêtes HTTP.

## Exemple : http.request

http.request

## Cas d'usage : http.request

Sur une capture réseau, http.request permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## http.response

Réponses HTTP.

## Exemple : http.response

http.response

## Cas d'usage : http.response

Sur une capture réseau, http.response permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## http.response.code

Filtre par code de réponse HTTP.

## Exemple : http.response.code

http.response.code == 404

## Cas d'usage : http.response.code

Sur une capture réseau, http.response.code permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## http.request.method

Filtre par méthode HTTP.

## Exemple : http.request.method

http.request.method == "POST"

## Cas d'usage : http.request.method

Sur une capture réseau, http.request.method permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## http.host

Filtre par hôte HTTP (Host header).

## Exemple : http.host

http.host == "evil.example.com"

## Cas d'usage : http.host

Sur une capture réseau, http.host permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## http.user_agent

Filtre par User-Agent.

## Exemple : http.user_agent

http.user_agent contains "curl"

## Cas d'usage : http.user_agent

Sur une capture réseau, http.user_agent permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## http.uri

Filtre par URI complète.

## Exemple : http.uri

http.uri contains "/admin"

## Cas d'usage : http.uri

Sur une capture réseau, http.uri permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## http.request.uri.query

Filtre par query string.

## Exemple : http.request.uri.query

http.request.uri.query contains "cmd="

## Cas d'usage : http.request.uri.query

Sur une capture réseau, http.request.uri.query permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## http.content_type

Filtre par type de contenu.

## Exemple : http.content_type

http.content_type == "application/x-www-form-urlencoded"

## Cas d'usage : http.content_type

Sur une capture réseau, http.content_type permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## http.authorization

Header Authorization (attention aux credentials en clair).

## Exemple : http.authorization

http.authorization

## Cas d'usage : http.authorization

Sur une capture réseau, http.authorization permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## http.cookie

Cookies HTTP.

## Exemple : http.cookie

http.cookie contains "sessionid"

## Cas d'usage : http.cookie

Sur une capture réseau, http.cookie permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## http2.headers

En-têtes HTTP/2.

## Exemple : http2.headers

http2.headers

## Cas d'usage : http2.headers

Sur une capture réseau, http2.headers permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## dns.qry.name

Filtre par nom de domaine interrogé.

## Exemple : dns.qry.name

dns.qry.name contains "pastebin.com"

## Cas d'usage : dns.qry.name

Sur une capture réseau, dns.qry.name permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## dns.flags.response

Distinguer requêtes (0) et réponses (1).

## Exemple : dns.flags.response

dns.flags.response == 1

## Cas d'usage : dns.flags.response

Sur une capture réseau, dns.flags.response permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## dns.qry.type

Type de requête DNS (1=A, 28=AAAA, 15=MX, 16=TXT).

## Exemple : dns.qry.type

dns.qry.type == 1

## Cas d'usage : dns.qry.type

Sur une capture réseau, dns.qry.type permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## dns.resp.ttl

TTL des réponses DNS (Tunneling DNS).

## Exemple : dns.resp.ttl

dns.resp.ttl < 60

## Cas d'usage : dns.resp.ttl

Sur une capture réseau, dns.resp.ttl permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## dns.len

Taille des paquets DNS (tunneling).

## Exemple : dns.len

dns.len > 200

## Cas d'usage : dns.len

Sur une capture réseau, dns.len permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## dns.txt

Champs TXT DNS (exfil).

## Exemple : dns.txt

dns.txt

## Cas d'usage : dns.txt

Sur une capture réseau, dns.txt permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tls.handshake.type

Filtre par type de handshake TLS (1=ClientHello).

## Exemple : tls.handshake.type

tls.handshake.type == 1

## Cas d'usage : tls.handshake.type

Sur une capture réseau, tls.handshake.type permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tls.handshake.extensions_server_name

SNI : le domaine demandé en clair dans TLS.

## Exemple : tls.handshake.extensions_server_name

tls.handshake.extensions_server_name contains "microsoft"

## Cas d'usage : tls.handshake.extensions_server_name

Sur une capture réseau, tls.handshake.extensions_server_name permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tls.record.version

Version TLS.

## Exemple : tls.record.version

tls.record.version == 0x0303

## Cas d'usage : tls.record.version

Sur une capture réseau, tls.record.version permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tls.alert_message

Alertes TLS (handshake échoués).

## Exemple : tls.alert_message

tls.alert_message

## Cas d'usage : tls.alert_message

Sur une capture réseau, tls.alert_message permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## tls.handshake.certificate

Certificats présentés.

## Exemple : tls.handshake.certificate

tls.handshake.certificate

## Cas d'usage : tls.handshake.certificate

Sur une capture réseau, tls.handshake.certificate permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## ssl.handshake.type

Ancien nom du filtre TLS (pré-Wireshark 3).

## Exemple : ssl.handshake.type

ssl.handshake.type == 1

## Cas d'usage : ssl.handshake.type

Sur une capture réseau, ssl.handshake.type permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## ftp.request.command

Commandes FTP.

## Exemple : ftp.request.command

ftp.request.command == "USER"

## Cas d'usage : ftp.request.command

Sur une capture réseau, ftp.request.command permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## ftp.response.code

Codes de réponse FTP.

## Exemple : ftp.response.code

ftp.response.code == 530

## Cas d'usage : ftp.response.code

Sur une capture réseau, ftp.response.code permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## smb2.cmd

Commandes SMB2 (numéro d'opcode).

## Exemple : smb2.cmd

smb2.cmd == 5

## Cas d'usage : smb2.cmd

Sur une capture réseau, smb2.cmd permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## smb2.filename

Fichiers accédés en SMB2.

## Exemple : smb2.filename

smb2.filename contains "password"

## Cas d'usage : smb2.filename

Sur une capture réseau, smb2.filename permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## smb2.nt_status

Statuts NT SMB2 (0xC000006A = bad password).

## Exemple : smb2.nt_status

smb2.nt_status == 0xc000006a

## Cas d'usage : smb2.nt_status

Sur une capture réseau, smb2.nt_status permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## smb2.access_mask

Masque d'accès SMB2.

## Exemple : smb2.access_mask

smb2.access_mask

## Cas d'usage : smb2.access_mask

Sur une capture réseau, smb2.access_mask permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## icmp.type

Type ICMP (8=echo request, 0=echo reply).

## Exemple : icmp.type

icmp.type == 8

## Cas d'usage : icmp.type

Sur une capture réseau, icmp.type permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## icmp.code

Code ICMP.

## Exemple : icmp.code

icmp.code == 0

## Cas d'usage : icmp.code

Sur une capture réseau, icmp.code permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## icmp.checksum

Checksum ICMP.

## Exemple : icmp.checksum

icmp.checksum

## Cas d'usage : icmp.checksum

Sur une capture réseau, icmp.checksum permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## arp.opcode

Opcode ARP (1=request, 2=reply).

## Exemple : arp.opcode

arp.opcode == 1

## Cas d'usage : arp.opcode

Sur une capture réseau, arp.opcode permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## arp.src.proto_ipv4

IP source des paquets ARP.

## Exemple : arp.src.proto_ipv4

arp.src.proto_ipv4 == 192.168.1.1

## Cas d'usage : arp.src.proto_ipv4

Sur une capture réseau, arp.src.proto_ipv4 permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## arp.duplicate-address-detected

Détection d'ARP spoofing (adresse dupliquée).

## Exemple : arp.duplicate-address-detected

arp.duplicate-address-detected

## Cas d'usage : arp.duplicate-address-detected

Sur une capture réseau, arp.duplicate-address-detected permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## dhcp.option.dhcp

Type de message DHCP (1=Discover, 2=Offer, 3=Request).

## Exemple : dhcp.option.dhcp

dhcp.option.dhcp == 3

## Cas d'usage : dhcp.option.dhcp

Sur une capture réseau, dhcp.option.dhcp permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## dhcp.option.hostname

Hostname déclaré en DHCP.

## Exemple : dhcp.option.hostname

dhcp.option.hostname contains "laptop"

## Cas d'usage : dhcp.option.hostname

Sur une capture réseau, dhcp.option.hostname permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## bootp.option.requested_ip

IP demandée en DHCP.

## Exemple : bootp.option.requested_ip

bootp.option.requested_ip == 192.168.1.50

## Cas d'usage : bootp.option.requested_ip

Sur une capture réseau, bootp.option.requested_ip permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## smtp.req.command

Commandes SMTP.

## Exemple : smtp.req.command

smtp.req.command == "RCPT"

## Cas d'usage : smtp.req.command

Sur une capture réseau, smtp.req.command permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## smtp.rsp.code

Codes de réponse SMTP.

## Exemple : smtp.rsp.code

smtp.rsp.code == 554

## Cas d'usage : smtp.rsp.code

Sur une capture réseau, smtp.rsp.code permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## imap.command

Commandes IMAP.

## Exemple : imap.command

imap.command == "LOGIN"

## Cas d'usage : imap.command

Sur une capture réseau, imap.command permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## pop.command

Commandes POP3.

## Exemple : pop.command

pop.command == "USER"

## Cas d'usage : pop.command

Sur une capture réseau, pop.command permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## kerberos.msg_type

Type de message Kerberos (10=AS-REQ, 11=AS-REP, 12=TGS-REQ).

## Exemple : kerberos.msg_type

kerberos.msg_type == 12

## Cas d'usage : kerberos.msg_type

Sur une capture réseau, kerberos.msg_type permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## kerberos.CNameString

Nom du principal dans Kerberos.

## Exemple : kerberos.CNameString

kerberos.CNameString contains "krbtgt"

## Cas d'usage : kerberos.CNameString

Sur une capture réseau, kerberos.CNameString permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## kerberos.cipher

Chiffre Kerberos (type d'encryption).

## Exemple : kerberos.cipher

kerberos.cipher == 18

## Cas d'usage : kerberos.cipher

Sur une capture réseau, kerberos.cipher permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## nbns.name

Noms NetBIOS.

## Exemple : nbns.name

nbns.name contains "DC01"

## Cas d'usage : nbns.name

Sur une capture réseau, nbns.name permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## nbss.name

Noms NetBIOS (session service).

## Exemple : nbss.name

nbss.name

## Cas d'usage : nbss.name

Sur une capture réseau, nbss.name permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## ldap.filter

Filtres LDAP.

## Exemple : ldap.filter

ldap.filter contains "userAccountControl"

## Cas d'usage : ldap.filter

Sur une capture réseau, ldap.filter permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## mysql.query

Requêtes MySQL.

## Exemple : mysql.query

mysql.query contains "SELECT"

## Cas d'usage : mysql.query

Sur une capture réseau, mysql.query permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## mongo.query

Requêtes MongoDB.

## Exemple : mongo.query

mongo.query

## Cas d'usage : mongo.query

Sur une capture réseau, mongo.query permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## websocket

Paquets WebSocket.

## Exemple : websocket

websocket

## Cas d'usage : websocket

Sur une capture réseau, websocket permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## frame.len

Taille des trames.

## Exemple : frame.len

frame.len > 1500

## Cas d'usage : frame.len

Sur une capture réseau, frame.len permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

## frame.time_delta

Délai depuis la trame précédente (beaconing).

## Exemple : frame.time_delta

frame.time_delta > 60

## Cas d'usage : frame.time_delta

Sur une capture réseau, frame.time_delta permet de filtrer rapidement les paquets pertinents avant d'exporter le flux. Combiner avec tshark en CLI pour automatiser l'analyse sur de gros PCAP.

