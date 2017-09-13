# 13. Zusammenhang zwischen ID3 und Candidate Elimination:
Würde man auf eine Lernaufgabe sowohl den ID3- als auch den Candidate-Elimination-Algorithmus anwenden, wie wäre der gelernte Entscheidungsbaum im Bezug auf die beiden Grenzmengen S und G des Candidate-Elimination-Algorithmus einzuordnen? Lässt sich diesbezüglich eine allgemeine Aussage treffen? Begründen Sie Ihre Antwort.


Candidate Elimination – Ergebnis Hypothesenraum "Workspace"
• Das heißt aber nicht, dass der Entscheidungsbaum, den der ID-3 Algorithmus liefert, der einzig mögliche ist. Gibt es mehrere Möglichkeiten, kommt dies beim Candidate Elimination Algorithmus heraus, wenn hier S und G vereinigt mehrere Hypothesen liefern.
• Die Menge S enthält am Ende den Wert aller Attribute, die im Entscheidungsbaum höchstens abgefragt werden müssen, um zu einer Entscheidung zu kommen. Beispiel: Im Bsp. 12 werden konkrete Werte für Wetter, Temperatur und Wind angegeben. Das heißt, im Entscheidungsbaum könnte man durch eine Kombination der Abfragen von Wetter, Temperatur und Wind eine Entscheidung erreichen.
• Die Menge G enthält am Ende des Candidate Elimination Algorithmus die Werte der Attribute, die im Entscheidungsbaum mindestens abgefragt werden müssen, um zu einer Entscheidung zu kommen. Beispiel: Im Bsp. 12 werden konkrete Werte für Wetter/Temperatur und Wind angegeben. Das heißt, im Entscheidungsbaum könnte man durch eine Kombination von Wetter bzw. Temperatur und Wind eine Entscheidung erreichen.