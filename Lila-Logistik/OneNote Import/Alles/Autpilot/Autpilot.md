Intune -\> Wipe kann bis zu 5 min dauern  
Autopilot  
Entra ID
 
Bester Weg: Intune Gerät wipen und dann löschen￼Dann im Autopilot das Gerät löschen  
Dann Entra ID Gerät löschen (falls nicht automatisch weg geht)  
Dann HWID File neu hochladen, damit der Autopilot Eintrag wieder kommt und neu enrollt werden kann
   

Alle 3 Objekte am besten im neuen Tab öffnen  
Reihenfolge beim Löschen:￼￼Erst Wipe dann Delete beim Intune Objekt

![Exported image](Exported%20image%2020250905165547-0.png)  

Dann zum Schluss  
Autopilot

![Exported image](Exported%20image%2020250905165549-1.png)   
Entra ID sollte sich dann von selbst löschen  
Falls nicht, dann da auch noch löschen
 
AD Deaktivieren / löschen
    
Todo 11.11:

- ==Autopilot Deployment Profil für CZ und PL==
- ==Gruppen für jeden Grouptag erstellen (jeweils den Namen anpassen)==
    - ==Gruppenname: PROD :: DE-BES :: Windows Autopilot devices==
    - ==Regeln für Dyn Gruppe:== ==(device.devicePhysicalIds -any _ -eq "[OrderID]:DE-BES")==
- ==Configuration Profile für jeden Standort - Domain Join==
- ==Conditional Access Intune rausnehmen, damit Autopilot klappt - bereits geschehen==
![Exported image](Exported%20image%2020250905165550-2.png)
 
Todo 15.11:  
ADC schauen ob alle OUs gesynced sind die relevant sind - Keine global Admin rechte  
 
 
Skript:￼USB Stick rein  
Shift + F10  
Powershell  
d: hwid.ps1  
Annehmen     
Compliance Status im Entra(setzt sich aus Intune + HW Anforderungen zusammen) ist ein anderer als im Intune

![Exported image](Exported%20image%2020250905165551-3.png)  

Wenn Probleme mit Conditional Access dann im Intune schauen
   

Remediation scripts:￼Sind Logon Scripts, basieren auf Detection und Remediation  
Z.b. ist ein Reg schlüssel vorhanden mit detenction, dann mach remediation
 
Platform Scripts:￼Werden einmalig angewendet
 
Bei Endpoint Security Firewall:￼Vorher die GPOs müssen deaktiviert sein, sonst führt das zu Problemen  
Gleiches bei Antivirus
 
Bitlocker Config:￼

![Exported image](Exported%20image%2020250905165552-4.png)  
![Exported image](Exported%20image%2020250905165553-5.png)      
Für 22.11:

- Firewall in Compliance deaktiviert, da GPO die Domain und Private auf off setzt. -\> Firewall für Autopilot Client aktivieren / GPO deaktivieren
- In den Programmen sind noch Sachen wie Solitair (muss erst runtergeladen werden), XBOX (fehlermeldung gaming-dienste erforderlich), Linkedin (muss erst runtergeladen werden) etc. -\> Klären ob wir das anpassen können oder ob man das normal so lässt.

-\> Geht unter Win11 nicht das Startmenü zu ändern.￼Mal testen mit Fresh Start

![Exported image](Exported%20image%2020250905165558-6.png)- Kann man Onedrive eig direkt SSO? Ohne das man extra drauf klicken muss? -\> Geht nicht. Ist erwartet
- Sperrbildschirm Hintergrund mitgeben -\> Marketing für Win11 kompatibles Bild angefragt -\> Lockscreen experience regkey -\> Für verschiedene Standorte mit Paketen arbeiten
- Bitlocker Key kam nicht -\> Lokale GPO denien
- BIOS PW setzen -\> Bei Dell möglich, kommt auf Modell an -\> Kevin schaut und meldet sich
- PDF Block Android -\> Intune App Protection Gruppe Intune_MAM BYDO rausgenommen
 
Todo:

- Lokale Bitlocker Richtlinie deaktivieren für die Autopilot Clients -\> Erledigt
- Autopilot Gerät gpresult und schauen was zieht
- Export Profile to JSON
 
Für 6.12  
Wie Assettmanagement im Intune? Was können wir am besten machen? Wie machen es andere?￼Intune S/N, Username, Modell, Hersteller, PC Name als CSV und dann damit weitermachen
 
Empfehlung 5€ oder nicht  
Lohnt sich das? Laufzeittest.  
Alles was auf Device ebene ist wird beim pre-provisining
   

Wenn Bitlocker rausgegeben wird, dann rotieren! Aktuellster ist oberster  
Onedrive alte Policies löschen  
Hello Pin nicht ablaufen lassen