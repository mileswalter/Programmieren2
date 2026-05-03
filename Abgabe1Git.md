**Git Status erklären**



Die Ausgabe sagt uns, dass wir aktuell im Branch namens b03 arbeiten, die Dateien *CONTRIBUTING.md* und *homework/b03.md* wurden bearbeitet sind aber noch nicht in der Staging Area, heißt sie sind noch nicht für den nächsten Commit vorgemerkt und müssen erstmal mit "*git add <file>…*" in die Staging area gebracht werden. Die Ausgabe sagt uns außerddem, dass wir mit *git restore* "*<file>…*" bestimmte Dateien wieder auf den Stand von b03 setzen können.



Außerdem werden wir darauf hingewiesen dass es eine Datei (*foo.java*) gibt, die noch komplett neu ist und nicht von Git mit verfolgt wird. Diese können wir wieder mit "*git add <file>…*" indie Staging area bringen.



Die letzte Zeile sagt, dass keine Änderungen zum committen vorhanden sind und wir vorher die Sachen mit "*git add*" zur Staging area hinzufügen können.



""

Um nur die Änderungen an *foo.java* zu committen wird in unserem Fall folgende Befehlssequenz benötigt:

*git add foo.java*

*git commit -m <Commit Nachricht>*









**Git Spiel**



Erstmal "*git log --oneline*" um die ID´s der Tage etc zu bekommen



1.1

Vorgehen: *git show 4aa8014*

Antwort: An Tag 1 ging Markus mit seinem Schwert in der Hand und mit leichter Rüstung bekleidet in den Dungeon und stieß auf erste Monster



1.2

Vorgehen: *git show <ID vom Tag>:stats.md* von Tag 1 hoch bis er halt 4xp hat

Antwort: Der Held an Tag 01.3 zum ersten mal 4xp



1.3 Wann hat der Held zum ersten Mal 10 hunger Punkte?

Vorgehen: selbes Vorgehen wie bei 1.2

Antwort: An Tag 01.4



1.4 

Vorgehen: *git log -p Rucksack.md* und dann die Änderungen anschauen

Antwort: Im Verlauf der Tage hatte der Held insgesamt 2 Heiltränke im Rucksack



1.5

Vorgehen: Selbe Vorgehensweise wie bei 1.4 nur schaue ich jetzt wann Gold weggegangen ist und was neu dazu gekommen ist

Antwort: 1 Brot für 5 Gold, 1 Heiltrank für 5 Gold



1.6

Vorgehen: *git diff 2ffebcf 39568d5*

Antwort: "Erfrischt und gestärkt machte sich Markus auf den Weg, um die letzte Etappe seiner Quest zu erfüllen." wurde hinzugefügt



1.7

Vorgehen: *git log -p Rucksack.md* und dann Schauen wann Essen im Inv weniger wurde und die ID dann mit den ganz am Anfang abgleichen um den Tag herauszufinden

Antwort: 1 Brot an Tag 3.14





2\.

Ich schaue das ich auf dem master Branch bin und gehe dann in die *stats.md* und Passe die xp auf 42 an und speicher die Datei. Dann öffne ich den Bash und gebe ein "*git add stats.md*" und dann "*git commit --amend --no-edit*" Damit packe ich die Änderung direkt an den letzen Commit und erstelle keinen neuen



3\. 

Die Geschichte wurde in *questlog.md* weitergeführt und dann mit *git* "*add questlog.md*" und "git commit -m "tag 04.6" committet



4\. Die Geschichte wurde in *questlog.*md weitergeführt. Es wurde schaden genommen und ein Heiltrank genutzt, weshalb in stats.md und Rucksack.md Änderungen vorgenommen wurden.dann mit "*git* *add questlog.md stats.md rucksack.md*" und "*git commit -m "tag 04.7*" committet



5\.

Neue Datei *gear.md* wurde erstellt und dann die Ausrüstung einfach von *stats.md* rüberkopiert. Am ende mit "*git* *add gear.md stats.md*" und "*git commit -m "tag 04.8*" committet









**Commit-Meldungen**



Der erste Commit ist zeimlich schlecht benannt meiner Meinung nach, da allein die Überschrift "Layer System 5" keine aussage kraft hat. Die Erklärung darunter ist auch sehr wage.

Das gefällt mir am zweiten Commit besser, dort sieht man direkt in der Überschrift es handelt sich um eine Änderung im Spiel und genauer gesagt um ein Besseres Item und Crafting System. Die Beschreibung darunter sind auch deutlich aussage kräftiger und wirken wie ein echter Changelog mit Änderungen.







