Registry Lookup  
You can also find the product code by perusing the registry from this base key: 
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall`

Press F3 key and search for your product name. If it's a 32-bit installer on a 64-bit machine, it might be under the following key: 
`HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\Uninstall`

The following registry keys are the common locations in which search and find the GUIDs of MSI packages:  
`HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall`
`HKLM\SOFTWARE\WOW6432Node\Microsoft\Windows\CurrentVersion\Uninstall`
`HKCU\Software\Microsoft\Windows\CurrentVersion\Uninstall`
 \> Aus \<[https://www.heelpbook.net/2019/powershell-check-and-find-the-product-guid-of-an-installed-msi-setup/](https://www.heelpbook.net/2019/powershell-check-and-find-the-product-guid-of-an-installed-msi-setup/)\>