# PlanLOS! Machbarkeitsstudie

## Architektur 

Im Folgenden Abbild 1 ist das Sequenzdiagram für die Architektur des LSTM-Netzwerk zu sehen.

![Sequencediagram](finished_activity_diagram.drawio.png "Sequence diagram")

Diese besteht aus drei unterschiedlichen Pipelines zum Data-Handling. Die Daten der öffentlichen Verkehrsunternehmen werden im GTFS-Format an PlanLOS! weitergeben. Dieses Format besteht aus 6 bis 15 CSV Dateien mit .txt Endungen, die in einem zip-Archiv zusammengefasst werden. 

Die internen Datensätze der Verkehrsbetreiber so wie des Verkehrsaufkommen befinden sich in einem ähnlichen JSON-Format. Nur die entsprechende Keys und Werte variieren.

Innerhalb der Pipeline für den Data-Handler wird, neben dem Preprocessing der Datensätze für die Vorhersage, auch eine Analyse der internen und traffic Daten durchgeführt. Diese werden an den Visualisierungsstate übergeben und eine detaillierte Auswertung des bestehenden und des geplanten Verkehrsplan dem Unternehmen zu ermöglichen. 

Exemplarisch ist im Folgenden das JSON-Format für die Metadaten dargestellt.

![Metadata im JSON-Format](JSON_metadata.png "Metadata im JSON-Format")

## Output


