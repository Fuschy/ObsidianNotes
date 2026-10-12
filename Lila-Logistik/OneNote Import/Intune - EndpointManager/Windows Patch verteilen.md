Zuerst muss das gewünschte Windows Update im Windows Update Catalog ([https://www.catalog.update.microsoft.com/Home.aspx](https://www.catalog.update.microsoft.com/Home.aspx)) heruntergeladen werden
 
Anschließend muss mit dem Microsoft Win32 Content Prep Tool (Download: [https://github.com/Microsoft/Microsoft-Win32-Content-Prep-Tool](https://github.com/Microsoft/Microsoft-Win32-Content-Prep-Tool)[GitHub - microsoft/Microsoft-Win32-Content-Prep-Tool: A tool to wrap Win32 App and then it can be uploaded to Intune](https://github.com/Microsoft/Microsoft-Win32-Content-Prep-Tool)) die .msu-Datei in eine .intunewin-Datei umgewandelt werden:
 ![Computergenerierter Alternativtext Please specify ...](Exported%20image%2020250905170239-0.png)

|              |                |                                                                                                                                                              |
| ------------ | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Erläuterung: | Source Folder  | Der Ordner, in dem sich die .msu-Datei befindet, soll angegeben werden                                                                                       |
|              | Setup-File     | Hier soll der Name der .msu-Datei angegeben werden. MIT Dateiendung                                                                                          |
|              | Output-Folder  | Hier wird die .intunewin-Datei abgelegt                                                                                                                      |
|              | Catalog-Folder | Prinzipiell N, ein Catalog-Folder kann angegeben werden, wenn alle Dateien in diesem Ordner als Catalog File behandelt werden sollen (für Windows 10 S Mode) |
 
Danach sollte sich die .intunewin-Datei im vorher spezifizierten Ordner befinden.  
______________
 
Wenn das erledigt ist, kann der Patch im Intune folgendermaßen verteilt werden:
 
Unter **Apps \< Windows \< Hinzufügen** und im Drop-Down Menü als App-Typ _"_**Windows-App (Win32)**_"_ auswählen

![Computergenerierter Alternativtext AppTyp auswhlen...](Exported%20image%2020250905170241-1.png)   
Anschließend die intune-Datei auswählen und eine **aussagekräftige Beschreibung (Grund für Patch)** hinterlegen und den Namen folgendermaßen vergeben: **Patch:: KB\<Nummer\>-x64**

![Computergenerierter Alternativtext App hinzufgen W...](Exported%20image%2020250905170243-2.png)   
Als Installationsbefehl und Deinstallationsbefehl folgendes hinterlegen:

![Computergenerierter Alternativtext App hinzufgen W...](Exported%20image%2020250905170244-3.png)  

|   |   |   |
|---|---|---|
|Erläuterung|Installationsbefehl|wusa.exe **\<full path of the .msu file\>** /quiet /norestart -Wait|
||Deinstallationsbefehl|wusa.exe /uninstall /kb:**\<KB-Nummer\>** /quiet|
   

Auf der nächsten Seite die Betriebssystemarchitektur und das mindestens erforderliche Betriebssystem aus dem Drop-Down-Menü auswählen

![Exported image](Exported%20image%2020250905170245-4.png)   
Auf der nächsten Seite muss das Regelformat angepasst werden:

![Exported image](Exported%20image%2020250905170246-5.png)

Als Skriptdatei **muss** eine ps1 geschrieben und hinterlegt werden, die folgendermaßen aussieht (entsprechende KB Nummer noch hinterlegen):
 
`$result = systeminfo.exe | findstr KB\<KB number\>`
 
`if ($result)`  
`{`  
`Write-Output "Found KB\<KB number\>"`  
`exit 0`  
`}`  
`else`  
`{`  
`exit 1`  
`}`  
____________________________________
 
Der Punkt **Abhängigkeiten** und **Ablösung** kann übersprungen werden.
 
Zum Schluss müssen noch die Zuweisungen erfolgen:  
Hier sollten noch nicht alle Mitarbeiter aufgenommen werden, sondern erst die Testgruppen!

![Exported image](Exported%20image%2020250905170247-6.png)  

Je nach Art des Patches müssen noch Filter erstellt werden, Popupbenachrichtigungen unterdrückt werden etc.
 
Wichtig: Es kann immer nur ein Filter ausgewählt werden, dementsprechend müssen also Filter miteinander durch **ODER** verknüpft werden.  
Filter können unter **Apps \< Filter** erstellt werden.
 
Tags: Intune, Patch-Management


