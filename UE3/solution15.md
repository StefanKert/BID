# 15. "Lazy Learning" vs. "Eager Learning":
Fallbasiertes Lernen wird auch oft als "Lazy Learning" bezeichnet, da das eigentliche Lernen nicht während der Trainingsphase sondern erst bei der Verarbeitung neuer unbekannter Beispiele erfolgt. Im Gegensatz dazu wird beim "Eager Learning" (z.B. Candidate-Elimination-Algorithmus, ID3-Algorithmus) bereits während der Trainingsphase ein Modell aus den Trainingsbeispielen generiert, wodurch die Klassifikation neuer Beispiele danach sehr schnell und unaufwändig erfolgen kann.
Stellen Sie die Vor- und Nachteile dieser beiden Lernstrategien gegenüber. Geben Sie weiters zwei Szenarien aus der Praxis an, bei denen sich jeweils die eine oder die andere Strategie besser eignet.


Lazy Learning:
+ Trainingsphase schnell/nicht vorhanden
+ Sehr einfach (auch prinzipiell - einfach vorhandene Fälle mit aktuellen vergleichen)
+ Keine Trainingsdaten nötig -> keine Annahmen, sondern nur Tatsachen gehen in die Fallbasis ein
- Geschwindigkeit zur Laufzeit gering
- alle Attribute werden berücksichtigt -> anfällig
- Overfitting (zu Beginn) kritisch
- Mehr Attribute verschlechtern Verhalten viel massiver

Eager Learning:
- Längere Trainingsphasen (vernachlässigbar)
- Verfahren sind komplizierter
+ Höhere Geschwindigkeit zur Laufzeit, da Modell bereits bekannt
+ Irrelevante Attribute werden aussortiert
+ Overfitting bei guter Modellierung besser beherrschbar
