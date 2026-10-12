1. Ins **Microsoft Volume Licensing Cente**r gehen und die **benötigte Windows Version herunterladen**.

Dies ist die aktuellste Enterprise Version.￼Zusätzlich muss auch der **Key rausgeschrieben** werden.￼Ich nehme den der "**Müller - Die lila Logistik Service GmbH**" mit dem Type MAK und 500 Lizenzen.
 
ISO-Datei entpacken und in den Ordner "**D:\DIP\OS**" legen.
 
In Baramundi auf **Operating Systems** gehen. Dann mit "**New**" ein neues Operating System anlegen  
Im sich öffnenden Fenster rechts auf die 3 Punkte gehen und dann den Pfad aussuchen wo man die entpackte ISO hingelegt hat.
 ![baramundi Management Center 2021 R2 Jobs X Environ...](Exported%20image%2020250905165939-0.png)  

Bei Bedarf müssen hier noch Daten nachgepflegt werden.  
Type muss passend mit der Windows Version gewählt werden. In diesem Fall wird Windows 11 noch nicht unterstützt, daher wähle ich Windows 10.
 ![operating syste Select tha folder containing the o...](Exported%20image%2020250905165941-1.png)   
Der Source Path muss angepasst werden. Hier auch wieder den Pfad der ISO auswählen.  
Im dem neuen Fenster dann die Variante mit "{DIP}… wählen.  
Haken bei "Use License Management" rein und den Lizenzschlüssel aus dem Volume Licensing Center aus dem ersten Schritt reinkopieren.

![New operating system Wirws or rEwer Configuration ...](Exported%20image%2020250905165942-2.png)  

Haken bei "**Copy files to DIP**" kann raus, da wir diese ja schon am Anfang hingelegt haben.  
Und dann Finish.

![New operating system Rrsh creion Creating operatin...](Exported%20image%2020250905165943-3.png)   
Wenn das Image dann erstellt wurde, muss es noch angepasst werden. Hier werden dann u.a. Cortana oder die XBOX Services deaktiviert.  
Dafür muss man oben auf "**Customize image**", dann noch die Edition auswählen und unten auf "**Load Image**".

![Exported image](Exported%20image%2020250905165945-4.png)  

Nach dem Load öffnet sich ein Fenster wo man das OS noch etwas anpassen kann.  
Ich habe nur folgendes gemacht: (Fett markiert wurde geändert)

![baramundi OS Customization Tool O Overview 9 Featu...](Exported%20image%2020250905165946-5.png)  
![baramundi OS Customization Tool O Overview 9 Featu...](Exported%20image%2020250905165947-6.png)  

Zum Schluss auf "**Save Image"** und "**Yes"**.
   

Danach muss der Job für das erstellte Image gemacht werden.  
Hierfür bei **Jobs** in den Ordner **Operating Systems** und dann auf **New** -\> **Job for Windows device**

![baramundi Management Center 2021 R2 Jobs X Environ...](Exported%20image%2020250905165951-7.png)  

**Name eingeben** und **"Next"**

![New job Tha job wizard will guida you through the ...](Exported%20image%2020250905165952-8.png)  

Deploy Operating System

![Create Edit ob ste This wizard guides you while ad...](Exported%20image%2020250905165954-9.png)  

Bei "OS" im Dropdown Menü das vorhin erstellte OS auswählen.

![CreateEdit job step Wth this step an operating sys...](Exported%20image%2020250905165955-10.png)  

Und bei den Options den Haken "Leave network boot as first boot option (only UEFI) rausnehmen.

![CreateEdit job step Wth this step an operating sys...](Exported%20image%2020250905165956-11.png)  

Den Bildschirm so lassen und Finish.

![reateEdit job step This step will boot the specifi...](Exported%20image%2020250905165957-12.png)  

Danach "**Next**" und nochmal auf "**Finish**" um den Job fertig zu stellen.