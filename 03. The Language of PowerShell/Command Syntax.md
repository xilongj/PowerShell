### PowerShell Commands Syntax
#### Syntax for Get-EventLog
```html
Syntax for Get-EventLog
# Command Structure
    Verb-Noun -Parameter1 <arg1> -Parameter2 <arg2, arg3>

# Example
    Get-EventLog -LogName Application -InstanceId 0,1

Syntax
    Get-EventLog [-LogName] <System.String> [[-InstanceId] <System.Int64[]>] 
        [-After <System.DateTime>] [-AsBaseObject ] 
        [-Before <System.DateTime>] [-ComputerName <System.String[]>] 
        [-EntryType <System.String[]>] [-Index <System.Int32[]>] 
        [-Message <System.String>] [-Newest <System.Int32>] [-Source <System.String[]>] 
        [-UserName <System.String[]>] [<CommonParameters>]

    Get-EventLog [-AsString ] [-ComputerName <System.String[]>] [-List ] [<CommonParameters>]
```
```html
PS C:\WINDOWS\system32> Get-EventLog -LogName Application -InstanceId 100, 5615

   Index Time          EntryType   Source                 InstanceID Message                                                         
   ----- ----          ---------   ------                 ---------- -------                                                         
     657 May 08 11:57  Information Microsoft-Windows...         5615 Windows Management Instrumentation Service started sucessfully  
     602 May 08 11:54  Information Microsoft-Windows...         5615 Windows Management Instrumentation Service started sucessfully  
     457 May 08 11:12  Information Microsoft-Windows...         5615 Windows Management Instrumentation Service started sucessfully  
      13 May 08 10:54  Information Microsoft-Windows...         5615 Windows Management Instrumentation Service started sucessfully  
      12 May 08 10:54  Information WLMS                          100 The license period for this installation of Windows has expired.
       4 May 09 01:52  Information Microsoft-Windows...         5615 Windows Management Instrumentation Service started sucessfully  
       2 May 09 01:52  Information WLMS                          100 The license period for this installation of Windows has expired.
```
```html
PS C:\WINDOWS\system32> Get-EventLog Application -EntryType Warning,Error -Newest 5

   Index Time          EntryType   Source                 InstanceID Message                                                                                         
   ----- ----          ---------   ------                 ---------- -------                                                                                         
     593 May 14 10:01  Error       Microsoft-Windows...         1020 The required buffer size is greater than the buffer size passed to the Collect function of th...
     396 May 12 17:26  Error       Application Hang             1002 The program MicrosoftEdge.exe version 11.0.18362.1 stopped interacting with Windows and was c...
     394 May 12 17:25  Warning     Microsoft-Windows...           63 A provider, PolicyAgentInstanceProvider, has been registered in the Windows Management Instru...
     393 May 12 17:25  Warning     Microsoft-Windows...           63 A provider, PolicyAgentInstanceProvider, has been registered in the Windows Management Instru...
     392 May 12 17:25  Warning     Microsoft-Windows...           63 A provider, PolicyAgentInstanceProvider, has been registered in the Windows Management Instru...
```
#### Syntax for Get-Service
```html
# Syntax for Get-Service
Syntax
    Get-Service [-ComputerName <System.String[]>] [-DependentServices ] -DisplayName <System.String[]> 
    [-Exclude <System.String[]>] [-Include <System.String[]>] [-RequiredServices ] [<CommonParameters>]

    Get-Service [-ComputerName <System.String[]>] [-DependentServices ] [-Exclude <System.String[]>] 
    [-Include <System.String[]>] [-InputObject <System.ServiceProcess.ServiceController[]>] 
    [-RequiredServices ] [<CommonParameters>]

    Get-Service [[-Name] <System.String[]>] [-ComputerName <System.String[]>] [-DependentServices ] 
    [-Exclude <System.String[]>] [-Include <System.String[]>] [-RequiredServices ] [<CommonParameters>]
```
```html
PS C:\WINDOWS\system32> Get-Service -DisplayName 'ActiveX Installer (AxInstSV)'

Status   Name               DisplayName                           
------   ----               -----------                           
Stopped  AxInstSV           ActiveX Installer (AxInstSV)          
```
