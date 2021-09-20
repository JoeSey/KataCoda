# http "von Hand"
Um zu verstehen, wie man Informationen im Netz von einem System zu einem anderen 
transportieren kann, ist es hilfreich, selbstverständliche Aktionen im Internet
einmal "von Hand" nachzuvollziehen.

## Browser im Terminal
Wir benutzen den Befehl "telnet", um uns auf einen Webserver zu verbinden. Worfür ist
der Befehl `telnet` ursprünglich entwickelt worden?

Verbinden wir uns nun auf einen Webserver mit diesem Befehl:
`telnet google.de 80`{{execute}}
Recherchieren Sie nun im Internet, wie Sie von einem Webserver über das
Hypertext Transfer Protocol eine Datei abrufen kann (oder, einfacher einfach 
das Stammverzeichnis /)

## ...und jetzt gezielt
Rufen Sie nun mit telnet die folgende URL ab:
http://www.hhs.karlsruhe.de/static/sey/index.html
