# Übungsaufgaben (begleitend zur Lehrveranstaltung)

## 1. Overfitting vs. zu starke Simplifizierung:
Worin besteht das Problem bei "Overfitting"? Worin bei "zu starker Simplifizierung"? Erklären Sie beide Begriffe anhand eines selbst gewählten Beispiels.

* Overfitting: 
    * __**Für die Erkennung von Farben werden beim Trainieren von Farben nur Farben mit einem sehr hohen Rotanteil verwendet. Dadurch werden rote Farben immer richtig erkannt, andere jedoch nicht**__


* Zu starke Simplifizierung:
    * __**Bei der Erkennung von Augen wurde soweit Simplifiziert, dass auch Türknöpfe als Augen erkannt werden.**__

## 2. Größe von Hypothesenräumen:
Betrachten Sie eine binäre Lernaufgabe (d.h. es gibt nur zwei verschiedene Zielklassen 0 oder 1), bei der jedes Beispiel durch n Attribute a1 . . . an charakterisiert wird, wobei jedes Attribut k unterschiedliche Werte annehmen kann.

1. Wieviele unterschiedliche Beispiele kann es bei dieser Lernaufgabe geben? Wieviele unterschiedliche Konzepte sind bei dieser Lernaufgabe möglich? Unter einem Konzept versteht man die Abbildung aller Beispiele auf die möglichen Klassen (d.h. das Konzept ist die zu lernende Realität).
    * __**Beispiele: n^k**__
    * __**Konzepte: n^k * [Anzahl der Lösungsklassen(2)]**__

2. Wieviele unterschiedliche Hypothesen sind möglich, wenn als Hypothesenbeschreibungssprache nur die additive Verknüpfung einfacher "Attribut = Wert" Paare zugelassen ist, wie z.B.:

> 0 ⇔ a1 = blau ∧ a7 = klein <br/>
> 1 ⇔ a3 = hoch ∧ a4 = langsam ∧ a8 = normal

* Lösung
    * __**2*k * n ^ k **__

    

3. Wieviele unterschiedliche Hypothesen sind möglich, wenn als Hypothesenbeschreibungssprache die disjunktive Normalform (DNF) zugelassen ist (d.h. die disjunktive Verknüpfung beliebig vieler und beliebig langer Konjunktionen), wie z.B.:

>0 ⇔ a1 = blau ∨ (a2 = sehr gering ∧ a7 = klein)
>1 ⇔ (a3 = hoch ∧ a4 = langsam) ∨ (a8 = normal ∧ a5 = glatt)

* Lösung
    * __**?????**__

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


## 4. Arten von Lernaufgaben
Erklären sie in eigenen Worten die Charaktaristika und Unterscheidungsmerkmale von:

1. Klassifikationsaufgaben.
    * Als Ergebnis sollten Datensätze bestimmten Klassen zugeordnet werden. Bspw. Mensch oder Kein Mensch. 
2. Regressionsaufgaben.
    * Es sollte ein passender Zahlenwert zu einem Eingabeparemeter gefunden werden. Anhand einer Funktion wird von einem Eingangswert x ein Ausgangswert y gefunden. Beispiel: Preisschätzung von Gründstücken. 
3. Zeitreihenanalyse.
    * Zeitabhängige Datensätze werden zur Lösung herangezogen, wie z.B. das Wetter.

Benennen sie jeweils ein oder mehrere typische Anwendungsfälle. Die eben genannten Fälle gehören alle zur Klasse der überwachten Lernaufgaben. Erklären sie in diesem Zusammenhang den Unterschied zwischen überwachten und unüberwachten Lernen.

1. Überwachtes Lernen
    * In der Trainingsphase werden Eingaben mit korrekten Lösungen vorgegeben, an die sich das System "anpasst".
Dadurch werden die Zusammenhänge zwischen Ein- und Ausgabe erlernt
2. Unüberwachtes Lernen
    * Keine Vorgaben bzgl. zu erwartender Ausgabe. System muss selbst Strukturen und Muster erkennen.

## 5. Cross-Validation:
Bei der Verwendung einer n-Fold Cross-Validation werden die verfügbaren Beispiele in n Partitionen unterteilt. Danach wird immer eine andere der n Partitionen als Testmenge ausgewählt und mit den verbleibenden n−1 Partitionen wird unter Verwendung eines bestimmten Lernverfahrens ein Modell gelernt. Dieser Vorgang wird wiederholt, bis alle Partitionen einmal als Testmenge verwendet wurden.

Warum ist ein solches Vorgehen beim maschinellen Lernen sinnvoll? Welche Aussagen können aufgrund des Ergebnisses der Cross-Validation gemacht werden? Dient die Cross-Validation zur Bewertung eines Modells oder eines Verfahrens?

__**Sinnvoll dann, wenn nicht sehr viele Daten verfügbar sind -> Aufteilung würde die Datenmenge noch mehr reduzieren. Außerdem ist es nicht immer einfach, repräsentativ auf Test- und Trainingsdaten aufzuteilen, da theoretisch zufällig unpassend verteilte Daten gewählt werden könnten.**__

__**Beurteilung des Modells (Training + Test)**__

## 6. Genereller-Als-Relation, Verband von Hypothesen und Konsistenz:
Gegeben seien folgende Trainingsbeispiele eines binären Lernproblems, bei dem jedes Beispiel durch 3 boolsche Attribute a1, a2 und a3 angegeben wird. Eine Hypothese wird ebenfalls als Tripel dargestellt, wobei zusätzlich das Zeichen ’?’ bei einem Attribut für einen beliebigen Wert steht.

<table>
<tr><td>a1</td><td>a2</td><td>a3</td><td></td><td>Zielkonzept</td></tr>
<tr><td>0</td><td>1</td><td>0</td><td></td><td>1</td></tr>
<tr><td>1</td><td>0</td><td>0</td><td></td><td>0</td></tr>
<tr><td>1</td><td>1</td><td>0</td><td></td><td>1</td></tr>
<tr><td>1</td><td>0</td><td>1</td><td></td><td>0</td></tr>
</table>

1. Stellen Sie den Verband aller Hypothesen, der durch die Genereller-Als-Relation gebildet wird, graphisch dar.

2. Welche der folgenden Hypothesen sind mit den Trainingsdaten konsistent?

<table>
<tr><td>[? ? ?]</td><td>[ ]</td></tr>
<tr><td>[0 1 0]</td><td>[1 1 1]</td></tr>
<tr><td>[? 1 0]</td><td>[1 ? 0]</td></tr>
<tr><td>[? ? 0]</td><td>[? 1 ?]</td></tr>
</table>

* Lösung: 

<table>
<tr><td>[? ? ?]</td></tr>
<tr><td>[? 1 0]</td></tr>
<tr><td>[? ? 0]</td></tr>
<tr><td>[? 1 ?]</td></tr>
</table>

## 7. Find-S Algorithmus:
Führen Sie für die im vorigen Beispiel skizzierte Lernaufgabe den Find-S Algorithmus mit den gegebenen Trainingsbeispielen durch. Geben Sie außerdem den Pfad im Verband an, der die Entwicklung der Hypothese bei der Ausführung des Algorithmus beschreibt. Findet der Find-S Algorithmus immer eine generellste oder eine spezifischste Hypothese, die mit den Trainingsdaten konsistent ist, falls eine solche existiert? Begründen Sie Ihre Antwort.


<table>
<tr><td>h</td><td>x</td></tr>
<tr><td>[1 1 1]</td><td>[0 1 0]</td></tr>
<tr><td>[? ? ?]</td><td>[0 1 0]</td></tr>
<tr><td>[? 1 ?]</td><td>[0 1 0]</td></tr>
<tr><td>[? 1 ?]</td><td>[1 1 0]</td></tr>
</table>

h = [? 1 ?]


__**Findet nicht immer spezifischsten Kandidaten -> hängt von der Ausgangssituation ab: Wenn die spezifischste Hypthesen keine Übereinstimmung bei immer gleichen Elementen hat (so wie hier bei [1 1 1]), werden eine zu generelle Hypothese gefunden (wäre bei [0 1 0] nicht passiert) **__

## 8. Candidate Elimination:
Betrachten Sie die Lernaufgabe sowie die Trainingsbeispiele aus Aufgabe 6.
1. Führen Sie mit den gegebenen Trainingsbeispielen den Candidate-Elimination-Algorithmus durch. Geben Sie dabei bei jedem Schritt des Algorithmus die entsprechende S und G Menge an. Zusätzlich geben Sie am Ende des Algorithmus die Menge aller konsistenten Hypothesen (d.h. den Versionenraum) an.
2. Verwenden Sie die generierte S und G Menge, um die Klasse folgender neuer Beispiele vorherzusagen:
<table>
<tr><td>a1</td><td>a2</td><td>a3</td></tr>
<tr><td>0</td><td>0</td><td>0</td></tr> 
<tr><td>1</td><td>1</td><td>1</td></tr>
<tr><td>0</td><td>0</td><td>1</td></tr>
<tr><td>0</td><td>1</td><td>1</td></tr>
</table>

3. Lernen Sie mit Hilfe des Candidate-Elimination-Algorithmus folgende weitere Trainingsbeispiele
und geben Sie dabei wieder f¨ur jeden Schritt die Entwicklung der S und G Menge an. Was
bedeutet das Ergebnis?
<table>
<tr><td>a1</td><td>a2</td><td>a3</td><td></td><td>Zielkonzept</td></tr>
<tr><td>1</td><td>1</td><td>1</td><td></td><td>1</td></tr>
<tr><td>0</td><td>0</td><td>0</td><td></td><td>1</td></tr>
</table>

## 9. Reihenfolge der Trainingsbeispiele beim Candidate Elimination Algorithmus:
Hat die Reihenfolge der Trainingsbeispiele auf das Ergebnis des Candidate-Elimination-Algorithmus irgendeine Auswirkung? Wie müsste man die Reihenfolge der Trainingsbeispiele möglichst geschickt wählen, um die Größe der S und G Menge während der Ausführung des Candidate-EliminationAlgorithmus möglichst klein zu halten?

- Keine Auswirkung auf das Ergebnis
- Reihenfolge: Idealerweise abwechselnd (wie im Beispiel), sodass in jedem Durchgang entweder Elemente von S oder G entfernt werden können