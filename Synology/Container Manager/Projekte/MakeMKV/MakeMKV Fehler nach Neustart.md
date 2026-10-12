![[Pasted image 20251027105442.png]]

Fehlermeldung enthält "/dev/sgX" -> Liegt daran, dass das Laufwerk zum Rippen auf einen anderen Slot gefallen ist.

Lösung:
In den Logs auf der Synology Container Manager schauen, welches Device er erkennt und hinzufügen will.
Dann ggfs. in der YAML Datei anpassen.

Befehle per SSH die eventuell helfen können:
lsscsi -g -> Zeigt alle angeschlossenen Devices an. Weiß nicht mehr genau wie der funktioniert.
"sudo chmod 0666 /dev/sgX" -> X für die Nummer die man in Log findet.