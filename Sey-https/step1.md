# https mit Zertifikaten "von Hand"
Dieses Szenario soll zeigen, wie man http mit einem SSL-Zertifikat absichern
kann und welche Probleme dabei entstehen.

## Webserver installieren
Damit wir mit dem Browser http**s** ausprobieren können, muss zunächst einmal
**http** funktionieren. Installieren Sie den Webserver wie in der letzten Übung
mit 

`apt install apache2`{{execute}}
Verbinden Sie sich nun mit dem Browser auf Ihren Server.

## ...und nun SSL aktivieren
Das aktivieren von SSL in Apache ist denkbar einfach (dies sicher zum Laufen
zu bekommen, dafür um so mehr. Aber eins nach dem anderen):

`a2enmod ssl`{execute}
