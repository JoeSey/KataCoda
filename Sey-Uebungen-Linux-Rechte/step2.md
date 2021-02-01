## Gruppen anlegen
Gruppen dienen unter Unix dazu, Benutzer zusammenzufassen, die dieselben
Berechtigungen haben sollen. Genau wie der Befehl `adduser` gibt es unter
Linux (Debian und Ubuntu und "verwandte" Distrubitionen) den Befehl
`addgroup`. Probieren wir es aus, die Gruppen *anwalt*, *mitarbeiter*
und *azubi* sollen angelegt werden:
`addgroup anwalt`{{execute}}
und dann packen wir den Benutzer *adam* in die Gruppe *anwalt*:
`adduser adam anwalt`{{execute}}
Eine Alterntive zu diesem Befehl ist `usermod`, den es auch auf anderen
Distributionen gibt:
`usermod -a -G anwalt berta`{{execute}}
...dies weist dem Benutzer *berta* die **zusätzliche (-a)** Gruppe
*anwalt* zu.

Legen Sie nun die restlichen Gruppen an und weisen Sie die Benutzer
zu wie angegeben.

## Überprüfen
Sie können prüfen, in welchen Benutzergruppen ein Linux-Benutzer ist,
indem Sie `groups adam`{{execute}} ausführen. Hier können Sie natürlich
auch einen anderen Benutzernamen angeben - wenn Sie keinen Benutzer angeben, 
werden die Gruppen ausgegeben, in denen der aktuelle Benutzer Mitglied ist.
