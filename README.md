# PlanLOS! Machbarkeitsstudie

## Architektur

Im Folgenden Abbild 1 ist das Sequenzdiagram für die Architektur des LSTM-Netzwerk zu sehen.

![Sequencediagram](finished_activity_diagram.drawio.png "Sequence diagram")

Diese besteht aus drei unterschiedlichen Pipelines zum Data-Handling. Die Daten der öffentlichen Verkehrsunternehmen werden im GTFS-Format an PlanLOS! weitergeben. Dieses Format besteht aus 6 bis 15 CSV Dateien mit .txt Endungen, die in einem zip-Archiv zusammengefasst werden. Um für uns einen einheitlichen Umgang mit den Daten zu gewährleisten werden diese im Preprocessing in ein JSON-Format umgewandelt.

Ebenfalls werden die Meta- und Trafficdaten in der entsprechenden Pipeline in das JSON-Format überführt. Da die keys und values der entsprechenden Daten im JSON-Format variieren werden unterschiedliche Methoden zum Einlesen der Daten in den prediction state bennötigt. Aber da sich die Daten im gleichen Format befinden, wird garantiert, dass über minimale Änderungen der Methoden zum Einlesen ein permanenter Datenstrom in das neuronale Netz gewährleistet wird.   

Innerhalb der Pipeline für den Data-Handler wird, neben dem Preprocessing der Datensätze für die Vorhersage, auch eine Analyse der internen und traffic Daten durchgeführt. Diese werden an den Visualisierungsstate übergeben und eine detaillierte Auswertung des bestehenden und des geplanten Verkehrsplan dem Unternehmen zu ermöglichen. 

Exemplarisch ist im Folgenden das JSON-Format für die Metadaten dargestellt.

![Metadata im JSON-Format](JSON_metadata.png "Metadata im JSON-Format")

## Output


