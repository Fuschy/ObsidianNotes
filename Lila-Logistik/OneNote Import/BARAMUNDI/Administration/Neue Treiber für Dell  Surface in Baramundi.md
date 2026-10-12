Für Dell:  
Nach Modellname + Treiberpaket googlen (evtl. auch hier auffindbar: [Treiberpakete der Dell Familie | Dell Deutschland](https://www.dell.com/support/kbdoc/de-de/000180534/treiberpakete-der-dell-produktreihe))  
Dann sollte man eine Seite wie diese finden: [Latitude 5520 Windows 10 Treiberpakete | Dell Deutschland](https://www.dell.com/support/kbdoc/de-de/000182132/latitude-5520-windows-10-treiberpakete)  
Alternativ kann man auch [hier](https://www.dell.com/support/kbdoc/de-de/000124139/dell-command-deploy-driver-packs-for-enterprise-client-os-deployment) sich das passende Gerät raussuchen

![OptiPIex 3090 Windows 1 0 Treiberpaket Zusammenfas...](Exported%20image%2020250905165850-0.png)

Dort das Treiberpaket herunterladen  
Diese .cab Datei dann entpacken mit 7Zip / WinRar  
Bei einer .exe Datei dann diese starten, dadurch wird das extrahieren gestartet  
Den Inhalt auf den VSBES-CMS01 verschieben: D:\DIP\Driver\Dell Inc\*Modellname*\  
Der Ordner *Modellname* muss erstellet werden, falls er nicht vorhanden ist.  
Am besten bei den bereits vorhandenen Ordnern vergleichen  
Danach: [[Treiber ins Image WIN PE (PXE)]]
   

Für Surfaces:  
Wenn es ein neues Surface ist was noch nicht im baramundi war, dann einmal "normal" einrichten um ins Windows zu gelangen.  
Dort dann nach Modellname + Treiberpaket googlen  
Dann sollte man eine Seite wie diese finden: [Download drivers and firmware for Surface (microsoft.com)](https://support.microsoft.com/en-us/surface/download-drivers-and-firmware-for-surface-09bb2e09-2a4b-cb69-0951-078a7739e120)  
Etwas weiter unten muss das Modell ausgewählt werden  
Dann den passenden Link öffnen und die .MSI herunterladen  
MSI installieren und den Pfad aus der Installation merken, nach der Installation sind in diesem Pfad alle Treiber  
Den gesamten Treiber Ordner rauskopieren auf einen USB Stick und dann auf den VSBES-CMS01 schieben.  
Pfad ist dann D:\DIP\Driver\Microsoft Corporatoin\*Modellname*\  
Der Ordner *Modellname* muss erstellt werden, falls er nicht vorhanden ist  
Danach: [[Treiber ins Image WIN PE (PXE)]]