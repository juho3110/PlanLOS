# PlanLOS! Machbarkeitsstudie

## Sequenzdiagram

Im Folgenden Abbild 1 ist das Sequenzdiagram für die Infrastruktur des LSTM-Netzwerk zu sehen.

![Sequencediagram](finished_activity_diagram.drawio.png "Sequence diagram")

Diese besteht aus drei unterschiedlichen Pipelines zum Data-Handling. Die erfassten Daten (Metadaten, Traffic und Intern) werden jeweils im JSON-Format erfasst und weiter verarbeitet. 

Exemplarisch ist im Folgenden das JSON-Format für die Metadaten dargestellt.

```json {
    "PlanLOS!": {
        "title": "Metadata",
		"GlossDiv": {
            "title": "S",
			"GlossList": {
                "GlossEntry": {
                    "ID": "SGML",
					"SortAs": "SGML",
					"GlossTerm": "Standard Generalized Markup Language",
					"Acronym": "SGML",
					"Abbrev": "ISO 8879:1986",
					"GlossDef": {
                        "para": "A meta-markup language, used to create markup languages such as DocBook.",
						"GlossSeeAlso": ["GML", "XML"]
                    },
					"GlossSee": "markup"
                }
            }
        }
    }
}
