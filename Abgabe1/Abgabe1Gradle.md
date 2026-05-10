Um auf der Konsole herauszufinden welche Tasks es gibt, gebe ich ".\gradlew tasks" ein

Java Dateien kommen in app/src/main/java/
JUnit_Testdateien kommen in app/src/test/java/
Externe Dateien wie Bilder oder so kommen in app/src/main/resources/


Unter plugins kann man Gradle neue Funktionen hinzufügen und sagen was Gradle noch so können soll.

Unter repositories legt man fest wo Gradle nach externen Bibliotheken suchen soll. meist mavenCentral()

Bei dependencies werden alle externen Bibliotheken die man dann braucht aufgelistet
und sagt auch direkt wofür man diese braucht, also testen, Applikation 

bei application sage ich was die hauptklasse ist und welche gestartet werden soll
Tasks für application sind zum Beispiel:
run: Dieser Task startet deine Anwendung direkt aus dem Quellcode. Er sucht die in der build.gradle festgelegte mainClass und führt deren Main Methode aus.
startScripts: Erstellt Betriebssystem-spezifische Startdateien. Diese Skripte regeln automatisch das Laden aller benötigten Programmbibliotheken.
distZip / distTar: Diese Tasks bündeln die gesamte Anwendung in ein komprimiertes Archiv. Dies ist das Paket, das du an andere Personen verschicken kannst, damit diese dein Programm nutzen können.





