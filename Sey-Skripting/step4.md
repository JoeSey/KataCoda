## Verzeichnisse wechseln
So könnte Ihr Skript jetzt aussehen:

``
for dir in clients/*
do
  cd $dir
  pwd
  cd ../..
done``{{copy}}

*Wichtig:* bevor Sie dies ausführen, schieben Sie create_users aus dem clients-Verzeichnis.
Sie können dies mit ``mv /root/sys-skripting1-master/clients/create_users ~``{{execute}}
machen. Sonst landen Sie anschließend im Verzeichnis / 

(warum?!)

### Eigentümer ändern
Als letztes muss noch eine Schleife über die jeweiligen web-Verzeichnisse 
laufen. Die Eigentümer einer Datei ändern wir unter Unix mit

``chown web1:client1 index.html``{{copy}}

Anstatt dem ``pwd``im letzten Schritt muss jetzt eine weitere Schleife über 
die ``web*`` im aktuellen Verzeichnis kommen und darin der chown ausgeführt werden.

Tauschen Sie sich untereinander aus!