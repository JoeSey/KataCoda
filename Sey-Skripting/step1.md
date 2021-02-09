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
Dies machen Sie mit ``wget https://gitlab.hhs.karlsruhe.de/Seyfried/sys-skripting1/-/archive/master/sys-skripting1-master.tar``{{execute}}.
Ein ``.tar``-File ist wie eine Zip-Datei, in diesem Beispiel jedoch nicht gepackt. Wir packen das aus mit einem
``tar xf sys-skripting1-master.tar``{{execute}}. Untersuchen Sie die Verzeichnisse mit einem ``tree``{{execute}}.

## User-Skript analysieren
Die erforderlichen Benutzer wurden eigentlich von unserem Hosting-System generiert. In diesem
Beispiel lassen wir sie per Skript erzeugen. Wechseln Sie ins Verzeichnis sys-skripting1-master
und schauen Sie sich dazu die Datei create_users an mit einem ``cat clients/create_users``{{execute}}. 
Was macht die erste for-Schleife?

Versuchen Sie es selber einmal:

``for i in 2 4 6 8 10
do
  echo Hallo $i
done``{{copy}}

Oder übersichtlicher (?) als Einzeiler: ``for i in 2 4 6 8 10; do echo Hallo $i; done``{{copy}}.

Der zweite Teil ist komplizierter. Wir tasten uns heran: Was macht ``seq 19``{{execute}}?
Jetzt noch die Konstruktion ``$( ... )``. Versuchen Sie einmal ein 
``mkdir $(seq 5)``{{execute}}. Was passiert? Schaffen Sie es, nicht nur die Verzeichnisse
1 bis 5 anzulegen, sondern die Verzeichnisse ``test-1, test2, test-3, test-4`` und ``test-5``?

Führen Sie nun das Skript ``create_users`` aus. Was müssen Sie tun?

## Weiter geht's.
Wir haben nun die erforderlichen Benutzer und Verzeichnisse. Weiter geht es im nächsten Schritt.
