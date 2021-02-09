## Verzeichnisse wechseln
So könnte Ihr Skript jetzt aussehen:

``
for dir in clients/*
do
  cd $dir
  pwd
  cd ../..
done``{{copy}}

### Eigentümer ändern
Als letztes muss noch eine Schleife über die jeweiligen web-Verzeichnisse 
laufen. Die Eigentümer einer Datei ändern wir unter Unix mit

``chown web1:client1 index.html``{{copy}}

Anstatt dem ``pwd``im letzten Schritt muss jetzt eine weitere Schleife über 
die ``web*`` im aktuellen Verzeichnis kommen und darin der chown ausgeführt werden.

Tauschen Sie sich untereinander aus!