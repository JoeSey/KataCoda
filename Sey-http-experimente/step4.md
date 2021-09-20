## Zusatzaufgaben
Alles, was nun folgt, ist die "Kür" nach dem Pflichtteil. Sie können sich nun
gerne in Teams koordinieren und gemeinsam eine Lösung erarbeiten.

# Daten an Webserver schicken und speichern
Senden Sie einen "Messwert" an Ihren Webserver und speichern Sie diesen dort ab.
Der Messwert ist unter einer URL abzurufen (z.B. /read.php) und unter einer
anderen abzulegen (z.B. /save.php). Der letzte Messwert wird immer überschrieben,
Sie müssen also keine fancy Datenbank-Anwendung fabrizieren.

## telnet ist nicht genug
Zum Absenden von Datenwerten an den Webserver eignet sich telnet nur bedingt. Eventuell
könnte `curl` hier besser funktionieren.

