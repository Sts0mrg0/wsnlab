### Setup:
Das Netzwerk besteht aus intel edisons, auf denen jeweils Contiki l�uft.
Statt dem standartm��ig installierten Yocto wurde Ubininux verwendet, um leichter Paktekte installieren zu k�nnen. Neben dem aktuellsten Ubilinux wurde au�erdem die aktuellste Version von mraa verwendet (Stand Januar 2016).
Das Contiki basiert auf einem UDP-Beispiel. Es gibt einen Server und mehrere (3 wurden getestet) Clients mit einem Platipus Board.
Der Server �ffnet einen WLAN-Accesspoint, die Clients w�hlen sich ein. Die Kommunikation erfolgt �ber IPv6, der jeweilige Addresspr�fix wird als Argument beim Aufruf �bergeben.
Um die Anwendung zu starten muss auf jedem client das configure_routes.py script ausgef�hrt werden.
Auf dem Master muss das Script master-routes.sh ausgef�hrt werden.

#### Code
Da an Contiki viele �nderungen vorgenommen werden mussten, wird es mit eingereicht.
Der eigentliche Programmcode liegt im Contiki Ordner unter /apps/wsn-client bzw /apps/wsn-server.
Die Hauptroutinen f�r die Applikation sowie die Prozesse befinden sich in wsn.c, wiederverwendbare Teile der Software sind in c- und h-Files ausgelagert.

### Teammitglieder
Marc S., Niklas D., Thomas S., Simon K., Daniel W.
