## 2. Größe von Hypothesenräumen
Betrachten Sie eine binäre Lernaufgabe (d.h. es gibt nur zwei verschiedene Zielklassen 0 oder 1), bei der jedes Beispiel durch n Attribute a1 . . . an charakterisiert wird, wobei jedes Attribut k unterschiedliche Werte annehmen kann.

1. Wieviele unterschiedliche Beispiele kann es bei dieser Lernaufgabe geben? Wieviele unterschiedliche Konzepte sind bei dieser Lernaufgabe möglich? Unter einem Konzept versteht man die Abbildung aller Beispiele auf die möglichen Klassen (d.h. das Konzept ist die zu lernende Realität).
    * Beispiele: k^n
    * Konzepte: k^n * [Anzahl der Lösungsklassen(2)]

2. Wieviele unterschiedliche Hypothesen sind möglich, wenn als Hypothesenbeschreibungssprache nur die additive Verknüpfung einfacher "Attribut = Wert" Paare zugelassen ist, wie z.B.:

> 0 ⇔ a1 = blau ∧ a7 = klein <br/>
> 1 ⇔ a3 = hoch ∧ a4 = langsam ∧ a8 = normal

* Lösung
    * k^n + n^k * k

3. Wieviele unterschiedliche Hypothesen sind möglich, wenn als Hypothesenbeschreibungssprache die disjunktive Normalform (DNF) zugelassen ist (d.h. die disjunktive Verknüpfung beliebig vieler und beliebig langer Konjunktionen), wie z.B.:

> 0 ⇔ a1 = blau ∨ (a2 = sehr gering ∧ a7 = klein)
> 1 ⇔ (a3 = hoch ∧ a4 = langsam) ∨ (a8 = normal ∧ a5 = glatt)

* Lösung
    * k^n + n^4 * k
