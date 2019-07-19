# Internet Protokolle (Einführung)

## Nachrichtenaustausch im Internet erfordert
1. Eindeutige Festlegung des Adressaten der Nachricht
2. Ermittlung des Übertragungsweges im Netwerk
3. Übermittlung vollständiger Nachrichten (Paketvermittlung)
4. Fehlerfreie Nachrichtenübermittlung

# Schichtenmodelle

## Netzwerkbetriebssysteme muss sehr komplexe Kommunikationsaufgaben lösen

* Aufteilung in verschieden Schichten oder Layer -> Schichtenmodell
* Jede Schicht ist verantwortlich für die Lösung eines Teilsproblems

1. Unterste Schicht müssen physikalische Signale ausgetauscht werden
2. Zweite Ebene werden Binärdaten in physikalische Signale umgesetzt
3. Binärdaten müssen mit Transportinformationen versehen und markiert werden

### Sender und Empfänger folgen dem gleichen Schichtenmodell
### Schichten kommunizieren mit den gleichen Kommunikationsprotokollen

* Schichtenmoddel sind hierarchisch organisiert: jede Schicht kommuniziert jeweils nur mit den direkt benachbarten Schichten 

## Arten von Schichtenmodellen

### ISO/OSI-Referenzmodell - Protokollfamilie im Telekommunikationsbereich
### TCP/IP-Stack - implementier in der TCP/IP-Internet- Protokollsuite
###  1. Application Layer
* FTP
* HTTP
* SMTP
###  2. Transport Layer
* zuverlässigen Datentransport
* gesicherte Qualitätskontrolle
* Datenflusskontrolle
###  3. Internet Layer
* Routing
###  4. Link Layer, Netzzugangsschicht

* Logische Einheiten werden gebildet
* Gruppierung der Bitströme (Datenpakete)

+ ### Funktionale Trennung in die Aufgabenbereiche
1. Media Access Control - MAC
* Steuerung des Zugriffs aus Übetragungsmedium
* bekannte MAC-Protokoll: Ethernet, Token Ring, FDDI
2. Logical Link Control - LLC
* Verwaltung der logischen Verbindungen einschließlich Fehleranalyse und Kontrolle
## Hardware Layer- gehört nicht zum Stack
* elektrischen, meschanische, funktionale, .. Parameter zur Übertragung notwendig
* direkt unterhalb des TCP-IP-Stapels

### Jeder der beteiligten Schichten fügt den eigentlichen Nutzdaten eigen Fluss- und Verwaltungsinformationen hinzu - > Overhead


# Sinn und Zweck des Internets
* Netzanwendungen verfügbar zu machen
* Filetransfer, Email, WWW, P2P-Netzwerke, Soziale Netze
* Internetanwendungen basieren auf Diensten und Anwendungen, die im Application Layer genutzt werden

## Internetanwedungen Vorraussetzungen
* zwei kommunizierende Rechner, genauer
* zwei Anwendungen, nocht genauer, 
* zwei Prozesse, die Instanzen  dieser Anwendung bilden

### Kommuniaktion folgt dem Client/Server-Prinzip
* Client forder beim Server Dienstleistungen an, die dieser leistet oder mit einer Fehlermeldung quittiert
1. Fehlermeldung
2. Nicht bereit

### Typische Dienste
* Verzeichnisdienste (DNS, LDAP)
* Nachrichtenaustausch- und der Informationsdienste (Emails, Emailserver)
* Simple Mail Transfer Protokoll (SMTP) (nur Text-Nachrichten)
* POP3 (komplette Email wird geladen) und IMAP für Abrufen von Emails
* MIME-Standards können neben Text auch andere Datenformate übertragen werden
* Emails können sicher mit PGP oder S/MIME übertragen werden

* Datentransferdienste
+ WWW. Word wide web (WWW: Client = Browser, intuitive Benutzeroberfläche)

## Ende der Vorlesung