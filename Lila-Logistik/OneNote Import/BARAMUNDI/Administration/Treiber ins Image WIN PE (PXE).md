Vorher muss voraussichtlich das hier gemacht werden: [Neue Treiber für Dell / Surface in Baramundi](Neue%20Treiber%20für%20Dell%20%20Surface%20in%20Baramundi.md)￼￼Auf dem CMS-BES-V01 die bMC öffnen.
 
In die Configuration \> Tools \> Boot Media Wizard

![baramundi Management Center 2021 RI Overview Organ...](Exported%20image%2020250905165852-0.png)   
Windows PE network boot image auswählen

![baramundi Management Su Boot Media Wiza This wizar...](Exported%20image%2020250905165856-1.png)   
CMS-BES-V01 auswählen falls nicht automatisch drin steht

![Exported image](Exported%20image%2020250905165857-2.png)
   

Architecture auf "x64" und Boot Mode auf "UEFI" stellen.  
Danach im untersten Pfad folgenden auswählen: D:\DIP\bMS\TFTPRoot\x64_uefi

![amundi Management Suite Boot Media Wizar Wirws PE ...](Exported%20image%2020250905165858-3.png)  

Dort erscheint dann eine Liste mit Treibern die bereits eingebunden sind ins Image  
Über Add fügt man dann die neuen benötigten Netzwerk Treiber hinzu

![baramundi Management Suite Boot Media Wizard ivas ...](Exported%20image%2020250905165859-4.png)  

Tags: Baramundi, Image, Preboot, WinPE, Boot Media Wizard, Treiber