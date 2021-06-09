## The PowerShell Pipeline
### Get-ChildItem
```html
PS C:\WINDOWS\system32> Get-ChildItem C:\Users\xilongj\Desktop\


    Directory: C:\Users\xilongj\Desktop


Mode                LastWriteTime         Length Name                                                                                                                               
----                -------------         ------ ----                                                                                                                               
d-----        5/14/2021   3:35 PM                NetDom                                                                                                                             



PS C:\WINDOWS\system32> Get-ChildItem C:\Users\xilongj\Desktop\ -Recurse


    Directory: C:\Users\xilongj\Desktop


Mode                LastWriteTime         Length Name                                                                                                                               
----                -------------         ------ ----                                                                                                                               
d-----        5/14/2021   3:35 PM                NetDom                                                                                                                             


    Directory: C:\Users\xilongj\Desktop\NetDom


Mode                LastWriteTime         Length Name                                                                                                                               
----                -------------         ------ ----                                                                                                                               
-a----        5/14/2021  12:40 PM            348 netdom.txt 
```
### Remove-Item
```html
PS C:\WINDOWS\system32> Get-ChildItem C:\Users\xilongj\PycharmProjects\PowerShell -Recurse | Remove-Item -WhatIf
```
```html
PS C:\WINDOWS\system32> Get-ChildItem C:\Users\xilongj\Desktop -Recurse | Remove-Item -Confirm
```
### Out-File
```html
PS C:\WINDOWS\system32> Get-EventLog -LogName Application | Out-File C:\Users\xilongj\Desktop\app.log
```
### Get-Content
```html
PS C:\WINDOWS\system32> Get-Content -Path C:\Users\xilongj\Desktop\app.log
```
### Get-Service 
```html
PS C:\WINDOWS\system32> Get-Service -Name BITS | Stop-Service -PassThru

Status   Name               DisplayName                           
------   ----               -----------                           
Stopped  BITS               Background Intelligent Transfer Ser...
```
### Import-Csv
```html
PS C:\WINDOWS\system32> Import-Csv -Path \\CBSDB01\xilongj\docs\new-alias.csv | Get-Member


   TypeName: System.Management.Automation.PSCustomObject

Name        MemberType   Definition                    
----        ----------   ----------                    
Equals      Method       bool Equals(System.Object obj)
GetHashCode Method       int GetHashCode()             
GetType     Method       type GetType()                
ToString    Method       string ToString()             
Name        NoteProperty string Name=L                 
Value       NoteProperty string Value=EventLog   
```
### New-Alias
```html
PS C:\WINDOWS\system32> Get-Content -Path \\CBSDB01\xilongj\docs\new-alias.csv
Name, Value
L, EventLog
List, Get-ChildItem
P, Ping
W, winver

PS C:\WINDOWS\system32> Import-Csv -Path \\CBSDB01\xilongj\docs\new-alias.csv | New-Alias -Verbose
VERBOSE: Performing the operation "New Alias" on target "Name: L Value: EventLog".
VERBOSE: Performing the operation "New Alias" on target "Name: List Value: Get-ChildItem".
VERBOSE: Performing the operation "New Alias" on target "Name: P Value: Ping".
VERBOSE: Performing the operation "New Alias" on target "Name: W Value: winver".
```
```html
PS C:\WINDOWS\system32> Import-Csv \\CBSDB01\xilongj\docs\all-srv.csv

name svcstatus
---- ---------
Bits Running


PS C:\WINDOWS\system32> Import-Csv \\CBSDB01\xilongj\docs\all-srv.csv | Stop-Service -PassThru

Status   Name               DisplayName
------   ----               -----------
Stopped  Bits               Background Intelligent Transfer Ser...


PS C:\WINDOWS\system32> Get-Service -Name BITS

Status   Name               DisplayName
------   ----               -----------
Stopped  BITS               Background Intelligent Transfer Ser...
```