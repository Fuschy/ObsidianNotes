SKUs für Lizenzen:
 ![[sku.csv]]
![[UserList_Microsoft_365_F3_14.3.2025_13_29_03.csv]]

![[UserList_Microsoft_365_E3_14.3.2025_13_28_51 1.csv]]

`$e3Sku = Get-MgSubscribedSku -All | Where SkuPartNumber -eq 'SPE_E3'`  
`Set-MgUserLicense -UserId "Roberto.Abbate@lila-logistik.com" -RemoveLicenses @($e3Sku.SkuId) -AddLicenses @{}`
   

`Set-MgUserLicense -UserId "\<Account\>" -RemoveLicenses @("\<AccountSkuId1\>") -AddLicenses @{}`
 
Remove:  
[Remove Microsoft 365 licenses from user accounts with PowerShell - Microsoft 365 Enterprise | Microsoft Learn](https://learn.microsoft.com/en-us/microsoft-365/enterprise/remove-licenses-from-user-accounts-with-microsoft-365-powershell?view=o365-worldwide)
 
E3:  
SKUID: 05e9a617-0261-4cee-bb44-138d3ef5d965  
SKU Part Number: SPE_E3
F3:  
SKUID: 66b55226-6b4f-492c-910c-a3b7a3c9d993  
SKU Part Number: SPE_F1