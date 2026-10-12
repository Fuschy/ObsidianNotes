Fehler:  
PS C:\Windows\system32\> `Install-Module -Name ExchangeOnlineManagement`  
PackageManagement\Install-Package : No match was found for the specified search criteria and module name 'ExchangeOnlineManagement'. Try Get-PSRepository to see all available registered module repositories.  
At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21  
... $null = PackageManagement\Install-Package @PSBoundParameters  

CategoryInfo : ObjectNotFound: (Microsoft.Power....InstallPackage:InstallPackage) Install-Package, Exception  
FullyQualifiedErrorId : NoMatchFoundForCriteria,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
 
Lösung:  
`Get-PSRepository` ausführen um zu prüfen dass das erreichbar ist.  
Wenn nein dann: [[Get-PSRepository Fehler]]
Wenn ja dann: ????