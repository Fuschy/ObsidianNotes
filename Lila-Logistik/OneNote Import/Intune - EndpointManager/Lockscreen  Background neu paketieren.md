Aus folgender Doku: [Set Desktop & Lock Screen Wallpaper Using Intune Win32 App](https://cloudinfra.net/set-desktop-lock-screen-wallpaper-using-intune-win32-app/#updating-the-desktop-and-lock-screen-wallpaper)

1. Lockscreen und Background Bilder mit entsprechender neuen Versionsnummer benennen.
   ![Exported image](Exported%20image%2020250905170314-0.png)
   Die aktuelle Nummer bekommt man aus der App im Intune raus:
   ![Exported image](Exported%20image%2020250905170316-1.png)  
2. Das bauen des IntuneWin Paketes muss jeweils separat gemacht werden.
   Dafür die IntuneWinAppUtil starten.
   Den Source Folder angeben, in dem die Bilder liegen.
   Als Setup File den Dateinamen mit Endung angeben.
   Als Output Folder den Pfad des Speicherortes der IntuneWin Datei angeben.  
   Den Catalog Folder mit "N" anwählen und bestätigen.
   ![Exported image](Exported%20image%2020250905170317-2.png)
   Prozess dann wiederholen für das andere Bild.

3. Der Output Ordner sollte dann ca. so aussehen:
   ![Exported image](Exported%20image%2020250905170321-3.png)  
4. Im Intune in die Entsprechende App gehen, hier am Beispiel vom Background.
   Erst auf Properties und dann bei den App Informationen auf Edit
   ![Exported image](Exported%20image%2020250905170323-4.png)  
5. Danach auf den Hyperlink bei "Select file to update" klicken und dann im neuen Menü die in Punkt 2 erstellte IntuneWin Datei auswählen und mit OK bestätigen.
   Dann noch entsprechend die App Version auf die neue ändern. Hier im Beispiel dann von 1.0 auf 2.0.
   Rest auf dieser Seite lassen und unten mit "Review + save" weiter gehen.
   ![Exported image](Exported%20image%2020250905170324-5.png)  
6. Im nächsten Abschnitt müssen die Install und Uninstall commands angepasst werden.
   Hier muss entsprechend nur der Dateiname des Bildes angepasst werden auf den in Schritt 1 vergebenen.
   Im Anschluss auch wieder mit "Review + save" bestätigen.
   ![Exported image](Exported%20image%2020250905170325-6.png)  
7. Die Requirements können übersprungen werden und bei den Detection rules klickt man dann auf den Hyperlink bei "File".
   Dort muss dann bei "File or folder" ebenfalls der Dateinamen angepasst und mit "OK" bestätigt werden.
   Danach auch wieder auf "Review + save" gehen.
   ![Exported image](Exported%20image%2020250905170327-7.png)  
8. Die Übersicht zum Schluss mit "Save" bestätigen und das Paket ist fertig gebaut.
   Das ganze muss dann entsprechend für den Lockscreen auch gemacht werden, sollte dieser geändert werden.

9. Danach muss noch das Configuration profile angepasst werden.
   Das Profil heißt aktuell PROD :: WIN :: Background & Lockscreen
   Im Configuration Profil runterscrollen und bei den Configuration settings auf Edit klicken.
   ![Exported image](Exported%20image%2020250905170328-8.png)  
10. Dort dann ebenfalls wieder die Dateinamen entsprechend anpassen und mit "Review + save" bestätigen    ![Exported image](Exported%20image%2020250905170329-9.png)  
11. Danach kann es etwas dauern bis sich die Geräte synchronisieren und das Bild ziehen. Es wird jedoch auf jedenfall dann ein Neustart benötigt. Ob das Bild auch auf dem Gerät ist, kann man über den Pfad "C:\Windows\Web\Wallpaper\" sehen.