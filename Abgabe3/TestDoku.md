\# Kurzdokumentation der JUnit-Tests für GameState



Der Test setUp() baut vor jedem Test ein festes 3x3-Spielfeld mit einer Wand unten links, einem Pin-Slot unten rechts und der Schlange in der Mitte auf, damit alle Tests reproduzierbar sind.



1\. Der Test testInitialStateIsRunning überprüft, ob das Spiel im Zustand RUNNING startet und die Schlange ohne Richtungseingabe stehen bleibt.

Das stellt sicher, dass das Spiel beim Start nicht direkt losrennt oder abstürzt, sondern auf die erste Aktion des Spielers wartet.



2\. Der Test testMoveIntoEmptySpace überprüft, ob die normale Bewegung in ein freies Feld funktioniert und die Schlange dabei wie vorgeschrieben wächst.

Das validiert die absolute Kernmechanik von Snake.



3\. Der Test testMoveIntoWallIsBlocked überprüft, ob die Wand-Blockade funktioniert, also dass die Schlange stehen bleibt und ihre Blickrichtung verliert, während das Spiel weiter läuft).

Das zeigt, dass Hindernisse korrekt erkannt werden und der Spieler nicht durch Wände "glitchen" kann. Gleichzeitig wird geprüft, dass eine Wand nicht zum Game Over führt.



4\. Der Test testMoveOutOfBoundsLosesGame überprüft, ob das Verlassen des Spielfeldrandes funktioniert und sofort zum Game Over (Status LOST\_OUT\_OF\_BOUNDS) führt.

Das verhindert, dass die Schlange das Level-Array verlässt, was sonst zu einer unschönen `ArrayIndexOutOfBoundsException` und einem Programmabsturz führen würde.



5\. Der Test testMoveIntoPinWrongDirectionIsBlocked überprüft, ob die Blockade bei falscher Anstoßrichtung an einen Pin funktioniert Pin soll bei LOW bleiben und die Schlange stoppt.

Das ist der Kern des Lockpicking-Rätsels. Wenn die Schlange Pins aus jeder Richtung aktivieren könnte, wäre die Positionsfindung völlig überflüssig.



6\. Der Test testMoveIntoHighPinIsBlocked überprüft, ob die Blockade bei einem bereits aktivierten Pin funktioniert.

Das fügt dem Spiel die nötige Komplexität hinzu. Bereits gelöste Pins werden zu Hindernissen, um die der Spieler herum navigieren muss. 



7\. Der Test testActivatePinChangesState überprüft, ob das Aktivieren eines Pins funktioniert -> Pin wird auf HIGH gesetzt und Schlange betritt das Feld nicht.

Stellt sicher, dass der Spieler tatsächlich mit den Pins interagieren kann. Es prüft auch explizit die Sonderregel, dass das Pin-Feld dabei nicht betreten wird.



8\. Der Test testActivateLastPinWinsGame überprüft, ob die Siegbedingung funktioniert. also dass das Spiel auf WON wechselt, sobald der letzte Pin im Level auf HIGH springt.

Dieser Test beweist, dass das System merkt, wann der Spieler seine Aufgabe erfolgreich abgeschlossen hat.



9\. Der Test testSelfCollisionLosesGame überprüft, ob die Selbstkollision funktioniert also das es dabei direkt zum GAME OVER kommt.

Das sichert die klassische und wichtigste Snake-Todesbedingung ab.



10\. Der Test testNoMovementWhenGameIsOver überprüft, ob der Early-Exit funktioniert, also das man sich nicht mehr bewegen kann, sobald das Spiel gewonnen oder verloren wurde.



