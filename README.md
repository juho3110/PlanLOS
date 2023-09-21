# PlanLOS! Machbarkeitsstudie

## Sequenzdiagram

Im Folgenden Abbild 1 ist das Sequenzdiagram für die Infrastruktur des LSTM-Netzwerk zu sehen.

![Sequencediagram](finished_activity_diagram.drawio.png "Sequence diagram")

Diese besteht aus drei unterschiedlichen Pipelines zum Data-Handling. Die erfassten Daten (Metadaten, Traffic und Intern) werden jeweils im JSON-Format erfasst und weiter verarbeitet.

Exemplarisch ist im Folgenden das JSON-Format für die Metadaten dargestellt.

```json {
    "PlanLOS!": {
        "title": "Metadata",
		"Metadata": {
			"Timestamp": {
				"timestamp": "08:57:37"
			}
            		"School": {
				"vacation": "1"
			}
			"Weather": {
				"propability_of_rain": "40",
				"temperature": "14",
				"extreme_weather_forecast": "0"
			}
			"Event": {
				"Long": "8.031088829040527",
				"Lat": "52.28971862792969",
				"timestamp_0": "09:00",
				"timestamp_1": "21:00"
			}
		}
	}
}
```


Die internen Datensätze der Verkehrsbetreiber so wie des Verkehrsaufkommen befinden sich in einem ähnlichen JSON-Format. Nur die entsprechende Keys und Werte variieren.
