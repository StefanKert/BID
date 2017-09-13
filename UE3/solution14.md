# 14. Pruning:
Beschreiben Sie mit eigenen Worten wozu Pruning beim Lernen von Entscheidungsbäumen dient. Worin besteht der Unterschied zwischen Pre- und Post-Pruning? Welches der beiden PruningVerfahren würden Sie bei der Implementierung eines Entscheidungsbaumlerners in der Praxis einsetzen und warum?

- Pruning soll Overfitting verhindern (zu genauer Anpassen an Trainingsdaten, sodass Rauschen zu stark berücksichtigt wird)
- Pre-Pruning: Knoten werden nicht weiter aufgeteilt, wenn keine Korrelation zwischen Klassen und Attributen besteht (z.B. übar Gain messbar)
- Post-Pruning: Konstruktion eines möglichst optimalen Baumes, der möglicherweise schon overfitted; dann "Abschneiden" von irrelevanten Ästen, die keinen Einfluss haben
- Empfehlenswert: Post-Pruning - dauert zwar beim Lernen des Modells länger, aber die Ergebnisse sind besser (Beim Pre-P. können unabsichtlich eigentlich sinnvolle Zweige wegfallen (Horizont-Effekt))