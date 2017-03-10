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
