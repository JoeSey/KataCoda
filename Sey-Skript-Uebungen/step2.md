## Aufgabe 2 - Vergleiche
Hier sollen Sie Zahlen vergleichen. Versuchen Sie einmal diese Zeile auszuführen:

``if [ 3 -lt 5 ]; then echo "drei ist kleiner als fuenf!"; fi``{{execute}}

Hierbei steht ``-lt`` für *less than*.

Wenn Sie wissen wollen, wie dieses komische if in der Shell funktioniert, versuchen Sie
einmal das hier:

``help test``{{execute}}

...das wirft Ihnen alle möglichen Tests, also if-Abfragen aus. Jetzt müssen
Sie sich nur noch daran erinnern, dass in ``$1`` der erste Parameter steht. Also, 
wenn Sie dieses Skript hier:

``#!/bin/bash
echo "Mein erster Parameter ist: $1"
``{{copy}}

...aufrufen mit ``./skript blah blubb``, dann ist das Ergebnis ``blah``.

Los geht's!

Für die Teilaufgabe b) sollten Sie noch wissen, dass in der Spezial-Variable ``$#`` die Anzahl
der übergebenen Parameter steckt.