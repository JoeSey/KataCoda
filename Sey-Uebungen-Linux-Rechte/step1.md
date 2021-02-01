# Übungen Benutzer in Linux
Heute soll ein kleines Szenario in Linux erstellt werden: vier Benutzer mit einem 
gemeinsamen Verzeichnis, in dem unterschiedliche Benutzergruppen unterschiedliche
Berechtigungen haben sollen.

## Schritt 1: Benutzer anlegen
Benutzer legen wir an mit `adduser`. Es sollen die Benutzer adam, berta, charlie
und donald angelegt werden. Dies machen wir mit
`adduser adam`{{execute}}
...danach muss ein Passwort vergeben werden und einige zusätzliche Informationen.

Diese Benutzer kann man, sobald sie angelegt sind, gleich testen: Am besten macht
man dazu ein neues Terminal auf (mit dem weißen Plus-Symbol neben der Überschrift
"Terminal"). Dann kann man in den neuen Account wechseln mit
`su adam`{{execute}}
und überprüfen, welchen Account man benutzt mit einem
`whoami`{{execute}}

### Restliche Benutzer
Legen Sie nun die Benutzer berta, charlie und donald an. Danach geht es weiter mit
den Benutzergruppen:
