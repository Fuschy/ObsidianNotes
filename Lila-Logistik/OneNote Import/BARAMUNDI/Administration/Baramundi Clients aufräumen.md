1. Um einen Export aus baramundi zu ziehen, welche Clients denn veraltet sind, muss man in das Environment, danach die Logical Group und dann "Include subfolders" aktiviern.
![Exported image](Exported%20image%2020250905165902-0.png)   5. Dann alle markieren die sich länger als die gewünschte Zeit nicht gemeldet haben, meistens alles mehr als 3 Monate.

Darauf dann Rechtsklick, auf Extras und "Save as static group" und dann im öffnenden Fenster auf Save.

![Exported image](Exported%20image%2020250905165903-1.png)  
9. In der Static Group dann nochmal gegenprüfen was für Geräte dort sich befinden. Manchmal sind es Server oder z.B. weitere Geräte von den Vorständen, die diese länger nicht genutzt haben. (Siehe Zeile 1 und Zeile 17)

Diese Geräte dann lieber rausnehmen und ggfs. Parallel abklären.

![Exported image](Exported%20image%2020250905165904-2.png)  
13. Wenn die Liste soweit passt, dann alles markieren, oben links auf Organize klicken und dann Export everything to Excel
![Exported image](Exported%20image%2020250905165909-3.png)  
16. Dann einen passenden Speicherort auswählen. Am besten dort, wo auch das Powershell Skript zum Deaktivieren liegt. Das ist Stand August 2025 noch der Server VSBES-ADM04 unter C:\scripts\Baramundi
![Exported image](Exported%20image%2020250905165910-4.png)  
19. Dann auf den ADM04 wechseln und die Excel öffnen um die ersten 6 Zeilen und das Logo heraus zu löschen und danach die Datei als .CSV abzuspeichern.
![Exported image](Exported%20image%2020250905165911-5.png)  
22. Am Besten die bestehende CSV überschreiben, damit im Skript nachher nichts angepasst werden muss.
![Exported image](Exported%20image%2020250905165912-6.png)  
25. Zum Schluss kann das Skript Baramundi_Deactivate in dem Pfad C:\scripts\Baramundi gestartet werden.

Das Skript kann keine Geräte verschieben, die in der "ADMIN" OU liegen und erweiterte Rechte benötigen. Die müssen manuell mit Unterstützung der Infra gemacht werden.
 28. Nachdem das Skript durch gelaufen ist, müssen die Clients im baramundi noch gelöscht werden.

Hierfür wieder zurück ins baramundi und die markierten Geräte der Gruppe mit "Delete" löschen.

![Exported image](Exported%20image%2020250905165914-7.png)  
32. Zum Schluss noch die erstellte Static Group wieder löschen.