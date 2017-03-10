## 3. Erkennung von Overfitting u. zu Starker Simplifizierung:

Wie kann bei der Anwendung maschineller Lernverfahren Overfitting bzw. ein zu simpler/einschränkender Hypothesenraum erkannt werden? Erklären sie in diesem Zusammenhang die Sinnhaftigkeit der Partitionierung der zur Verfügung stehenden Daten auf Trainings-, Test- und evtl. Validierungsdaten. Woran würrden sie folgende Sachverhalte erkennen?

1. Overfitting tritt auf.
    * __**Trainingsdaten extrem genau. Test und Validierungsdaten eher ungenau. Großes Gefahrenpotential auch wenn Trainings und Testdaten sehr ähnlich sind. Gute Aufteilung nötig.**__

2. Der Hypothesenraum enthält eine geeignete Modellierung der Aufgabenstellung möglicherweise nicht.
    * __**Modell unzureichend genau bei der Anpassung im Training.**__

3. Die zur Verfügung stehenden Daten ermöglichen es nicht, den gewünschten Zusammenhang zu erlernen.
    * __**Häufig ist ein tiefers Wissen in der aktuellen Domäne notwendig. Ansonsten werden Entscheidung oft nicht deterministisch getroffen sondern beruhen auf irrelevanten Daten und sind daher für das Ergbniss irrelevant.**__

> Partitionierung der Daten: <br/>
> Modell passt sich an Trainingsdaten an, Overfitting ist dabei zB sehr schwer zu erkennen. <br/>
> Darum: Aufteilen in Trainings + Testdaten + ggf. Validierungsdaten <br/>
> - Trainingsdaten: Werden zum Training des Modells verwendet
> - Testdaten: Dienen zum Test des Modells; bei starken Abweichungen des Ergebnisses muss das Modell ge�ndert werden
> - Validierungsdaten: Abschlie�endes Validieren mit zuvor noch "nie" verwendeten Daten, quasi Blindtest -> werde nicht zum Training oder Testen verwendet.

