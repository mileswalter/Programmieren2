Tests wie *shouldIncreaseCount\_whenCatIsAdded* und s*houldFindCorrectCat\_whenSearchingByName* stellen sicher, dass die Kernaufgaben des Cafes überhaupt funktionieren. Ohne diese Tests wüssten wir nicht, ob der interne Baum die Daten korrekt speichert.

Außerdem ist *shouldNotCountDuplicateWeights* esonders relevant, da er ein spezifisches Verhalten des Systems dokumentiert: Die Klasse *Node* lässt keine Duplikate zu, und da *FelineOverLord* nach Gewicht vergleicht, kann das Cafe keine Katzen mit dem selben Gewicht haben. Dieser Test macht dieses logisch fragwürdige, aber technisch vorhandene Verhalten transparent.

Wenn Nutzer falsche Eingaben macht soll das Programm nicht abstürzen. Tests für null-Werte oder ungültige Gewichtsbereiche stellen sicher, dass das Programm kontrolliert reagiert und nicht abstürzt.


Die Tests sind unterschiedlich, weil sie nicht nur die korrekte Funktion bestätigen, sondern auch Grenzfälle, logische Fehler, wie z.B. Gewichts-Duplikate und die Stabilität bei falschen Eingaben abdecken. Sie testen somit verschiedene Ausführungspfade der Software.



