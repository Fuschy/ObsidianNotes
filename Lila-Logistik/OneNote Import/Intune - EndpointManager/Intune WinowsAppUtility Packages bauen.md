Tags: Intune Paketierung Apps
 
Alle Dateien, welche für die Installation benötigt werden, müssen im Source-Folder abgelegt werden (auch die MST-Datei falls nötig)  
Außerdem muss auch ein Output-Folder erstellt bzw definiert werden.
 ![Exported image](Exported%20image%2020250905170258-0.png)     
![Exported image](Exported%20image%2020250905170259-1.png)  

Mit Alt + F über Powershell öffnen  
.\In + Tab
 ![Exported image](Exported%20image%2020250905170301-2.png)  

Über Shift + Rechtklick den Pfad zum Source Ordner kopieren und in der Powershell einfügen (Rechtsklick)  
Den Name mit Endung kopieren und einfügen und in der Powershell einfügen (Rechtsklick)  
Über Shift + Rechtsklick den Pfad des Destination Ordners kopieren und in der Powershell einfügen (Rechtsklick)  
N
 ![Exported image](Exported%20image%2020250905170302-3.png)
 Warten bis Done
 ![Exported image](Exported%20image%2020250905170306-4.png)  

Dann befindet sich die .intunewin-Datei im Output Ordner
 ![Exported image](Exported%20image%2020250905170308-5.png)

Diese kann nun unter Windows | Apps unter Add im Intune hochgeladen werden
 ![Exported image](Exported%20image%2020250905170310-6.png)   
Als App Type Windows app (Win32) auswählen
 ![Exported image](Exported%20image%2020250905170311-7.png)

Den restlichen Schritten folgen. Für Anwendungen mit MST-Datei muss zusätzlich das Install Command angepasst werden.
 
Der folgende Code muss hierbei angepasst werden:
 
`msiexec.exe /I "MSIFILE.msi" TRANSFORMS="MSTFILE.mst" /quiet /norestart`
 
Zuweisung erfolgt über User-Gruppen.