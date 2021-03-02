## Das Ziel
Was wir wollen, ist das folgende:

Jedes Verzeichnis im Verzeichnisbaum soll in der Gruppe ``clientx`` gehören
und jede html-Datei dem Benutzer ``weby``, mit den passenden Zahlen x und y.

Beispiel:

``
drwxr-x--- 13 web19 client9 4096 Jan 24 14:59 index.html
``

...im Verzeichnis clients/client9/web19. Von Hand ist das echt stressig. 
Also schreiben wir ein kleines Skript.

## Editor anwerfen!
Starten Sie Ihren Lieblingseditor. Oder verwenden Sie ``nano fix_users``{{execute}}.
Wenn Sie wollen, können Sie oben über dem Terminal-Bereich auf das "+" Icon klicken
und in einem zweiten Fenster das Skript ausprobieren (Achtung: ins gleiche Verzeichnis
wechseln. Und: das Skript abspeichern, bevor Sie es ausführen!)

Was sollte in der ersten Zeile Ihres Skripts stehen?

(Wir sind jetzt im Verzeichnis sys-skripting1-master. Falls Sie sich "verlaufen" haben,
machen Sie vorher bitte ein ``cd /root/sys-skripting1-master``{{execute}}).


Schreiben Sie zunächst eine Schleife, die über die client-Verzeichnisse iteriert:

``
cd /root/sys-skripting1-master/clients
for dir in *
do
  echo "Verzeichnis $dir"
done
``{{copy}}

Speichern und Ausführen, dann geht es weiter.
