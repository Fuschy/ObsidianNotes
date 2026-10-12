![Computergenerierter Alternativtext DIPBE3VOl State...](Exported%20image%2020250905170031-0.png)  

Sehr geehrter Herr Mayershofer,
 
  dieser Fehler hat häufig folgenden Hintergrund und kann anhand folgender Beschreibung gelöst werden:
 
Prüfen Sie vorab,  
 - dass in der Firewall, in Richtung baraDIP Server, der Port 10083/TCP offen ist.  
 - dass die installierte baraDIP Version identisch zur baramundi Server Version ist.  
   
Öffnen Sie auf dem baraDIP Server eine cmd (als Administrator gestartet) und geben hier folgendes ein:  
**"C:\Program Files (x86)\baramundi\baraDIP\baraDIPConfig.exe" /Communication=http**  
   
 Es öffnet sich die baraDIPconfig.exe, diese können Sie bestätigen und auch gleich wieder schließen.  
 Öffnen Sie jetzt zur Kontrolle, ob die Eingabe funktioniert hat, folgende Datei mit einem Editor: "C:\Program Files (x86)\baramundi\baraDIP\Apache\conf\**httpd.conf**".  
 Wenn in der Zeile 23 "**Listen 10083**" steht, hat die cmd Eingabe (die Rückstellung von https auf http) funktioniert, steht hier allerdings noch "**Listen 10083 https**", muss der cmd Befehl auf einen Schreibfehler kontrolliert werden und nochmal eingegeben werden.  
   
 Löschen Sie jetzt die Zertifikatsdatei "C:\Program Files (x86)\baramundi\baraDIP\Apache\conf\**mycert.crt**".  
 In der BMC \> Konfiguration \> DIP-Verwaltung \> DIP-Server editieren Sie Ihren baraDIP Eintrag und passen im Feld Name den Wert auf (z.B.) den FQDN an. (Durch diesen Wert wird gleich das neue Zertifikat ausgestellt).  
 Entfernen Sie zudem das Häkchen bei "HTTPS" im gleichen DIP Eintrag.  
 Markieren Sie jetzt den baraDIP Eintrag in der BMC und klicken oben in der Menüleiste (oder im Kontextmenü) auf "HTTPS konfigurieren".  
   
 Das Zertifikat auf dem baraDIP Server wird neu ausgestellt, und baraDIP wird zugleich auf HTTPS umgestellt.  
   
 Warten Sie jetzt ca. 60 Sekunden und prüfen dann in der BMC, ob die Kommunikation zum baraDIP Dienst jetzt funktioniert.  
 
 
Bitte achten Sie beim Senden einer E-Mail darauf, dass der Betreff die Ticketnummer  
in Klammern beinhaltet: z.B. (#12345).
 
Mit freundlichen Grüßen,
 
Michael Smoczok  
Support Specialist