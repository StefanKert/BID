## 3. Erkennung von Overfitting u. zu Starker Simplifizierung:

Wie kann bei der Anwendung maschineller Lernverfahren Overfitting bzw. ein zu simpler/einschränkender Hypothesenraum erkannt werden? Erklären sie in diesem Zusammenhang die Sinnhaftigkeit der Partitionierung der zur Verfügung stehenden Daten auf Trainings-, Test- und evtl. Validierungsdaten. Woran würrden sie folgende Sachverhalte erkennen?

1. Overfitting tritt auf.
    * Trainingsdaten extrem genau. Test und Validierungsdaten eher ungenau. Großes Gefahrenpotential auch wenn Trainings und Testdaten sehr ähnlich sind. Gute Aufteilung nötig.

2. Der Hypothesenraum enthält eine geeignete Modellierung der Aufgabenstellung möglicherweise nicht.
    * Modell unzureichend genau bei der Anpassung im Training.

3. Die zur Verfügung stehenden Daten ermöglichen es nicht, den gewünschten Zusammenhang zu erlernen.
    * Häufig ist ein tiefers Wissen in der aktuellen Domäne notwendig. Ansonsten werden Entscheidung oft nicht deterministisch getroffen sondern beruhen auf irrelevanten Daten und sind daher für das Ergbniss irrelevant.

> Partitionierung der Daten: <br/>
> Wenn sich das Modell an die Trainingsdaten anpasst ist Overfitting sehr schwer zu erkennen. <br/>
> Lösung: Aufteilen in Trainings + Testdaten + ggf. Validierungsdaten <br/>
> - Trainingsdaten: Training des Modells
> - Testdaten: Testen des Modells; bei starken Abweichungen des Ergebnisses muss das Modell geändert werden
> - Validierungsdaten: Validieren mit zuvor NOCH NIE verwendeten Daten. Daten dürfen nicht zum Training oder Testen verwendet.

