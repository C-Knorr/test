# GoGreen GDV Dokumentation

* [Einführung](#einführung)

* [Konzept](#konzept)

* [Datenquellen](#datenquellen)

* [Datenauswertung und -aufbereitung](#datenauswertung und -aufbereitung)


## <a name="einführung"></a> Einführung 
Barcelonas Luftqualität während einer Pandemie

Die Coronapandemie hat Auswirkungen auf verschiedenster Ebenen auf der ganzen Welt. Zu Beginn der Pandemie war Spanien eines der betroffensten Ländern. Um das Verbreiten des Virus einzudämmen, wählte Spanien im zweiten Quartal des Jahres 2020 den Weg des harten Lockdowns. Wie sich der Lockdown und generell das Leben während einer Pandemie auf die Luftqualität der Stadt Barcelona auswirkt, wird in diesem Projekt näher betrachtet.

## <a name="konzept"></a> Konzept 

Im Rahmen der Vorlesung Grundlagen der Datenvisualisierung des Wintersemesters 2020/2021 ist dieses Projekt entstanden. Als vierköpfiges Team sollten wir urbane Daten einer Stadt mit mehr als 250.000 Einwohnern aus dem EU Raum auswählen, aufbereiten, analysieren und abschließend mit einer interaktiven Visualisierung angemessen darstellen. Relativ schnell nach Start des Projekts entstand innerhalb des Teams der Wunsch, Luftqualitätsdaten einer großen Stadt zu untersuchen. Die Luftqualität als zentrales Merkmal des Projekts auszuwählen war in unserem Interesse, da unter anderem ein Teammitglied aus Stuttgart... Aufgrund eines umfangreichen Datenangebots des städtischen Open Data Portals, wurde die Stadt Barcelona ausgewählt. Als Untersuchungsmerkmal wurde zunächst die Verkehrsinfrafstruktur Barcelonas gewählt. Nach einer ausführlichen Datenauswertung entschieden wir uns allerdings dazu, die Luftqualitätsdaten im Zusammenhang mit der Coronapandemie zu betrachten.
Unser Ziel war es letztendlich folgende Fragen zu beantworten:

* Punkt 1

* Punkt 2

* Punkt 3

Unser Dashboard wurde dabei mit plotly/dash umgesetzt.

## <a name="datenquellen"></a> Datenquellen 
Als zentrale Datenquelle der Luftqualitätsdaten Barcelonas, wurde das [Open Data Portal](https://opendata-ajuntament.barcelona.cat/data/en/dataset) der Stadt Barcelona gewählt. Gemessene Daten zur Luftqualität werden seit dem Jahr 2018 von sieben Messstationen auf diesem Portal zur Verfügung gestellt. Es werden Daten zu CO, NO, NO2, O3, PM10 und SO2 erhoben, wobei nicht alle Messstationen alle Schadstoffe messen. Aufgrund einer geänderten Datenstrukturierung seit April 2019, wurden ab diesem Zeitpunkt die Luftqualitätsdaten im Projekt verwendet. Ältere Daten konnten aufgrund der erfolgten Änderungen nicht sinnvoll verwendet werden.

Die im Projekt verwendeten Corona Infektions- und Todeszahlen der Stadt Barcelona, entstammen aus...

Die Ereignisse, die im Zeitstrahl der Coronainzidenzien dargestellt werden, wurden aus verschiedenen Nachrichtenportalen entnommen.

## <a name="datenauauswertung und -aufbereitung"></a> Datenauswertung und -aufbereitung 

Inzidenz- und Todeszahlen, sowie die Ereignisdaten im Rahmen der Coronapandemie konnten ohne weitere Bearbeitung verwendet werden.

Die Daten zur Luftqualität mussten zunächst bearbeitet werden, um diese in dem geplanten Umfang einsetzen zu können. Zum einen musste das Format der Messstationskoordinaten umgewandelt werden, um diese problemlos weiterzuverwenden. Die vorhandenen Koordinaten im Format ED50 wurden per Pythonskript in ein übliches Format zu Längen- und Breitengrad transformiert.




