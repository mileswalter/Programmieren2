Aufgabe 1

1.1:

Ich habe *git diff master end --name-only* damit mir die Dateien angezeigt werden die geändert wurden.
Dann binb ich in *hero.md* rein und habe die geändert und anschließend mit *git add* und *git commit* committet.

Am Ende habe ich mit *git merge end* den end Branch in den Master Branch gemerged.



1.2:
Ich habe mit *git diff master end* geschaut wo Änderungen sind und dann woanders was geändert.
Dann habe ich am Anfang bei *questlog.md* eine Zeile hinzugefügt und wieder mit *git add* und *git commit* committet.

Am Ende habe ich mit *git merge end* gemerged wobei ein Conflict aufgetreten ist. diesen habe ich dann behoben indem ich erneut *questlog.md* geöffnet habe, dann habe ich folgende Zeilen entfernt "<<<<<<< HEAD

=======

>>>>>>> end"

und mit *git add questlog.md* und *git commit* den Merge vollendet.



1.3:

Wenn die Änderung anders ist als in *end* dann bekomme ich einen Merge Konflikt.

Wenn die Änderung identisch ist habe ich ebenfalls einen Merge Konflikt erhalten. Ich denke normalerweise sollte dies nicht passieren wie auch in Aufgabe 2 nicht dennoch bekomme ich immer und überall Merge Konflikte angeblich sind irgendwelche Leerzeilen entfernt worden die vorher da waren (da waren aber keine) etc.



1.4:
Ich habe wieder in Rucksack die Tränke auf 2 geändert und dann mit *git checkout end* auf den end Branch gewechselt und

diesen dann mit *git rebase master* auf die Spitze des Masters gesetzt

Mein rebase wurde in 3 schritte aufgeteilt und bei jedem der 3 gab es einen Konflikt in *questlog.md* die habe ich dann genause behoben wie bei aufgabe 2 nur habe ich nach *git add* statt committ einfach *git rebase --continue* eingegeben

