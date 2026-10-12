Zuerst werden Ressourcen Account benötigt, welche dann die Rufnummer tragen.  
Hierfür geht man ins Teams Admin Center -\> Voice -\> Resource accounts -\> Add

![Exported image](Exported%20image%2020250905170820-0.png)  

Dort gibt man dann einen Usernamen an und wählt als type die call queue aus.

![Exported image](Exported%20image%2020250905170822-1.png)  

Nach der Anlage muss dem Account die Lizenz "Microsoft Teams Phone Resource Account" zugewiesen werden.

![Exported image](Exported%20image%2020250905170823-2.png)  

Danach muss eine Telefonnummer für den Ressourcen Account vergeben werden. Dies geschieht über folgenden Powershell-Befehl:

1. Connect-Microsoft Teams
2. Set-CsPhoneNumberAssignment -Identity RessourceAccount@lila-logistik.com -PhoneNumber +497143810XXXXX -PhoneNumberType DirectRouting