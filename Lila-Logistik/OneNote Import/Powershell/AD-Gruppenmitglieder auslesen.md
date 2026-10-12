**PowerShell als Admin starten**
 
**Mit diesem Befehl werden die Mitglieder der Gruppe direkt angezeigt:**
`Get-ADGroupMember "GruppenName" | Select-Object Name`

![Computergenerierter Alternativtext Administrator W...](Exported%20image%2020250905170900-0.png)
 **Mit diesem Befehl werden die Mitglieder der Gruppe nach `C:\temp\*.txt` exportiert:** 
  
`Get-ADGroupMember "GruppenName" | Select-Object Name \> C:\temp\*.txt`