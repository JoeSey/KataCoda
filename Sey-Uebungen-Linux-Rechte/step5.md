## Weitere Verzeichnisse
Eine mögliche Lösung der Aufgabe sieht so aus:
`$ ls -l
total 16
drwxr-xrwx 2 root root   4096 Feb  1 09:53 austausch
d------rwx 2 root azubi  4096 Feb  1 09:55 briefe
d---rwx--- 2 root anwalt 4096 Feb  1 09:53 chefsachen
drwxrwxr-x 2 root anwalt 4096 Feb  1 09:54 vertraege`

## Warum das t-Bit wichtig ist
In der abschließenden Aufgabe machen wir Unfug mit dem 
austausch-Ordner.
`su adam
echo "Der Azubi donald bekommt ein Anfangsgehalt von 500€ monatlich" \
> /home/kanzlei/austausch/gehalt.txt
exit
su donald
cd  /home/kanzlei/austausch/`{{execute}}

Nun sind Sie als Benutzer *donald* im Verzeichnis `austausch`. Versuchen
Sie zunächst, mit `nano gehalt.txt` die Datei zu ändern. Warum geht das nicht?
(Sie kommen mit Strg-X aus dem Editor nano wieder heraus). Dann tricksen wir
eben:

`cp gehalt.txt meins.txt
nano meins.txt
`

Geben Sie nun Ihre Gehaltsvorstellung in diese neue Datei ein und speichern
Sie mit Strg-O, Enter. Wieso geht das nun?

Jetzt löschen wir das Original und benennen unsere Datei so wie die ursprüngliche
Datei hieß:

`rm gehalt.txt`{{execute}}

(was soll diese komische Warnung? Ignorieren Sie diese!) Und:

`mv meins.txt gehalt.txt
ls -l`{{execute}}

Was verrät uns? Verhindern Sie nun solche Manipulationen, indem Sie das t-Bit für
den Austausch-Ordner setzen und versuchen Sie das Szenario erneut.

