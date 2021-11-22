### Lösung
Die Auflösung ist recht einfach: Sie müssen dem Google-Server, auf den Sie sich mit
`telnet google.de 80`{{execute}}
verbudnen haben, das Kommando
`GET /`{{execute}} 
schicken.

## Status-Codes
Versuchen Sie auf dem Google-Server einmal, 
`GET /nichtda.html`{{execute}} 
abzurufen. Was kommt Ihnen hier bekannt vor?

## Einen Webserver installieren
Installieren Sie nun einen Webserver. Wir werden im folgenden apache2 verwenden, Sie können
aber auch einen anderen Webserver installieren:
`apt update`{{execute}}
(was tut das? Recherchieren Sie und machen Sie sich Notizen!)
`apt install apache2`{{execute}}

## Überprüfen
Lassen Sie sich nun die IP-Adresse Ihres Servers anzeigen:
`ip address`{{execute}}
...und rufen Sie nun mit telnet die Adresse / ab.
