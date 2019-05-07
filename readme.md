# Datenintensive und datenfokussierte Aktivitäten in der Stadtbibliothek Gelsenkirchen

## Einleitung

Die Digitalisierung ermöglicht in der heutigen Zeit einen äußerst effizienten Informationsaustausch. Diese Entwicklung ist im so genannten Informationszeitalter unverzichtbar und Institutionen wie Stadtbibliotheken machen sich die Möglichkeiten, Informationen über Netzwerke, zwischen Datenbanken oder zwischen zwei Computern zu senden, zunutze, um diese Informationen innerhalb der eigenen Strukturen auszutauschen oder aus externen Quellen zu importieren. Dadurch können Synergien geschaffen werden, die ein effizienteres Arbeiten und das schnellere Erhalten von aktuellen Informationen ermöglichen. Zudem können bestimmte Arbeitsschritte zielführend automatisiert werden.   
Die Stadtbibliothek Gelsenkirchen bezieht Daten über bestimmte Schnittstellen von externen Institutionen und Firmen, um diese innerhalb der eigenen Organisation weiterzuverwenden und für eigene Zwecke aufzubereiten. Außerdem nutzt die Stadtbibliothek die digitale Infrastruktur der Stadt, um beispielsweise Dokumente zur kooperativen Bearbeitung auf einem zentralen Speicher dem Bibliothekspersonal zur Verfügung zu stellen. Diese Datenvorhaltungen und -flüsse sollen im Folgenden beschrieben werden, um im Anschluss ein Beispiel herauszustellen, das mit Blick auf Verbesserungspotenzial genauer beleuchtet wird. Eine Projektskizze soll dazu dienen, den Ablauf der Implementierung zu umreißen.

## 1. Datenströme und -vorhaltungen in der Stadtbibliothek Gelsenkirchen

Die Stadtbibliothek Gelsenkirchen bezieht aus externen Quellen bestimmte Metdadaten, um diese im eigenen Katalog weiterzuverwenden. Außerdem werden über Netzlaufwerke Daten zwischen dem Bibliothekspersonal, aber auch zwischen Bibliotheksnutzer*innen ausgetauscht. Das Content Management System (CMS) Sharepoint wird als so genanntes Wiki verwendet, damit Informationen bereitgestellt und vom Personal direkt zur Recherche hinterlegt werden können. Die Stadtbibliothek Gelsenkirchen sammelt, katalogisiert und verwaltet ihren Bestand mit dem Bibliothekssystem [BIBDIA](https://www.axiell.de/bibdia/) von der [Firma AXIELL](https://www.axiell.de/). 

  ### 1.1 Import von Metadaten aus externen Quellen in den OPAC 

Um die Katalogisierung der neu eingegangenen Medien der Stadtbibliothek effizient zu gestalten, werden die Titel- und Normdaten aus der Deutschen Nationalbibliothek (DNB) heruntergeladen. Anstatt sämtliche Normdaten aus dem vorliegenden Medium zu [autopsieren](https://de.wikipedia.org/wiki/Autopsie_(Bibliothekswesen)), wird der [Datenshop](https://www.dnb.de/DE/Header/Hilfe/datenshop.html) der DNB genutzt, um die Metadaten direkt in das Bibliothekssystem zu laden. Hierfür wird das maschinenlesbare Austauschformat [MARC21](https://www.dnb.de/DE/Standardisierung/Formate/MARC21/marc21_node.html) verwendet. Überdies sei erwähnt, dass zur Kataloganreicherung, auch [Catalogue Enrichment](https://www.hbz-nrw.de/produkte/digitalisierung/catalogue-enrichment) genannt, zum größten Teil das Angebot des [Hochschulbibliothekszentrums NRW](https://www.hbz-nrw.de/ueber-uns) (hbz) genutzt wird. Auch hier werden mit MARC21 etwa Inhaltsverzeichnisse oder Buchcover hochgeladen. Nach Rücksprache mit der Projektkoordination Catalogue Enrichment* gibt es jedoch keine sonderlich hohe Priorität zur Digitalisierung der Buchcover von Seiten des hbz. Dies führt zu einem Mangel an Bildern und so musste eine andere Lösung gefunden werden, damit für möglichst jedes Medium auch ein Buchcover angeboten werden kann. Aus diesem Grund hat die Stadt Gelsenkirchen einen Vertrag mit Amazon geschlossen, um Zugriff auf deren Buchcover zu erhalten. Wenn der [OPAC](https://katalog.stadtbibliothek-ge.de/opax/de/qsim.html.S) aufgerufen und eine beliebige Suche durchgeführt wird, kann davon ausgegangen werden, das ein Großteil der bereitgestellten Coverbilder von Amazon ist. Ein Klick auf ein Cover führt dann zu dem Titel auf der Website von Amazon. Dies wird in der Bibliothekslandschaft [kontrovers diskutiert](https://www.kribiblio.de/?p=681), aber auch von Nutzer*innen unter Umständen als [kritisch 
wahrgenommen](https://www.bib-info.de/verband/publikationen/aktuell.html?tx_ttnews%5Btt_news%5D=4524&cHash=d764971a32). Gleichwohl wurden andere Lösungen in Betracht gezogen, aufgrund der zusätzlichen Einnahmequelle, die das so genannte [Affiliate-Programm von Amazon](https://partnernet.amazon.de/) bietet, jedoch deutlich weniger favorisiert. 

*E-Mail-Korrespondenz hat Sperrvermerk – wird auf Anfrage gern zugesendet
 
  ### 1.2 Import von Fremddaten aus Digitale Virtuelle Bibliotheken in den OPAC 

Einen anderen Bezugsweg für Metadaten im Bibliothekskatalog haben die digitalen Medien. Titel- und Normdaten für die im OPAC ausgewiesenen eBooks, ePapers, eAudios u.a. werden über die [Onleihe](http://www.onleihe.net/) bezogen. Die Onleihe gehört zur [Digitale Virtuelle Bibliotheken](http://www.onleihe.net/unternehmen.html) (divibib), welche zur so genannten [ekz 
Gruppe](http://www.onleihe.net/unternehmen/die-ekz-gruppe.html) gehört. Für die Titel der Onleihe werden sämtliche Metadaten im MAB/MARC Format von der divibib bereitgestellt. Die Stadtbibliothek bezieht auch hier für sämtliche lizenzierten digitalen Titel die Titeldaten im MARC21 Format, um sie im eigenen OPAC zu präsentieren. Jedoch werden z.B. keine Buchcover mit bezogen, sondern auf der Ergebnisseite ein Hinweis „Downloadtitel“ angezeigt. Ein Link auf derselben Seite mit der Bezeichnung „Titel nur digital verfügbar; zur Ausleihe bitte hier klicken!“ führt dann auf die [externe Seite](https://ebib.onleihe.de/gelsenkirchen/frontend/welcome,51-0-0-100-0-0-1-0-0-0-0.html) der Onleihe. Diese Webseite wird nicht von Gelsenkirchen selbst gehostet. Die divibib präsentiert hier die lizenzierten Titel der Stadtbibliothek Gelsenkirchen und dort finden sich auch die Kataloganreicherungen, die Nutzer*innen ausführlichere Informationen bieten als diejenigen im OPAC.

### 1.3 Datenaustausch über Netzlaufwerke der Stadtbibliothek Gelsenkirchen

Um anfallende Daten für das [Referat 40 Bildung](https://www.gelsenkirchen.de/de/rathaus/politik_und_verwaltung/Vorstandsbereiche_und_Dienststellen/33632-referat-40-bildung) zu speichern, wurde ein Netzlaufwerk eingerichtet. Dieses Netzlaufwerk hat eine Gesamtspeicherkapazität von ca. 8 TB und muss sämtliche Dokumente, Bilder, Filmmaterialien, Logos etc. für das gesamte Referat bereitstellen. Die Stadtbibliothek hat Zugriff auf eine [Partition](https://www.itwissen.info/partition-Partition.html) in der Größe von ca. 1,5 TB. Diese Partition enthält einen Netzwerkordner, der an jedem Arbeitsplatz der Stadtbibliothek denselben Zugriff auf die dort gespeicherten Daten anbietet. In diesem Netzwerkordner können sämtliche Daten vom gesamten Personal der Stadtbibliothek eingesehen und verändert werden. Ein [RAID](https://www.elektronik-kompendium.de/sites/com/1001011.htm) unterstützt die Datensicherheit und kann bei einem kritischen Ausfall der Hardware einen Verlust verhindern. Herauszustellen ist noch, dass die Partitionen für die Abteilungen Querschnittmanagement, Schul- und Bildungsentwicklung, Schulbetrieb, Stadtbibliothek und Volkshochschule nur von den jeweiligen Abteilungen einzusehen sind. So hat ein Mitarbeiter der Stadtbibliothek etwa keinen Zugriff auf die anderen vier Partitionen des Netzlaufwerks, sondern nur auf die eigene Partition, hier aber dann auf jeden Ordner.
Des Weiteren gibt es ein Netzlaufwerk für den Computerraum namens [log in](https://stadtbibliothek.gelsenkirchen.de/Homepage/Bibliotheken/Medienzentrum/login.asp). Hier kommt das so genannte [Sneaker 
Net](https://www.bet.de/lexikon/sneakernet/) zum Einsatz. Eine externe Festplatte wird wöchentlich an den Server des log ins angeschlossen, auf welche sämtliche Daten aus dem Netzlaufwerk gesichert werden. Da dies aufgrund der eingeschränkten Funktionen des Windows Explorers jedoch sehr mühselig ist, wird diese Problemstellung im zweiten Punkt genauer behandelt werden.

  ### 1.4 Bereitstellung von Informationen über Sharepoint zu internen Zwecken
 
Das [Content Management System](https://wirtschaftslexikon.gabler.de/definition/content-management-system-cms-31303) (CMS) [Sharepoint](https://products.office.com/de-de/sharepoint/collaboration) dient als 
[Enterprise Wiki](https://it-service.network/blog/2017/07/20/enterprise-wiki-chancen-und-risiken/). Hier wird bibliotheksinternes Wissen in Wikipedia-Form vom Bibliothekspersonal vorgehalten, gepflegt und aktualisiert: Von Anleitungen bei Mahnfällen bis hin zum Umgang mit dem 3D-Drucker ist hier das Spezialwissen des Bibliothekspersonals hinterlegt und per Schlagwörter durchsuchbar gemacht (die Anleitung 3D-Druck befindet sich auf z.B. auf folgendem Pfad in Sharepoint: Technik/3D-Druck/Bedienungsanleitung).

## 2. Implementierung eines Backupprogramms für den Netzwerkordner des Computerraums

Insgesamt werden 14 PCs mit Windows 10 für die Nutzer*innen im *log in*, dem Computerraum der Stadtbibliothek Gelsenkirchen, bereitgestellt, gepflegt und gewartet. Hier finden zum einen von Lehrern, Freiberuflern und Ehrenamtlichen für SchülerInnen und Interessierten veranstaltete Kurse statt, die also nur indirekt von der Stadtbibliothek vermittelt sind. Dazu gehören Veranstaltungsformate wie beispielsweise Schulradio, Programmierkurse oder Literaturkurse, aber auch Vereine und Organisationen können den Raum für Bewerbungstrainings, Sprachkurse, Seniorenradio u.v.m nutzen. Zum anderen wird der Computerraum direkt für Veranstaltungen von der Stadtbibliothek genutzt für eBook-Schulungen, 3D-Druck-Workshops und Bibliothekseinführungen. Nicht zuletzt dient er für interne Zwecke, so für Mitarbeiterschulungen oder Telefonkonferenzen über Internet-Videotelefonie etwa mit den Zweigstellen der Stadtbibliothek. 
Die genannten 14 PCs im log in sind [Clients](https://www.itwissen.info/Client-client.html) eines [Windows-Server 2012R2](https://de.wikipedia.org/wiki/Microsoft_Windows_Server_2012#Windows_Server_2012_R2). Angeordnet sind sie in einer [Sterntopologie](https://www.itwissen.info/Sterntopologie-star-topology.html), verbunden über einen [Switch](https://www.itwissen.info/Switch-switch.html). Der Windows Server dient als Druck- und Dateiserver. Neben einem angeschlossenen [Netzwerkdrucker](https://www.itwissen.info/Netzwerkdrucker-network-printer.html) befindet sich auch ein Netzlaufwerk auf dem Server, auf das alle Clients Zugriff haben. Jedes Backup des Netzwerkspeichers wird über den Dateimanager, [Windows-Explorer](https://de.wikipedia.org/wiki/Windows-Explorer), des Windows Servers manuell durchgeführt. Auf dem Server selbst befinden sich ca. 500 GB Daten, die in den genannten Veranstaltungen fortwährend verändert, erweitert oder gelöscht werden. Durch die limitierte Funktion des Windows-Explorers lässt sich manuell nur sehr aufwändig feststellen, welche Dateien nun fehlen, verändert oder neu erstellt wurden. Deshalb wäre ein automatisiertes wöchentliches [monitoring](https://www.itwissen.info/Monitoring-monitoring.html) und Backup von geänderten Daten ein deutlich effizienteres und zudem transparenteres Vorgehen, die Daten des Netzwerkordners zu sichern.

Die Herausforderung hierbei ist, einerseits ein geeignetes Programm zu erstellen, welches über Nacht die Sicherung durchführt und andererseits die korrekte Hardware zu nutzen. So gilt es z.B. zu beachten dass der [Datendurchsatz](https://www.itwissen.info/Datendurchsatz-data-throughput.html) stimmen muss, da ansonsten die Sicherung zu lange dauern könnte und den Start der nächsten Veranstaltung behindern könnte. Ein erster Gedanke, einen [Einplatinencomputer](https://www.itwissen.info/Einplatinencomputer-single-board-computer-SBC.html) zu nutzen, wurde nach kurzer Recherche verworfen, da die Performance unter Umständen hier nicht ausreicht. Es sei dabei erwähnt, dass das [übertakten](https://www.informatik-verstehen.de/lexikon/overclocking/) zu einer eventuell ausreichenden Leistungssteigerung führen kann, jedoch ist dies mit Risiken verbunden und erfordert ein Know-how, das nicht vorhanden ist. 
Die andere präferierte Variante ist, einen der vorhandenen Client-PCs mit einer zweiten Partition auszustatten und auf diese Partition [Linux Ubuntu](https://www.itwissen.info/Ubuntu-ubuntu.html) zu installieren. 

Das Backup-Programm soll direkt beim Start von Ubuntu ausgeführt werden. Zurzeit werden noch Möglichkeiten ermittelt, um über das [BIOS](https://de.wikipedia.org/wiki/BIOS) ein [Wake-on-lan](https://www.itwissen.info/WOL-wake-on-LAN.html) einzurichten und so das Backup aus der Ferne zu starten. 


