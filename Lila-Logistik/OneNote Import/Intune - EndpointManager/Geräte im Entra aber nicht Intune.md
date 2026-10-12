Passiert wenn man sich am PC anmeldet und der User noch keine Lizenz hatte, die ihn berechtigt das Gerät im Intune zu onboarden. E3/F3 reichen dafür aus.
 
Fehler erkennbar in der Ereignisanzeige:￼Anwendungs- und Dienstprotokolle  
Microsoft  
Windows  
DeviceManagement-Enterprise-Diagnostics-Provider  
Administrator
 
Dort dann Ereignis-ID 76 ist der Fehler.

![Exported image](Exported%20image%2020250905170253-0.png)   
Zum fixen muss man folgendes machen:￼Windows-Taste + R￼%windir%\system32\GroupPolicy
 
Dort dann alles rauslöschen. Dadurch wird der gesamte GPO Cache geleert.  
Dann einmal "gpedit.msc" als Admin öffnen, damit die Standardordner wieder generiert werden.
 
Danach den PC neustarten und dann ein gpupdate /force machen.
 
Dann sieht man in der Ereignisanzeige eine Ereignis-ID 75 die bestätigt das es funktioniert hat.￼Es braucht danach ca. 5-10 Minuten bis das Gerät sauber im Entra UND Intune auftaucht.

![Exported image](Exported%20image%2020250905170254-1.png)  

Ggfs. weiteres Troubleshooting:￼dsregcmd /leave  
Dsregcmd /join
 
Dadurch werden die Geräte aus dem Entra entfernt und neu gejoined.

![Exported image](Exported%20image%2020250905170256-2.png)