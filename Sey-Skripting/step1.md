# Übungen Skripting in Linux
Das Szenario heute soll das Thema Skripting weiter vertiefen. Es ist ein Anwendungs-
Szenario für eine Webhosting-Umgebung. Dort gibt es Kunden-Accounts, ``client1``,
``client2``,... und jeder Kunde kann eine oder mehrere Web-Präsenzen haben. Diese
heißen ``web1``, ``web2``,...

Bei der Migration von einen älteren Hosting-System musste diese Struktur neu aufgebaut
werden. Nun haben wir das Problem, dass die Eigentümer-Eigenschaften nicht mehr stimmen.
Um sich die Situation anschauen zu können, müssen Sie sich zunächst die Verzeichnis-Struktur
holen.

## Beispiel-Dateien laden
Dies machen Sie mit ``git clone ``{execute}. Untersuchen Sie die Verzeichnisse mit
einem ``tree``{execute}.

## Benutzer anlegen
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
