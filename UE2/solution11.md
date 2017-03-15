## 11. Entropie und Informationsgewinn:
Gegeben seien folgende Trainingsbeispiele eines Lernproblems mit zwei Klassen:

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
.tg .tg-baqh{text-align:center;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-baqh">a1</th>
    <th class="tg-baqh">a2</th>
    <th class="tg-baqh">Zielkonzept</th>
  </tr>
  <tr>
    <td class="tg-baqh">gut</td>
    <td class="tg-baqh">klein</td>
    <td class="tg-baqh">+</td>
  </tr>
  <tr>
    <td class="tg-baqh">gut</td>
    <td class="tg-baqh">klein</td>
    <td class="tg-baqh">+</td>
  </tr>
  <tr>
    <td class="tg-baqh">gut</td>
    <td class="tg-baqh">groß</td>
    <td class="tg-baqh">-</td>
  </tr>
  <tr>
    <td class="tg-baqh">schlecht</td>
    <td class="tg-baqh">groß</td>
    <td class="tg-baqh">+</td>
  </tr>
  <tr>
    <td class="tg-baqh">schlecht</td>
    <td class="tg-baqh">klein</td>
    <td class="tg-baqh">-</td>
  </tr>
  <tr>
    <td class="tg-baqh">schlecht</td>
    <td class="tg-baqh">klein</td>
    <td class="tg-baqh">-</td>
  </tr>
</table>

1. Berechnen Sie die Entropie für die gegenenen Trainingsdaten im Hinblick auf das Zielkonzept.

    Entropy (C) = - 3/6 * ld (3/6)  - 3/6 * ld (3/6) 
                = -0,5 * -1         - 0,5 * -1
                = 1

2. Berechnen Sie den Informationsgewinn der beiden Attribute a1 und a2.
    - Entropy(Gesamt) = 1  
    - Entropy(a1 gut) = 0,9183
    - Entropy(a1 schlecht) = 0,9183
    - Entropy(a2 klein) = 1
    - Entropy(a2 groß) = 1

    - Gain(a1) = 0,0817042
    - Gain(a2) = 0

3. Beschreiben Sie mit eigenen Worten, was die beiden Maßzahlen Entropie und Informationsgewinn eigentlich aussagen bzw. messen, und erkl¨aren Sie, warum sie beim Lernen von Entscheidungsbäumen von großer Bedeutung sind.

- Entropie
    - Mit der Entropie wird die Reihnheit bzw. Unreinheit einer beliebigen Menge von Beispielen berechnet. Die Entropie bestimmt den mittleren Informationsgehalt eines Attributes.
- Informationsgewinn
    - Der Informationsgewinn ist die erwatete Verringerung der Entropie, wenn eine Eigenschaft an einem bestimmten Knoten abgefragt wird.