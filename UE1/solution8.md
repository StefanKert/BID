## 8. Candidate Elimination:
Betrachten Sie die Lernaufgabe sowie die Trainingsbeispiele aus Aufgabe 6.
1. Führen Sie mit den gegebenen Trainingsbeispielen den Candidate-Elimination-Algorithmus durch. Geben Sie dabei bei jedem Schritt des Algorithmus die entsprechende S und G Menge an. Zusätzlich geben Sie am Ende des Algorithmus die Menge aller konsistenten Hypothesen (d.h. den Versionenraum) an.

G = {[???]}
S = {[010], [111]}


<table>
<tr><td></td><td>X</td><td></td><td>S</td><td>G</td></tr>
<tr><td>1.</td><td>[010]</td><td>+</td><td>{[010], [111]}</td><td>{[???]}</td></tr>
<tr><td>2.</td><td>[010]</td><td>+</td><td>{[010], [?1?]}</td><td>{[???]}</td></tr>
<tr><td>3.</td><td>[010]</td><td>+</td><td>{[010]}</td><td>{[???]}</td></tr>
<tr><td>4.</td><td>[100]</td><td>-</td><td>{[010]}</td><td>{[?1?]}</td></tr>
<tr><td>5.</td><td>[110]</td><td>+</td><td>{[010]}</td><td>{[?1?]}</td></tr>
<tr><td>6.</td><td>[110]</td><td>+</td><td>{[?10]}</td><td>{[?1?]}</td></tr>
<tr><td>7.</td><td>[101]</td><td>-</td><td>{[?10]}</td><td>{[?1?]}</td></tr>
</table>

V = {[?10], [?1?]}

2. Verwenden Sie die generierte S und G Menge, um die Klasse folgender neuer Beispiele vorherzusagen:
<table>
<tr><td>a1</td><td>a2</td><td>a3</td><td></td><td><b>Klasse</b></td></tr>
<tr><td>0</td><td>0</td><td>0</td><td></td><td><b>0</b></td></tr>
<tr><td>1</td><td>1</td><td>1</td><td></td><td><b>1</b></td></tr>
<tr><td>0</td><td>0</td><td>1</td><td></td><td><b>0</b></td></tr>
<tr><td>0</td><td>1</td><td>1</td><td></td><td><b>1</b></td></tr>
</table>

3. Lernen Sie mit Hilfe des Candidate-Elimination-Algorithmus folgende weitere Trainingsbeispiele
und geben Sie dabei wieder für jeden Schritt die Entwicklung der S und G Menge an. Was
bedeutet das Ergebnis?

<table>
<tr><td>a1</td><td>a2</td><td>a3</td><td></td><td>Zielkonzept</td></tr>
<tr><td>1</td><td>1</td><td>1</td><td></td><td>1</td></tr>
<tr><td>0</td><td>0</td><td>0</td><td></td><td>1</td></tr>
</table>

___

<table>
<tr><td></td><td>X</td><td></td><td>S</td><td>G</td></tr>
<tr><td>8.</td><td>[111]</td><td>+</td><td>{[?10]}</td><td>{[?1?]}</td></tr>
<tr><td>9.</td><td>[111]</td><td>+</td><td>{[?1?]}</td><td>{[?1?]}</td></tr>
<tr><td>10.</td><td>[000]</td><td>+</td><td>{}</td><td>{}</td></tr>
</table>

V = { }  

Traningsdaten sind auf Grund des letzten Trainingsbeispiels inkonsitent. Für [0 0 0] sollte auf Grund der bisherigen Trainingsdaten das Konzept 0 herauskommen. Ein mögliches Problem wäre auch, dass dieses Konzept nicht in H enthalten ist und sich daher das bisherige Model falsch trainiert hat.