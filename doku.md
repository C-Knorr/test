# GoGreen GDV Dokumentation

* [Einführung](#einführung)

* [Konzept](#konzept)

* [Datenquellen](#datenquellen)

* [Datenauswertung und -aufbereitung](#datenauswertung)


## <a name="einführung"></a> Einführung 
Barcelonas Luftqualität während einer Pandemie

Dokumentation des Projektes Barcelonas Luftqualität während einer Pandemie im Rahmen des Wahlfaches Grundlagen der Datenvisualisierung des Wintersemesters 2020/2021 an der Hochschule Mannheim bei Herrn Prof. Dr. Till Nagel.

Die Coronapandemie hat Auswirkungen auf verschiedenster Ebenen auf der ganzen Welt. Zu Beginn der Pandemie war Spanien eines der betroffensten Ländern. Um das Verbreiten des Virus einzudämmen wählte Spanien im zweiten Quartal des Jahres 2020 den Weg des harten Lockdowns, der sich bis Juli 2020 hinzog. In diesem Projekt wird betrachtet, wie sich die Pandemie auf die Luftqualität der Stadt Barcelona ausgewirkt hat. Dabei betrachten wir neben den Luftqualitätsdaten und Coronainzidenz - und Todeszahlen zwischen dem 01.04.2019 und dem 31.12.2020 zusätzlich Maßnahmen, Einschränkungen und Ereignisse, die währenddessen stattfanden. Luftqualitätsdaten konnten hierbei aus dem Opendata Portal Barcelonas abgerufen werden. Es konnte festgestellt werden, dass manche Schadstoffarten während der Pandemie und vor allem während des harten Lockdowns deutlich weniger gemessen wurden als im Vergleichszeitraum des Vorjahres.

## <a name="konzept"></a> Konzept 

Im Rahmen der Vorlesung Grundlagen der Datenvisualisierung des Wintersemesters 2020/2021 ist dieses Projekt entstanden. Als vierköpfiges Team sollten wir urbane Daten einer Stadt mit mehr als 250.000 Einwohnern aus dem EU Raum auswählen, aufbereiten, analysieren und abschließend mit einer interaktiven Visualisierung angemessen darstellen. Relativ schnell nach Start des Projekts entstand innerhalb des Teams der Wunsch, Luftqualitätsdaten einer großen Stadt zu untersuchen. Die Luftqualität als zentrales Merkmal des Projekts auszuwählen war in unserem Interesse, da in unserem Team ein gesteigertes Umweltbewusstsein vorhanden ist und ein Gruppenmitglied aus Stuttgart, einer Stadt mit sehr hoher Luftbelastung, stammt.

Aufgrund eines umfangreichen Datenangebots des städtischen Open Data Portals, wurde die Stadt Barcelona ausgewählt. Als Untersuchungsmerkmal wurde zunächst die Verkehrsinfrafstruktur Barcelonas gewählt. Nach einer ausführlichen Datenauswertung, mit wenig vielversprechenden Erkenntnissen, und aufgrund der Aktualität entschieden wir uns allerdings dazu, die Luftqualitätsdaten im Zusammenhang mit der Coronapandemie zu betrachten. Dabei sollten Coronainzidenz- sowie Todeszahlen und weitergehende Ereignissdaten zur Coronapandemie eingebunden werden, um folgende Fragen zu beantworten:

* Hat die Coronapandemie maßgebliche Auswirkungen auf die Luftqualität in der Stadt Barcelona?

* Gab es Unterschiede und Änderungen in Bezug auf verschiedene Ereignisse und Einschränkungen, die während der Pandemie stattfanden?

* Gibt es einen Unterschied zwischen den verschiedenen Schadstoffarten?

* Gibt es Auffälligkeiten und Unterschiede zwischen den einzelnen Messstationen?

Unser Dashboard wurde dabei mit Plotly/Dash umgesetzt.

## <a name="datenquellen"></a> Datenquellen 
Als zentrale Datenquelle der Luftqualitätsdaten Barcelonas, wurde das [Open Data Portal](https://opendata-ajuntament.barcelona.cat/data/en/dataset) der Stadt Barcelona gewählt. Das Open Data Portal überzeugte hierbei durch eine großen Datenvielfalt und einer Sprachauswahlmöglichkeit, welche wir bei anderen Open Data Portalen, wie zum Beispiel das Datenportal Den Haags, vermisst haben. Gemessene Daten zur Luftqualität werden seit dem Jahr 2018 von sieben Messstationen auf diesem Portal zur Verfügung gestellt. Es werden Daten zu CO, NO, NO2, O3, PM10 und SO2 erhoben, wobei nicht alle Messstationen alle Schadstoffe messen. Aufgrund einer geänderten Datenstrukturierung seit April 2019, wurden ab diesem Zeitpunkt die Luftqualitätsdaten im Projekt verwendet. Ältere Daten konnten aufgrund der erfolgten Änderungen nicht sinnvoll verwendet werden. Die Daten lagen monatsweise im csv-Format vor.

Die im Projekt verwendeten Corona Infektions- und Todeszahlen der Stadt Barcelona, entstammen aus... und lagen für die einzelnen Monate im Format vor.

Die Ereignisse, die im angedachten Zeitstrahl der Coronainzidenzien dargestellt werden sollten, wurden aus verschiedenen Nachrichtenportalen entnommen.

Im Rahmen einer Anfrage an die Universitat Politècnica de Catalunya, einer technischen Universität in Barcelona, die eigene Luftmessstationen betreibt, erhofften wir uns weitere Luftqualitätsdaten zu erhalten, um eine breitere, aussagekräftigere Datenbasis zu erhalten. Zu unserem Bedauern konnten uns allerdings keine für unser Projekt hilfreiche Datensätze zur Verfügung gestellt werden.

## <a name="datenauswertung"></a> Datenauswertung und -aufbereitung 

Die Daten der spanischen Ereignisse rund um Corona wurden in einer csv-Datei zusammengefasst und mit dem jeweiligen Datum versehen.

Die Daten der Inzidenz- und Todeszahlen der einzelnen Monate wurden in einer Tabelle zusammengefasst. Fehlende Inzidenz- und Todeszahlen für Januar und Februar 2020 wurden mit dem Wert 0 ergänzt, um diese Daten in Rechnungen mit einzubeziehen und sinnvoll darstellen zu können.

Die Daten zur Luftqualität mussten zunächst aufbereitet werden, um diese in dem geplanten Umfang einsetzen zu können. Die csv-Dateien der einzelnen Monate wurden in einer Tabelle zusammengefasst. Zusätzlich wurden separate Tabellen für die einzelnen Schadstoffarten erzeugt, um Daten performanter einbinden zu können. 

Im Rahmen der explorativen Datenanalyse, wurden zunächst die Luftqualitätsdaten mit Hilfe der Software Tableau initial untersucht. Zunächst wurden die vorhandenen Daten auf Vollständigkeit und Extremwerte untersucht. Dabei fiel auf, dass an vereinzelten Tagen auffällig hohe Luftverschmutzungsdaten gemessen. Die gemessene Daten überstiegen den üblichen Rahmen um ein Vielfaches. Dennoch entschieden wir uns dafür diese Ausreißer nicht zu löschen und weiterzuverwenden, da stündliche Ausreißer in der durchschnittlichen Betrachtung weniger ins Gewicht fallen. Erste Auffälligkeiten im zeitlichen Verlauf wurden ebenfalls durch die Datenanalyse in Tableau festgestellt. Unterschiede und Schwankungen in Bezug auf die einzelnen Schadstoffarten konnten hierbei aufgedeckt werden. Die Erkenntnisse halfen dabei einordnen zu können, welche Schadstoffwerte überwiegend während der Pandemie im Vergleich zum Vorjahr abwichen und welche nicht.

Mit Hilfe von QGIS wurde die geografische Lage der Messstationen untersucht. Wir wollten uns ein erstes Bild verschaffen, wie die Messstationen innerhalb der Stadt verteilt und welche Charakteristika im Umkreis der Stationen vorhanden waren.

## Implementierung

### Anforderungen an die Implementierung

Aus der explorativen Datenanalyse und den daraus resultierenden Experimenten, wurden für den zu entwickelnden Prototyp im Hinblick auf die Untersuchungshypothese folgende Anforderungen an diesen entwickelt. Dabei wird im folgenden zwischen Anforderungen für die Visualisierung der Daten, sowie der Benutzung und Handhabe des Prototyps unterschieden.

**Visualisierungsanforderungen:**

- (1)  Visualisierung  gemessener Werte eines Schadstoffes und der Lokalität  an der dieser jeweils gemessen worden ist

- (2) Visualisierung eines Vergleichs der gemessenen Werte an den verschiedenen Orten/Messstationen

- (3) Visualisierung der Anzahl der festgestellten Infizierten an Covid-19

- (4) Todesfälle mit Covid-19

- (5) Regierungsmaßnahmen im zeitlichen Verlauf

- (6) Visualisierung von Messwerten eines Schadstoffes und der Zeitpunkt der Messung

- (7) Visualisierung von Messwerten von unterschiedlichen Schadstoffe/Schadstoffklassen im zeitlichen Verlauf

- (8) Visualisierung eines Vergleichs von Messwerten eines Schadstoffes in einem Jahr vor der Corona-Pandemie und dem Jahr 2020 zum jeweils gleichen Jahreszeitpunkt


- (9) Visualisierung eines Vergleichs eines gemessenen Wertes eines Schadstoffes an einem Ort im Vergleich zum Durchschnitt der gemessenen Werte an allen anderen Stationen
Neben den Anforderung für die Visualisierung stellen sich wie oben beschrieben auch gewisse Anforderungen zur Benutzung und Handhabe des Prototyps

**Usabilityanforderungen**

- (10) Möglichkeit zur Eingrenzung des zu betrachtenden Zeitraums für alle Visualisierungen

- (11)  Auswahlmöglichkeit zur Betrachtung der Schadstoffes

- (12)  Auswahlmöglichkeit der zeitlichen Aggregation für Visualisierungen über die Zeit

- (13) Auswahlmöglichkeit zur Betrachtung der Messwerte einer einzelnen Stationen

Eine Ausführliche Beschreibung der entwickelten Anforderung inklusive Begründungen finden sie in diesem weiterführenden Dokument.

### Visualisierung

Anhand dieser Anforderungen wurde folgendes Programm(siehe Bild) zur Visualisierung der Daten und damit verbundenen Untersuchung der Hypothese implementiert.


![Screenshot_Gesamt](Screenshot_Gesamt.png)

Für die Umsetzung von Anforderung 1 wurde ein Scatter-Geo/Bubble-Map implementiert.
![Scattergeo/Bubble-Map](Screenshot_Scattergeo.png)

Dieser ist oben links in der Gesamtansicht zu sehen. Durch das Zentrum der Kreise(Scatter/Bubble) wird der Standort der Messung bzw. der Messtation(Geographische Koordinate) auf einer Karte markiert. Die Größe der Kreise  zeigt dabei durchschnittlichen Messwert im gewählten Zeitraum(oben rechts) an dem jeweiligen Standort. Alternativ wurde auch die Darstellung als Choroplethenkarte in Betracht gezogen. Das wurde verworfen, da die Choroplethenkarte geographische Flächen betrachtet. Die untersuchten Messstationen messen in begrenztem Radius, sodass eine Übertragung auf eine größere geographische Fläche in diesem Fall nicht sinnvoll ist. Die Anzahl der Messstationen ist auch zu gering, um größer geographische Räume als eine Einheit zu betrachten. Die Größe des durchschnittlichen Messewerte, würde zudem bei einer Choroplethenkarte meist über Farbe kodiert werden. Das würde zu Schwierigkeiten bei der exakten Unterscheidung bei ähnlichen Werten führen. Bei Kreisen unterschiedlicher Größen ist das bei geringem Unterschied für den Betrachter einfacher. Damit kann auch die Umsetzung von Anforderung 2, Vergleich der Messtationen untereinander, unterstützt werden.
Der Vorteil einer Bubble-Map ist zudem, das in die Karte herein- und herausgezoomt werden kann, sodass das exakte Umfeld einer Messstation betrachtet werden kann(z.B. Park, Autobahn usw.) Das wäre bei einer gefärbten Choroplethenkarte nur sehr schwer möglich.
Die Bubble-Map bietet außerdem den Vorteil, dass über die Farbe der Kreise, weitere Informationen visualisiert werden können. Dieser Vorteil wurde für die Umsetzung der Anforderung 13 genutzt. Die Bubbles haben zunächst einen einheitliche Farbe(schwarz). Der Prototyp wurde so programmiert, dass über ein Klick auf einen der Scatter die entsprechende Station ausgewählt werden kann. Diese Bubble erscheint nun in der Farbe rot und die  gemssenen Werteverläufe der ausgewählten Station werden nun in den unteren beiden Graphen in der gleichen Farbe(rot) gezeigt. Dadurch wird eine farbliche Konsistenz geschaffen. Die Alternative jeder Station exakt eine individuelle Farbe wurde verworfen, da die Stationenanzahl zum einen zu hoch ist um jeder Station eine wirklich für den Betrachter auf Anhieb unterscheidbare Farben zu bieten und damit eine leichte zu entstehende Verbindung zwischen Station/Lokalität und Farbe zu gewährleisten, als auch dass die Stationen sich je nach Schadstoffklasse zu sehr von Ihrer Lokalität unterscheiden. Selbst bei nur kleinen Veränderungen wie von einer Straßenkreuzung zur nächsten Straßenkreuzung bei gleicher Benennung der Station, wäre ein Beibehalten der Farbe ein inhaltliche Irreführung auf Grund des begrenzten Messradius einer Messstation.

Für die Umsetzung der Anforderung 4-7 wurde ein Liniendiagramm gewählt.
![Screenshot_Pandemieverlauf](Screenshot_Pandemieverlauf.png)

Liniendiagramme sind für kontinuierliche Zeitreihendaten, wie die Anzahl der Corona-Infizierten, der Todesfälle und auch der Schadstoffmesswerte, eine angemessene Visualisierung. Im folgenden Liniendiagramm(siehe Bild) wurden die Anzahl der Infizierten, die Todesfälle und die Regierungsmaßnahmen visualisiert. In blauer Farbe ist die Anzahl der Covid-19-Infizierten codiert und  in gelb die Anzahl der Todesfälle in Covid-19 zum jeweiligen Zeitpunkt. Mit grauen vertikalen Balken, jeweils eine in Kraft treten eine Regierungsmaßnahme. Dabei gilt für alle drei Werte, die gleiche x-Achse, welches der kalendarischen Jahresverlauf des Jahres 2020 ist. Somit wird der zeitliche Zusammenhang sehr deutlich. Die y-Achse hingegen ist nicht für alle in diesem Liniendiagramm dargestellten Informationen einheitlich: für die Anzahl der Infizierten gilt die y-Achsenskalierung auf der linken Seite, für die Anzahl der Anzahl der Todesfälle die y-Achsenskalierung auf der rechten Seite(siehe Bild). Für die unterschiedliche y-Achsenskalierung wurde sich entschieden, da bei einer einheitlichen y-Achsenskalierung, der Verlauf der Anzahl Todesfälle auf Grund des großen absoluten Unterschiedes in der Anzahl zur Anzahl der Infizierten, weniger deutlich erkennbar ist. Auch eine getrennte Darstellung der Verläufe hätte den Nachteil, das der zeitliche Zusammenhang zwischen Infizierungsanzahl, Todesanzahl und Regierungsmaßnahme weniger sichtbar wird.

Für die gemessenen Werte eines Schadstoffes wurde folgendes Liniendiagramm programmiert.

![Screenshot_Schadstoffverlauf_ohne_Vergleich](Screenshot_Schadstoffverlauf_ohne_Vergleich.png)

Dabei wird auf der x-Achse als Einteilung der allgemeine kalendarische Jahresverlauf genutzt(01.01.-31.12). So ist ein direkter Vergleich von den gemessenen Werten aus dem Jahr 2019 vor der Pandemie(dargestellt als gestrichelte Linie: - - -) und den gemessenen Werten aus dem Pandemiejahr 2020 möglich (Anforderung 8). Bei exakter chronologischer Einteilung(1.1.2019 – 31.12.2020) wäre der Vergleich schwieriger ersichtlich, da nur eine kontinuierliche Linie abgebildet wäre und an zwei verschiedenen x-Positionen suchen müsste.
Auf der y-Achse ist entsprechend des Schadstoffes die passende Werteskalierung anhand der gemessenen Werte in der für den Schadstoff entsprechenden Einheit zu finden. Die Farbe schwarz, die Defaultfarbe aller Bubbles in der Bubble-Map, zeigt dabei den Durchschnittswert über alle Stationen hinweg. Wird wie bei der Bubble-Map beschrieben eine Station ausgewählt und dadurch diese in der Karte rot markiert, erscheint in gleichem Rot, ebenso wieder in gestrichelt, die Werte dieser Station im Jahr 2019 und in durchgezogener Linie die Werte der ausgewählten Station aus dem Jahr 2020.

![Screenshot_Schadstoffverlauf_mit_Vergleich](Screenshot_Schadstoffverlauf_mit_Vergleich.png)

Durch diese Farbkonsistenz wird eine direkte inhaltliche Verbindung zwischen Karte und Liniendiagramm geschaffen. Eine Legende zeigt das zusätzlich noch einmal an. Somit ist eine Einordnung der Station zur Gesamtsituation möglich(Anforderung 9)
Eine alternative Darstellung der verschiedenen Werteverläufe in Form  eines Flächendiagramms, dass ebenso für Zeitreihen geeignet ist, oder in Form eines unstacked-Barcharts erwiesen sich schlecht, da der direkte Vergleich zwischen 2019 und 2020 bei gleichzeitigem Vergleich von Durchschnitt aller Stationen und einer Station, als schwierig ersichtlich sowie der ganze Graph insgesamt unübersichtlich wirkt.
Ebenso unübersichtlich wirkte es die Wertverläufe aller gemessenen Schadstoffe in einen Graph zu visualisieren. Die Alternative der gleichzeitigen Darstellung aller Schadstoffe in Form  eines Small-Multiples wurde als gut betrachtet, in Zusammenspiel mit dem Scatter-Geo aber als  unpassend. So wären auf an fast allen Koordinaten mehrere sich überlagernde Kreise, da an einer Station meist zu mehreren Schadstoffen gleichzeitig Werte erhoben wurden. Erschwerend kommt hinzu, dass an vielen Stationen nicht alle Schadstoffen aufgezeichnet worden sind.

Um dennoch alle Schadstoffe berücksichtigen zu können(Anforderung 11), wurde folgendes Bedienelement implementiert.

![Screenshot_Bedienelement](Screenshot_Bedienelement.png)

Dort ist es möglich exakt einen der Schadstoffe auszuwählen. Je nach Auswahl zeigen die Karte als auch die unteren beiden Linegraphen die entsprechenden Werte des ausgewählten Schadstoffes an. Ebenso ist es möglich den betrachteten Zeitraum über das Bedienungselement einzuschränken(Anforderung 10). Alle Graphen passen sich dem entsprechend an um auch hier wieder eine zeitliche Konsistenz zu gewährleisten. Ebenso ist es hier möglich, die zeitliche Aggregation zu bestimmen(Anforderung 11). Auswahl besteht zwischen Tag, Woche, Monat. Das wirkt sich auch hier auf alle Graphen aus, ist aber besonders wichtig für den untersten Linegraph.

![Screenshot_Durchschnittsverlauf](Screenshot_Durchschnitssverlauf.png)

Dieser zeigt je nach Auswahl den durchschnittlichen Verlauf innerhalb eines Tages(0.00 Uhr bis 23.59), einer Woche(Montag bis Sonntag) oder innerhalb eines Monats(1. Tag des Monats bis zum 31. Tag eines Monats an) an. Wie beim obendrüber sich befindlichen Linegraph werden alle dort bekannten Visualisierungsmuster übernommen(schwarz gestrichelt: Durchschnittlicher Werteverlauf von allen Stationen 2019, schwarz durchgezogen:  Durchschnittlicher Werteverlauf von allen Stationen 2020, rot gestrichelt: Werteverlauf der im Scatter-Geo ausgewählten Station 2019, rot durchgezogen: Werteverlauf der im Scatter-Geo ausgewählten Station 2020)

In der Infobox wird zur Schlagzahleinordnung und groben Zusammenfassung  die absoluten Zahlen zum Durchschnittsmesswert aller Stationen entsprechend dem ausgewähltem Schadstoff im gewählten Zeitraum angezeigt.

![Infobox](Screenshot_Infobox.png)

Ebenso wird in tabellarischer Form die absoluten Zahlen der Covid-19-Infizierten und Todesfälle mit Covid-19 in dem gewählten Zeitraum angezeigt.

### Tools

Für die Umsetzung der Visualisierung wurden hauptsächlich Tools gesucht, die eine hohe Interaktivität zwischen den verschiedenen Graphen bietet, sodass ein Benutzer, schnell die Ansicht seiner Wahl erhält. Deshalb kamen Altair, plotly/dash als auch d3.js in Betracht. Altair ist ein Visualisierungsbibliothek in Python welche auf auf Vega/Vega-Lite basiert. Mit Altair ist es mit sehr geringem Implementieraufwand möglich alle gängigen Visualisierungstypen zu implementieren. Allerdings sind bei der Interaktivität und der Individualisierung der einzelnen Visualisierungen schnell die Grenzen erreicht. Das wäre bei d3.js nicht der Fall. D3 bietet alle Freiheiten der Gestaltung und Implementierung. Allerdings ist der Programmieraufwand sehr hoch. Hinzukommt, dass das Erlernen sich als schwierig gestaltet auf Grund von schwächen in der Dokumentation und Inkompatibilitäten von Versionen.
Deshalb wurde dieser Prototyp mit plotly/Dash implementiert. Plotly ist ein mächtige Visualisierungsbibliothek in der Programmiersprache Python, welches die Möglichkeit zu Realisierung aller bekannten Visualisierungstechnicken mit großer Möglichkeit zur Individualisierung bietet. Über das damit verbundene Framework Dash, lassen sich die mit Plotly programmierten Visualisierung in HTML-Seiten einbinden und gleichzeitig Interaktivität zwischen den Graphen herstellen.(Bild) Über CSS lässt sich zudem das weitere Erscheinungsbild neben der Graphen komplett individualisieren. Darüber hinaus bestand innerhalb des Teams Erfahrung mit Python sowie mit plotly/Dash.
