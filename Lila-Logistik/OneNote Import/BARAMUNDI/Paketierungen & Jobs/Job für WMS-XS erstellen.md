Anfrage kommt im Normalfall vom BCP Team, mit einer Mail von Körber.￼In dieser Mail ist der **Download Link** vom Installationspaket.  
Doku ist am Beispiel vom WMS-Gliwice Archiv gemacht.
 ![CALL75400 GLI WMSX Archivumgebung Installer Servic...](Exported%20image%2020250905170130-0.png)  

1. Zip aus dem Link herunterladen 
2. Entpacken und nach "**D:\Dip\Apl\WMS…**" verschieben, ggfs. Muss ein neues Verzeichnis erstellt werden sollte eine neue Instanz von WMS eingeführt werden.
![Home Fav o rites Desktop Downloads Recent places S...](Exported%20image%2020250905170131-1.png)  
3. Ordner dann umbenennen, damit man erkennt um welches System es sich handelt.
![GLI Home Fav o rites Desktop Downloads Recent plac...](Exported%20image%2020250905170136-2.png)  
4. BDS Skript von einem bestehenden Installer, kopieren und in den neu angelegten Ordner einfügen.
![chi Home Favo rites Desktop L Downloads Recent pla...](Exported%20image%2020250905170138-3.png)  
5. BDS Skript öffnen und die Daten darin anpassen
![Install WMSX Gliwice Archivbds X Action 8 202707 5...](Exported%20image%2020250905170140-4.png)  
Folgende Anpassungen müssen gemacht werden:
- Zeile 2 und 3: Sind Informationszeilen, damit man nachvollziehen kann wer welchen Job erstellt hat und bei Rückfragen ggfs. nachhaken kann.
- Zeile 5: Den Pfad anpassen, damit das richtige System drin steht.
![Folder name Create Folder lnstall WMSX GLI Archiv ...](Exported%20image%2020250905170141-5.png)
- Zeile 6: Neuen Quellordner angeben (den, den man davor unter DIP\Apl\WMS… angelegt hat). Wichtig dass "{DIP}" vorne ist wie im Screenshot. Dadurch weiß der Client dann, dass er auf den nächst besten DIP schauen soll.
  Zusätzlich den Zielordner anpassen, auf den aus Zeile 5
![S ouce folder T arget folder Options Copy Files DI...](Exported%20image%2020250905170142-6.png)
- Zeile 7: Die erste Zeile anpassen auf den Zielpfad aus Zeile 5. Zweite Zeile muss nach "**call** " die **.cmd Datei** angegeben werden, die Körber oder das BCP im Ticket nennt zum Ausführen. Hier **nur** der **Dateiname**, ohne die Dateiendung (.cmd).
![Run Embedded CMD CMD cd GLI_Archiv call rt_muea08 ...](Exported%20image%2020250905170144-7.png)
- Zeile 8: Pfad aus Zeile 5 angeben, damit dieser dann nach Installation wieder gelöscht werden kann.
![Folder name Remove Folder GLI_Archiq Cancel](Exported%20image%2020250905170145-8.png)
- Zeile 9: Ist zuständig für die Umbenennung der Verknüpfung nach der Installation. Hierfür bietet es sich an, die Installation einmal manuell durchzuführen, damit man weiß wie sich das Programm nennt nach der Installation und ob die Pfade auch stimmen.
 
6. Danach müssen noch die Script Properties geändert werden.
![Open X Close Save All Save as Exe Print CtrlN Ctrl...](Exported%20image%2020250905170149-9.png)  
   
7. Zum Schluss speichern und dann kann eine Software in Baramundi erstellt werden aus diesem .BDS Skript und daraus dann der Job.