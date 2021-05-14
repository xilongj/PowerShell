### Getting Help and Finding Commands
#### Get-Help Get-Service -Examples
```html
PS C:\WINDOWS\system32> Get-Help Get-Service -Examples    
```
#### Get-Help Get-Service -Detailed
```html
PS C:\WINDOWS\system32> Get-Help Get-Service -Detailed
```
#### Get-Help Get-Service - Full
```html
PS C:\WINDOWS\system32> Get-Help Get-Service -Full
```
#### Get-Help Get-Service -Online
```html
PS C:\WINDOWS\system32> Get-Help Get-Service -Online
```
#### Get-Help Get-Service -ShowWindow
```html
PS C:\WINDOWS\system32> Get-Help 'Get-Event' -ShowWindow
```
#### Measure-Object
```html
PS C:\WINDOWS\system32> Get-Verb | Measure-Object    

Count    : 98
Average  :
Sum      :
Maximum  :
Minimum  :
Property :



PS C:\WINDOWS\system32> Get-Command | Measure-Object 

Count    : 1585
Average  :
Sum      :
Maximum  :
Minimum  :
Property :
```
#### Get-Help Stop-Service -Examples
```html
PS C:\WINDOWS\system32> Get-Help *Service*                                                                                              
Name                              Category  Module                    Synopsis                                                          
Resume-Service                    Cmdlet    Microsoft.PowerShell.M... Resumes one or more suspended (paused) services.
Set-Service                       Cmdlet    Microsoft.PowerShell.M... Starts, stops, and suspends a service, and changes its properties.
Start-Service                     Cmdlet    Microsoft.PowerShell.M... Starts one or more stopped services.
Stop-Service                      Cmdlet    Microsoft.PowerShell.M... Stops one or more running services.
Suspend-Service                   Cmdlet    Microsoft.PowerShell.M... Suspends (pauses) one or more running services.
Get-NetFirewallServiceFilter      Function  NetSecurity               ...
Set-NetFirewallServiceFilter      Function  NetSecurity               ...

PS C:\WINDOWS\system32> Get-Help Stop-Service -Examples
```
#### Get-Help *Process*
```html
PS C:\WINDOWS\system32> Get-Help *Process*                                                                                                           
Name                              Category  Module                    Synopsis
----                              --------  ------                    --------
Enter-PSHostProcess               Cmdlet    Microsoft.PowerShell.Core Connects to and enters into an interactive session with a local process.
Exit-PSHostProcess                Cmdlet    Microsoft.PowerShell.Core Closes an interactive session with a local process.
Get-PSHostProcessInfo             Cmdlet    Microsoft.PowerShell.Core Gets process information about the PowerShell host.
Debug-Process                     Cmdlet    Microsoft.PowerShell.M... Debugs one or more processes running on the local computer.
Get-Process                       Cmdlet    Microsoft.PowerShell.M... Gets the processes that are running on the local computer or a remote computer.
Start-Process                     Cmdlet    Microsoft.PowerShell.M... Starts one or more processes on the local computer.
Stop-Process                      Cmdlet    Microsoft.PowerShell.M... Stops one or more running processes.
Wait-Process                      Cmdlet    Microsoft.PowerShell.M... Waits for the processes to be stopped before accepting more input.
Get-AppvVirtualProcess            Function  AppvClient                ...
Start-AppvVirtualProcess          Function  AppvClient                ...
ConvertTo-ProcessMitigationPolicy Cmdlet    ProcessMitigations        ConvertTo-ProcessMitigationPolicy...
Get-ProcessMitigation             Cmdlet    ProcessMitigations        Get-ProcessMitigation...
Set-ProcessMitigation             Cmdlet    ProcessMitigations        Set-ProcessMitigation...

PS C:\WINDOWS\system32> Get-Help Start-Process -Examples
```
#### Get-Help \*log*
```html
PS C:\WINDOWS\system32> Get-Help *log*
PS C:\WINDOWS\system32> Get-Help Clear-EventLog -Examples
```
#### Get-Command -Name *a
```html
PS C:\WINDOWS\system32> Get-Command -Name *a                                                              
CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Alias           blsmba ->                                          2.0.0.0    SmbShare
Alias           cvpa -> Convert-Path
Alias           grsmba ->                                          2.0.0.0    SmbShare
Alias           gsmba ->                                           2.0.0.0    SmbShare
Alias           rksmba ->                                          2.0.0.0    SmbShare
Alias           rvpa -> Resolve-Path
Alias           ulsmba ->                                          2.0.0.0    SmbShare
Function        Disable-NetAdapterRdma                             2.0.0.0    NetAdapter
Function        Enable-NetAdapterRdma                              2.0.0.0    NetAdapter
Function        Get-NetAdapterRdma                                 2.0.0.0    NetAdapter
Function        Get-NetIPsecMainModeSA                             2.0.0.0    NetSecurity
Function        Get-NetIPsecQuickModeSA                            2.0.0.0    NetSecurity
Function        Get-NetworkSwitchGlobalData                        1.0.0.0    NetworkSwitchManager
Function        Get-StorageEnclosureVendorData                     2.0.0.0    Storage
Function        Remove-NetIPsecMainModeSA                          2.0.0.0    NetSecurity
Function        Remove-NetIPsecQuickModeSA                         2.0.0.0    NetSecurity
Function        Set-NetAdapterRdma                                 2.0.0.0    NetAdapter
Cmdlet          ConvertFrom-StringData                             3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Export-FormatData                                  3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-FormatData                                     3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-PfxData                                        1.0.0.0    PKI
Cmdlet          Get-TypeData                                       3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Import-LocalizedData                               3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Remove-TypeData                                    3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Update-FormatData                                  3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Update-TypeData                                    3.1.0.0    Microsoft.PowerShell.Utility
```
#### Get-Help Get-EventLog -ShowWindow
```html
PS C:\WINDOWS\system32> Get-Help Get-EventLog -ShowWindow  
PS C:\WINDOWS\system32> Get-EventLog -List          
  Max(K) Retain OverflowAction        Entries Log
  ------ ------ --------------        ------- ---
  20,480      0 OverwriteAsNeeded         707 Application
  20,480      0 OverwriteAsNeeded           0 HardwareEvents
     512      7 OverwriteOlder              0 Internet Explorer
  20,480      0 OverwriteAsNeeded           0 Key Management Service
  20,480      0 OverwriteAsNeeded       6,337 Security
  20,480      0 OverwriteAsNeeded         611 System
  15,360      0 OverwriteAsNeeded         100 Windows PowerShell

PS C:\WINDOWS\system32> Get-EventLog Application  
```
#### Get-Content
```html
PS C:\WINDOWS\system32> Get-Content -Path C:\Users\xilongj\Documents\desktop.ini

[.ShellClassInfo]
LocalizedResourceName=@%SystemRoot%\system32\shell32.dll,-21770
IconResource=%SystemRoot%\system32\imageres.dll,-112
IconFile=%SystemRoot%\system32\shell32.dll
IconIndex=-235
```
#### Get-Help Clear-History
```html
PS C:\WINDOWS\system32> Get-Help Clear-History -Examples
Clear-History -Id 3, 5
```
#### Get-Alias -Name \*M
```html
PS C:\WINDOWS\system32> Get-Alias -Name *M

CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Alias           gcm -> Get-Command                                                  
Alias           gm -> Get-Member                                                    
Alias           icm -> Invoke-Command                                               
Alias           irm -> Invoke-RestMethod                                            
Alias           rm -> Remove-Item                                                   
Alias           shcm -> Show-Command                                                
Alias           trcm -> Trace-Command
```
#### Get-Service BITS
```html
PS C:\WINDOWS\system32> Get-Service BITS

Status   Name               DisplayName                           
------   ----               -----------                           
Stopped  BITS               Background Intelligent Transfer Ser...



PS C:\WINDOWS\system32> Start-Service BITS -PassThru

Status   Name               DisplayName                           
------   ----               -----------                           
Running  BITS               Background Intelligent Transfer Ser...
```
