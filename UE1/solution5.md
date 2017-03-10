## 5. Cross-Validation:
Bei der Verwendung einer n-Fold Cross-Validation werden die verfügbaren Beispiele in n Partitionen unterteilt. Danach wird immer eine andere der n Partitionen als Testmenge ausgewählt und mit den verbleibenden n−1 Partitionen wird unter Verwendung eines bestimmten Lernverfahrens ein Modell gelernt. Dieser Vorgang wird wiederholt, bis alle Partitionen einmal als Testmenge verwendet wurden.

Warum ist ein solches Vorgehen beim maschinellen Lernen sinnvoll? Welche Aussagen können aufgrund des Ergebnisses der Cross-Validation gemacht werden? Dient die Cross-Validation zur Bewertung eines Modells oder eines Verfahrens?

Sinnvoll dann, wenn nicht sehr viele Daten verfügbar sind -> Aufteilung würde die Datenmenge noch mehr reduzieren. Außerdem ist es nicht immer einfach, repräsentativ auf Test- und Trainingsdaten aufzuteilen, da theoretisch zufällig unpassend verteilte Daten gewählt werden könnten.

Beurteilung des Modells (Training + Test)