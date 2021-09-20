## Berechtigungen vergeben
Nun wird es "ernst". Wir beginnen mit dem Verzeichnis `vertraege`.
Hier sollen die Anwälte Vollzugriff haben, alle anderen Lesezugriff. 
Berchtigungsvergaben unter Unix bestehen immer aus zwei Schritten:

### Benutzer/Gruppen zuweisen
Als erstes ändern wir die Eigentümer-Gruppe des Verzeichnisses auf *anwalt*.
Der Zustand vorher ist:

`ls -l /home/kanzlei`{{execute}}

...nun soll der Gruppen-Eigentümer geändert werden auf *anwalt*. Dies geschieht
zum Beispiel mit diesem Befehl:

`chgrp anwalt vertraege`{{execute}}

Was ist passiert?

`ls -l /home/kanzlei`{{execute}}

Jetzt fehlt für den neuen Eigentümer noch das erweiterte Schreibrecht. Dies setzen
wir mit

`chmod g+w vertraege`{{execute}}

...und vergleichen genau den Vorher- und Nachher-Zustand:

`ls -l /home/kanzlei`{{execute}}

Versuchen Sie es! Loggen Sie sich auf einem neuen Terminal als einer der beiden
Anwalts-Accounts ein (`su adam`) und legen Sie eine neue Datei an. Zum Beispiel mit 
`echo "Das ist wichtig" > /home/kanzlei/vertraege/mein.txt`{{execute}}.

Zurück im ersten Terminal kümmern Sie sich um die anderen Verzeichnisse.
