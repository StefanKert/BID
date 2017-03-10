## 7. Find-S Algorithmus:
Führen Sie für die im vorigen Beispiel skizzierte Lernaufgabe den Find-S Algorithmus mit den gegebenen Trainingsbeispielen durch. Geben Sie außerdem den Pfad im Verband an, der die Entwicklung der Hypothese bei der Ausführung des Algorithmus beschreibt. Findet der Find-S Algorithmus immer eine generellste oder eine spezifischste Hypothese, die mit den Trainingsdaten konsistent ist, falls eine solche existiert? Begründen Sie Ihre Antwort.

<table>
<tr><td>h</td><td>x</td></tr>
<tr><td>[0 1 0]</td><td>[0 1 0]</td></tr>
<tr><td>[0 1 0]</td><td>[1 0 0] (Skip)</td></tr>
<tr><td>[? 1 0]</td><td>[1 1 0]</td></tr>
<tr><td>[? 1 0]</td><td>[1 0 1] (Skip)</td></tr>
</table>

h = [? 1 0]

Findet immer die spezifischte Lösung die für alle positiven Lösungen gilt. Die generellste Lösung wäre [? 1 ?] gefunden wurde aber die spezifischere Lösung [? 1 0].