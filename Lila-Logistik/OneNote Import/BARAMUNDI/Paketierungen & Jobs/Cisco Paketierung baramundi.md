1. ZIP-Datei mit Installationsdateien bei Infra anfragen und dann auf den DIP packen.
![Exported image](Exported%20image%2020250905170051-0.png)  
4. Im Baramundi unter Software einen Ordner anlegen und dann oben auf "New" und dann "Application"
![Exported image](Exported%20image%2020250905170052-1.png)  
7. "User baramundi Application Wizard" wählen und Next
![Exported image](Exported%20image%2020250905170053-2.png)  
10. Im Verzeichnis die "Core-VPN-Predeploy" MSI-Datei auswählen und dann auf Next
![Exported image](Exported%20image%2020250905170058-3.png)
      

1. "Create windows installer command line" auswählen und Next
![Exported image](Exported%20image%2020250905170059-4.png)  
4. Standard Einstellungen lassen
![Exported image](Exported%20image%2020250905170100-5.png)  
7. Falls Logging benötigt wird, kann das hier eingestellt werden, wird aber meist nicht benötigt.
![Exported image](Exported%20image%2020250905170101-6.png)  
10. Weitere MSI Properties werden meist auch nicht benötigt
![Exported image](Exported%20image%2020250905170102-7.png)  
13. Die Commandline nochmal überprüfen ob sie richtig aussieht, im Normalfall auch alles Standard lassen.
![Exported image](Exported%20image%2020250905170103-8.png)  
16. Den Kommentar anpassen mit Datum im Format "YYYY-MM-DD - Kürzel", damit man im Nachgang bei Fragen auf die Person zugehen kann.￼Und falls notwendig die anderen Felder noch pflegen, damit die sauber aussehen.
![Exported image](Exported%20image%2020250905170105-9.png)  
19. Nach dem Finish taucht noch die Path Selection auf, hier die Version mit "{DIP}" nehmen.
![Exported image](Exported%20image%2020250905170110-10.png)  
22. Die extended settings müssen im Normalfall auch nicht geöffnet werden, daher hier dann auch auf Finish.
![Exported image](Exported%20image%2020250905170112-11.png)  
25. Das ganze muss dann noch wiederholt werden für "SBL", "DART" und "Umbrella".￼SBL - Start before login - Für die VPN Verbindung vor der Windows Anmeldung

DART - Diagnostics and Reporting Tool - Für eventuelle Troubleshootings  
Umbrella - Für den Umbrella Filter

![Exported image](Exported%20image%2020250905170113-12.png)  
29. Am Ende sollte das so ca. aussehen:
![Exported image](Exported%20image%2020250905170114-13.png)  
32. Die Hauptsoftware "AnyConnect VPN" auswählen und oben auf "Create install job"
![Exported image](Exported%20image%2020250905170115-14.png)  
35. Den Namen dann anpassen, damit es eindeutig aussieht und das "INST:" vorne steht.

Dann bei Job type auf "Active (online only)" stellen, dies stellt sicher das der Job auch nur probiert wird, wenn der Client im baramundi online ist. Dann auf Next

![Exported image](Exported%20image%2020250905170117-15.png)  
39. Um die Restlichen Software Pakete gleichzeitig mit zu installieren, muss hier der Eintrag angeklickt und dann auf "Edit" geklickt werden.
![Exported image](Exported%20image%2020250905170118-16.png)  
42. Dann unten auf "Add"
![Exported image](Exported%20image%2020250905170123-17.png)  
45. In der Selection dann die restlichen drei Software Pakete anwählen und auf OK
![Exported image](Exported%20image%2020250905170124-18.png)  
48. Die Übersicht sollte dann so ca. aussehen und dann auf Finish
![Exported image](Exported%20image%2020250905170125-19.png)  
51. Hier dann wieder auf Next
![Exported image](Exported%20image%2020250905170126-20.png)  
54. Zum Schluss dann auf Finish
![Exported image](Exported%20image%2020250905170128-21.png)