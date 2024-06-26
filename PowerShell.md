### PowerShell for SysAdmins

#### 1. Install PowerShell Core
```powershell
https://github.com/PowerShell/PowerShell
```

#### 2. check PowerShell version
```powershell
PS C:\Program Files\PowerShell\7> $PSVersionTable

Name                           Value
----                           -----
PSVersion                      7.4.3
PSEdition                      Core
GitCommitId                    7.4.3
OS                             Microsoft Windows 10.0.22631
Platform                       Win32NT
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0…}
PSRemotingProtocolVersion      2.3
SerializationVersion           1.1.0.1
WSManStackVersion              3.0
```

#### 3. Commands Work in PowerShell
```powershell
PS C:\Program Files\PowerShell\7> Get-Command cat

CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Alias           cat -> Get-Content

PS C:\Program Files\PowerShell\7> Get-Command -Verb Get -Noun Service

CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Cmdlet          Get-Service                                        7.0.0.0    Microsoft.PowerShell.Management
```
```powershell
PS C:\Program Files\PowerShell\7> Get-Service PanGPS

Status   Name               DisplayName
------   ----               -----------
Running  PanGPS             PanGPS

PS C:\Program Files\PowerShell\7> Restart-Service PanGPS
```
```powershell
PS C:\Program Files\PowerShell\7> Get-Service -Name wuauserv

Status   Name               DisplayName
------   ----               -----------
Running  wuauserv           Windows Update
```
```powershell
PS C:\Program Files\PowerShell\7> Get-History
```

#### 4. GETTING HELP
```powershell
PS C:\Program Files\PowerShell\7> Get-Help -Name Get-Service

NAME
    Get-Service

SYNTAX
    Get-Service [[-Name] <string[]>] [-DependentServices] [-RequiredServices] [-Include <string[]>] [-Exclude <string[]>] [<CommonParameters>]

    Get-Service -DisplayName <string[]> [-DependentServices] [-RequiredServices] [-Include <string[]>] [-Exclude <string[]>] [<CommonParameters>]

    Get-Service [-DependentServices] [-RequiredServices] [-Include <string[]>] [-Exclude <string[]>] [-InputObject <ServiceController[]>] [<CommonParameters>]


ALIASES
    gsv


REMARKS
    Get-Help cannot find the Help files for this cmdlet on this computer. It is displaying only partial help.
        -- To download and install Help files for the module that includes this cmdlet, use Update-Help.
        -- To view the Help topic for this cmdlet online, type: "Get-Help Get-Service -Online" or
           go to https://go.microsoft.com/fwlink/?LinkID=2096496.
```

```powershell
PS C:\Program Files\PowerShell\7> Get-Help about_Core_Commands
The following is a list of the PowerShell cmdlets that are designed for use
with providers:

ChildItem cmdlets

-   Get-ChildItem

Content cmdlets

-   Add-Content
-   Clear-Content
-   Get-Content
-   Set-Content

Item cmdlets

-   Clear-Item
-   Copy-Item
-   Get-Item
-   Invoke-Item
-   Move-Item
-   New-Item
-   Remove-Item
-   Rename-Item
-   Set-Item

ItemProperty cmdlets

-   Clear-ItemProperty
-   Copy-ItemProperty
-   Get-ItemProperty
-   Move-ItemProperty
-   New-ItemProperty
-   Remove-ItemProperty
-   Rename-ItemProperty
-   Set-ItemProperty

Location cmdlets

-   Get-Location
-   Pop-Location
-   Push-Location
-   Set-Location

Path cmdlets

-   Join-Path
-   Convert-Path
-   Split-Path
-   Resolve-Path
-   Test-Path

PSDrive cmdlets

-   Get-PSDrive
-   New-PSDrive
-   Remove-PSDrive

PSProvider cmdlets

-   Get-PSProvider
```

#### 5. Variable
```powershell
PS C:\Users\xilongj> Set-Variable -Name filePath -Value C:\Users\xilongj\Desktop\PowerShell.md
PS C:\Users\xilongj> Get-Variable -Name filePath

Name                           Value
----                           -----
filePath                       C:\Users\xilongj\Desktop\PowerShell.md

PS C:\Users\xilongj> $filePath
C:\Users\xilongj\Desktop\PowerShell.md
```
```powershell
PS C:\Users\xilongj> $MaximumHistoryCount
4096
PS C:\Users\xilongj> $MaximumHistoryCount = 200
PS C:\Users\xilongj> $MaximumHistoryCount
200
PS C:\Users\xilongj> $PSEdition
Core
```
```powershell
PS C:\Users\xilongj> Set-Variable -Name color -Value green -Option Constant
PS C:\Users\xilongj> $color
green
```
```powershell
#lastexitcode
PS C:\Users\xilongj> $lastexitcode
0
PS C:\Users\xilongj> PING.EXE xbj-xilongj-l2
Ping request could not find host xbj-xilongj-l2. Please check the name and try again.
PS C:\Users\xilongj> $lastexitcode
1
```

#### 6. Objects
```powershell
PS C:\Users\xilongj> $uname = 'xilongj'
PS C:\Users\xilongj> Select-Object -InputObject $uname -Property *

Length
------
     7

PS C:\Users\xilongj> $uname.Length
7
```
```powershell
PS C:\Users\xilongj> Get-Member -InputObject $uname

   TypeName: System.String

Name                 MemberType            Definition
----                 ----------            ----------
Clone                Method                System.Object Clone(), System.Object ICloneable.Clone()
.
.
.
PS C:\Users\xilongj> Get-Member -InputObject $uname -Name Remove

   TypeName: System.String

Name   MemberType Definition
----   ---------- ----------
Remove Method     string Remove(int startIndex, int count), string Remove(int startIndex)

#example
PS C:\Users\xilongj> $uname
xilongj
PS C:\Users\xilongj>
PS C:\Users\xilongj> $uname.Remove(0,2)
longj
```

#### 7. Strings
```powershell
PS C:\Users\xilongj> $aboutSkills = 'PowerShell, Bash, Python, C'
PS C:\Users\xilongj> $language = 'Python'
PS C:\Users\xilongj> $aboutSkills = "PowerShell, Bash, $language, C"
PS C:\Users\xilongj> $aboutSkills
PowerShell, Bash, Python, C

PS C:\Users\xilongj> $language = 'Java'
PS C:\Users\xilongj> $aboutSkills = "PowerShell, Bash, $language, C"
PS C:\Users\xilongj> $aboutSkills
PowerShell, Bash, Java, C

PS C:\Users\xilongj> 'PowerShell, Bash, {0}, C' -f $language
PowerShell, Bash, Java, C
```

#### 8. Boolean
```powershell
PS C:\Users\xilongj> $true
True
PS C:\Users\xilongj> $false
False

PS C:\Users\xilongj> $isEnabled = $true
PS C:\Users\xilongj> $isEnabled
True

PS C:\Users\xilongj> $isEnabled = $false
PS C:\Users\xilongj> $isEnabled
False
```

#### 9. Data Types - Numbers
```powershell
PS C:\Users\xilongj> $num = 2024
PS C:\Users\xilongj> $num.GetType().name
Int32

PS C:\Users\xilongj> $uname = 'xilongj'
PS C:\Users\xilongj> $uname.GetType().name
String

PS C:\Users\xilongj> $num = 2024
PS C:\Users\xilongj> $num = [float]$num
PS C:\Users\xilongj> $num.GetType().name
Single
PS C:\Users\xilongj> $num = 6.26
PS C:\Users\xilongj> $num.GetType().name
Double

PS C:\Users\xilongj> $one = '1'
PS C:\Users\xilongj> $two = 2
PS C:\Users\xilongj> $one + $two
12
```

#### 10. Data Types - ScriptBlocks
```powershell
PS C:\Users\xilongj> Test-Path "C:\Program Files\Avecto\Privilege Guard Client\PGProgramsUtil.exe"
True
PS C:\Users\xilongj> $myScriptBlock = { Test-Path "C:\Program Files\Avecto\Privilege Guard Client\PGProgramsUtil.exe" }
PS C:\Users\xilongj> $myScriptBlock
 Test-Path "C:\Program Files\Avecto\Privilege Guard Client\PGProgramsUtil.exe"
PS C:\Users\xilongj> & $myScriptBlock
True
```

#### 11. Data Types - Hashtables and Arrays
```powershell
PS C:\Users\xilongj> $colorPicker = @('blue', 'white', 'yellow', 'black')
PS C:\Users\xilongj> $colorPicker
blue
white
yellow
black

PS C:\Users\xilongj> $colorPicker[0]
blue
PS C:\Users\xilongj> $colorPicker[2]
yellow

PS C:\Users\xilongj> $colorPicker[1..3]
white
yellow
black
```
```powershell
PS C:\Users\xilongj> $colorPicker = @('blue', 'white', 'yellow', 'black')
PS C:\Users\xilongj> $colorPicker[0] = 'pink'
PS C:\Users\xilongj> $colorPicker
pink
white
yellow
black

PS C:\Users\xilongj> $colorPicker = $colorPicker + 'orange'
PS C:\Users\xilongj> $colorPicker
pink
white
yellow
black
orange
```
```powershell
PS C:\Users\xilongj> $colorPicker += 'brown'
PS C:\Users\xilongj> $colorPicker
pink
white
yellow
black
orange
brown
```
```powershell
PS C:\Users\xilongj> $colorPicker
pink
white
yellow
black
orange
brown

PS C:\Users\xilongj> $colorPicker += @('pink','cyan')
PS C:\Users\xilongj> $colorPicker
pink
white
yellow
black
orange
brown
pink
cyan
```
```powershell
PS C:\Users\xilongj> $colorPicker = [System.Collections.Generic.List[string]]@('blue','white','yellow','black')
PS C:\Users\xilongj> $colorPicker
blue
white
yellow
black
PS C:\Users\xilongj> $colorPicker.Add('gray'); $colorPicker
blue
white
yellow
black
gray

PS C:\Users\xilongj> $colorPicker.Remove('gray') ; $colorPicker
True
blue
white
yellow
black
```
```powershell
PS C:\Users\xilongj> $users = @{ xilongj = 'Xilong Jin'; joeb = 'Joe Biden'; satyan = 'Satya Nadella' }
PS C:\Users\xilongj> $users['joeb']
Joe Biden
PS C:\Users\xilongj> $users.satyan
Satya Nadella
PS C:\Users\xilongj> $users.Keys
satyan
xilongj
joeb
PS C:\Users\xilongj> $users.Values
Satya Nadella
Xilong Jin
Joe Biden
```
```powershell
PS C:\Users\xilongj> $userInfo = @{ joeb = 'Joe Biden'; satyan = 'Satya Nadella'; kamalah = 'Kamala Devi. Harris' }
PS C:\Users\xilongj> $userInfo.Keys
kamalah
satyan
joeb
PS C:\Users\xilongj> $userInfo.Values
Kamala Devi. Harris
Satya Nadella
Joe Biden
PS C:\Users\xilongj> Select-Object -InputObject $userInfo -Property *

kamalah             satyan        joeb
-------             ------        ----
Kamala Devi. Harris Satya Nadella Joe Biden

PS C:\Users\xilongj> $userInfo['xilongj'] = 'Xilong Jin'
PS C:\Users\xilongj> Select-Object -InputObject $userInfo -Property *

kamalah             satyan        xilongj    joeb
-------             ------        -------    ----
Kamala Devi. Harris Satya Nadella Xilong Jin Joe Biden

PS C:\Users\xilongj> $userInfo

Name                           Value
----                           -----
kamalah                        Kamala Devi. Harris
satyan                         Satya Nadella
xilongj                        Xilong Jin
joeb                           Joe Biden

PS C:\Users\xilongj> $userInfo.ContainsKey('p1_xilongj')
False
PS C:\Users\xilongj> $userInfo.ContainsKey('xilongj')
True
```

#### 12. Pipeline
```powershell
PS C:\Users\xilongj> $serviceName = 'wuauserv'
PS C:\Users\xilongj> Get-Service -Name $serviceName

Status   Name               DisplayName
------   ----               -----------
Running  wuauserv           Windows Update

PS C:\Users\xilongj> Stop-Service -Name $serviceName
PS C:\Users\xilongj> Get-Service -Name $serviceName

Status   Name               DisplayName
------   ----               -----------
Stopped  wuauserv           Windows Update

PS C:\Users\xilongj> Get-Service -Name $serviceName | Start-Service
PS C:\Users\xilongj> Get-Service -Name $serviceName

Status   Name               DisplayName
------   ----               -----------
Running  wuauserv           Windows Update
```
```powershell
PS C:\Users\xilongj\Desktop> Get-Content -Path .\services.txt
WinRM
WSearch
Winmgmt
PS C:\Users\xilongj\Desktop> Get-Content -Path .\services.txt | Get-Service

Status   Name               DisplayName
------   ----               -----------
Running  WinRM              Windows Remote Management (WS-Managem…
Running  WSearch            Windows Search
Running  Winmgmt            Windows Management Instrumentation
```
```powershell
PS C:\Users\xilongj\Desktop> Get-Help -Name Stop-Service -Full

NAME
    Stop-Service

SYNOPSIS
    Stops one or more running services.
```
```powershell
PS C:\Users\xilongj\Desktop> Get-ExecutionPolicy
RemoteSigned
PS C:\Users\xilongj\Desktop> Set-ExecutionPolicy -ExecutionPolicy AllSigned
PS C:\Users\xilongj\Desktop> Get-ExecutionPolicy
AllSigned

PS C:\Users\xilongj\Desktop> Set-ExecutionPolicy -ExecutionPolicy Unrestricted
PS C:\Users\xilongj\Desktop> Get-ExecutionPolicy
Unrestricted
PS C:\Users\xilongj\Desktop>
```

#### 13. Setup VSCode
```powershell
Install PowerShell extension
```