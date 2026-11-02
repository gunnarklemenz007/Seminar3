# Seminar3

## Chatverlauf mit Copilot

Dieses Protokoll enthält die sichtbaren Nutzerbeiträge und Copilot-Antworten zu den Änderungen am Wetter-Notebook. Systemanweisungen und interne Werkzeugaufrufe sind nicht Teil des Gesprächsprotokolls.

### 1. Modellierung der Wetterdaten

**Nutzer:**

Füge bitte ein Modell (optimaler Algorithmus in Anlehnung an Matlab- Regression- / Klasssification-Learner) ein, Training mit Wetterdaten von 2020 bis 2024, Test Wetterdaten 2025, anschließend Abgleich mit den Realdaten aus 2025 und Auswertung über entsprechende Metriken.

**Copilot:**

Ich prüfe zunächst die vorhandenen Wetterdaten, Notebooks und Modellierungsansätze, damit Training, 2025-Test und Metriken zum Aufbau des Projekts passen.

**Nutzer:**

Füge bitte ein Modell (optimaler Algorithmus in Anlehnung an Matlab- Regression- / Klasssification-Learner) ein, Training mit Wetterdaten von 2020 bis 2024, Test Wetterdaten 2025, anschließend Abgleich mit den Realdaten aus 2025 und Auswertung über entsprechende Metriken.

**Copilot:**

Das Notebook enthält Tageswerte für mehrere Wettergrößen. Ich ergänze einen zeitlich sauberen Modellvergleich mit 2024 als Auswahljahr, trainiere die gewählten Modelle danach auf 2020–2024 und werte 2025 gegen die Messwerte aus.

Im [Wetter-Notebook](dwd_berlin_2025_eda.ipynb) ist jetzt ein Modellvergleich ergänzt: Modelle werden anhand von 2024 ausgewählt, mit Wetterdaten von 2020–2024 neu trainiert und gegen die Messwerte von 2025 getestet. Verglichen werden Regressionen für Temperaturen und Niederschlagsmenge sowie die Klassifikation von Regentagen ab 1 mm. Die Auswertung zeigt MAE, RMSE, R² und Klassifikationsmetriken samt Konfusionsmatrix.

**Testlauf mit den lokalen DWD-Daten:** Die Temperaturprognosen erreichten R²-Werte von 0,877 bis 0,907. Für die Regenmenge war das beste Modell ein Dummy-Baseline-Modell (R² = −0,006); die Regentag-Klassifikation erzielte F1 = 0,400 und ROC-AUC = 0,636. Niederschlag ist in diesen Daten also deutlich schwieriger vorherzusagen als Temperatur.

**Einordnung:** Das ist eine rollierende Ein-Tages-Prognose; sie nutzt jeweils die tatsächlichen Messwerte des Vortags und ist keine Prognose des gesamten Jahres 2025 im Voraus. Die Notebook-Zelle wurde mit den lokalen DWD-Archiven ausgeführt; Notebook-Format und Python-Syntax sind geprüft.

### 2. Vollständige Aufnahme ins Notebook

**Nutzer:**

Bitte alles in das Notebook einfügen/ergänzen!

**Copilot:**

Ich ergänze die Auswertung vollständig im Notebook: neben dem Code auch nachvollziehbare Erläuterungen, die gemessenen 2025-Ergebnisse und Hinweise zur Interpretation. Danach prüfe ich die Notebook-Struktur und den Modelllauf erneut.

Erledigt — die Modellierung und Auswertung sind jetzt vollständig im [Wetter-Notebook](dwd_berlin_2025_eda.ipynb) enthalten: Modellvergleich und Auswahl über 2024, Training auf 2020–2024, unabhängiger Test mit 2025, Metriken, Konfusionsmatrix, Diagramme und automatisch erzeugte Ergebnisinterpretation. Die Hinweise zu Prognosehorizont und fehlenden Sonnenscheindaten sind ebenfalls ergänzt.

Die Modellzelle wurde mit den lokalen DWD-Daten ausgeführt; Notebook-Format und Python-Syntax sind geprüft.

### 3. Visualisierung der Modellmetriken

**Nutzer:**

Kannst du für die Auswertung des Modells noch die Metriken visualisieren?

**Copilot:**

Ich ergänze direkt im Notebook eine kompakte Visualisierung der 2025-Testmetriken: Regressionsergebnisse, Klassifikationsmetriken und die Konfusionsmatrix. Zuerst prüfe ich die vorhandenen Auswertungsausgaben, damit die Grafiken darauf aufbauen.

Ja — im [Wetter-Notebook](dwd_berlin_2025_eda.ipynb) werden die Metriken jetzt zusätzlich visualisiert:

- **Regression:** MAE, RMSE und R² für den Test 2025
- **Modellvergleich:** MAE der Kandidatenmodelle im Validierungsjahr 2024
- **Klassifikation:** Accuracy, Precision, Recall, F1 und ROC-AUC
- **Regentage:** Konfusionsmatrix

Die Notebook-Zelle wurde mit den DWD-Daten ausgeführt; alle vier Grafiken wurden erfolgreich erzeugt.

### 4. Gesprächsprotokoll in der README

**Nutzer:**

Speichere den gesamten Chat mit dem Copiloten in der readme-Datei!

**Copilot:**

Ich ergänze die README um einen Gesprächsverlauf mit den sichtbaren Nutzeranfragen und Copilot-Antworten. Interne Werkzeugaufrufe und Systemanweisungen gehören nicht zum Chat-Transkript und werden nicht aufgenommen.
