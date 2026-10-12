1. Baramundi Management Suite Version aus dem _Forum_ herunterladen
2. Snapshot vom Server und Datenbankserver **SQL-BES-V05** von der Infra erstellen lassen.
3. "**Baramundi Server**" Dienst stoppen
4. **Management Suite Setup** Starten
5. ![[Exported image 20250905165919-0.png]]
6. **Standard**
7. **Standardverzeichnis** lassen
8. ![[Exported image 20250905165924-1.png]]
9. ![252n5u2W 8 punueeq u m35 s](Exported%20image%2020250905165925-2.png)
10. Nach Beendigung wird die Datenbank geupdated.
11. **Existing Database**, durchklicken
![baramundi Management Suite Database Manager This w...](Exported%20image%2020250905165926-3.png)
12. **Server Neustart ohne Windows Updates**
13. **Baramundi Management Center** starten, Server in "**operational Mode"** setzen
![Exported image](Exported%20image%2020250905165927-4.png)  
14. **MSW: management Cente**r Freigeben
    1. Unter Managed Software \< baramundi Management Suite \< Management Center
        1. Die letzten beiden Releases können auf released gesetzt werden, die anderen sollten nicht released sein. Nach dem Update das älteste aus dem release nehmen
15. **PXE Relay** Freigeben
    1. Unter Managed Software \< baramundi Management Suite \< PXE-Relay
        1. Die letzten beiden Releases können auf released gesetzt werden, die anderen sollten nicht released sein. Nach dem Update das älteste aus dem release nehmen
16. **baraDip** Freigeben
    1. Unter Managed Software \< baramundi Management Suite \< baraDIP
        1. Die letzten beiden Releases können auf released gesetzt werden, die anderen sollten nicht released sein. Nach dem Update das älteste aus dem release nehmen
      
    
17. **Automation Studio** Freigeben
    1. Unter Managed Software \< baramundi Management Suite \< Automation Studio
        1. Die letzten beiden Releases können auf released gesetzt werden, die anderen sollten nicht released sein. Nach dem Update das älteste aus dem release nehmen
          
        
18. Baramundi Management Agent in **d:\dip\bms\client\setup** austauschen. Liegt in der ISO
19. **Dips** syncen lassen
20. **Fortschritt** kontrollieren
21. DIPS Neustarten
22. Patch Management Center / Patch MSW Job starten, bei User und Server, für **BMC Update**
23. Agent aktualisiert sich von selbst
24. Auf allen Dips den Patch: **MSW** laufen lassen, damit sich die Software Komponenten von Baramundi updaten
25. **WinPE** updaten unter Tools \< Boot media wizard
    1. Boot Media Wizard einmal durchlaufen lassen (Den Pfad nach Doku anpassen: [[Treiber ins Image WIN PE (PXE)]])
26. REST MIT DOKU VON BARAMUNDI ABLGEICHEN!
       
==Nach Update, alle Dips neustarten!==
