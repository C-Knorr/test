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
Als zentrale Datenquelle der Luftqualitätsdaten Barcelonas, wurde das [Open Data Portal](https://opendata-ajuntament.barcelona.cat/data/en/dataset) der Stadt Barcelona gewählt. Das Open Data Portal überzeugte hierbei durch eine großen Datenvielfalt und einer Sprachauswahlmöglichkeit, welche wir bei anderen Open Data Portalen, wie zum Beispiel das Datenportal Amsterdams, vermisst haben. Gemessene Daten zur Luftqualität werden seit dem Jahr 2018 von sieben Messstationen auf diesem Portal zur Verfügung gestellt. Es werden Daten zu CO, NO, NO2, O3, PM10 und SO2 erhoben, wobei nicht alle Messstationen alle Schadstoffe messen. Aufgrund einer geänderten Datenstrukturierung seit April 2019, wurden ab diesem Zeitpunkt die Luftqualitätsdaten im Projekt verwendet. Ältere Daten konnten aufgrund der erfolgten Änderungen nicht sinnvoll verwendet werden. Die Daten lagen monatsweise im csv-Format vor.

Die im Projekt verwendeten Corona Infektions- und Todeszahlen der Stadt Barcelona, entstammen aus... und lagen für die einzelnen Monate im Format vor.

Die Ereignisse, die im angedachten Zeitstrahl der Coronainzidenzien dargestellt werden sollten, wurden aus verschiedenen Nachrichtenportalen entnommen.

Im Rahmen einer Anfrage an die Universitat Politècnica de Catalunya, einer technischen Universität in Barcelona, die eigene Luftmessstationen betreibt, erhofften wir uns weitere Luftqualitätsdaten zu erhalten, um eine breitere, aussagekräftigere Datenbasis zu erhalten. Zu unserem Bedauern konnten uns allerdings keine für unser Projekt hilfreiche Datensätze zur Verfügung gestellt werden.

## <a name="datenauswertung"></a> Datenauswertung und -aufbereitung 

Die Daten der spanischen Ereignisse rund um Corona wurden in einer Exceldatei aggregiert und mit dem jeweiligen Datum versehen. Um die Datei in einem Graphen abbilden zu können, wurde der Hilfswert "X" für alle Einträge eingefügt.

Die Daten der Inzidenz- und Todeszahlen der einzelnen Monate wurden in einer Tabelle zusammengefasst. Fehlende Inzidenz- und Todeszahlen für Januar und Februar 2020 wurden mit dem Wert 0 ergänzt, um diese Daten in Rechnungen mit einzubeziehen.

Die Daten zur Luftqualität mussten zunächst bearbeitet werden, um diese in dem geplanten Umfang einsetzen zu können. Die csv-Dateien der einzelnen Monate wurden in einer Tabelle zusammengefasst. Zusätzlich wurden separate Tabellen für die einzelnen Schadstoffarten erzeugt, um performantere Daten einbinden zu können. Zudem galt es, die Messstationskoordinaten, die im Format ED50 vorlagen, umzuwandeln, um diese weiterzuverwenden zu können. Mit der Software QGIS wurden die Koordinaten in das Format WGS84 transformiert. Dieses Koordinatenformat konnte im weiteren Verlauf in verschiedenen Programmen problemlos zur Darstellung eingesetzt werden.

Im Rahmen der explorativen Datenanalyse, wurden zunächst die Luftqualitätsdaten mit Hilfe der Software Tableau initial untersucht. Zunächst wurden die vorhandenen Daten auf Vollständigkeit und Extreme untersucht. Dabei fiel auf, dass an vereinzelten Tagen auffällig hohe Luftverschmutzungsdaten gemessen. Die gemessene Daten überstiegen den üblichen Rahmen um ein vielfaches. Dennoch entschieden wir uns dafür diese Ausreißer nicht zu löschen und weiterzuverwenden. Erste Auffälligkeiten im zeitlichen wurden ebenfalls durch die Datenanalyse in Tableau festgestellt. Unterschiede und Schwankungen in Bezug auf die einzelnen Schadstoffarten konnten hierbei aufgedeckt werden. Die Erkenntnisse halfen dabei einordnen zu können, welche Schadstoffwerte überwiegend während der Pandemie im Vergleich zum Vorjahr abwichen und welche nicht.

Mit Hilfe von QGIS wurde die geografische Lage der Messstationen untersucht. Wir wollten uns ein erstes Bild verschaffen, wie die Messstationen innerhalb der Stadt verteilt waren und welche Charakteristika im Umkreis der Stationen vorhanden waren.





