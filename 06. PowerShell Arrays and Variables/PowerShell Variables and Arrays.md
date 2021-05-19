## PowerShell Variables
### Set Variables
```html
PS C:\WINDOWS\system32> Get-WmiObject -Class Win32_Bios

SMBIOSBIOSVersion : 6.00
Manufacturer      : Phoenix Technologies LTD
Name              : PhoenixBIOS 4.0 Release 6.0
SerialNumber      : VMware-56 4d 9d 62 a8 76 b3 f0-00 50 b6 1d d7 66 2d c5
Version           : INTEL  - 6040000

PS C:\WINDOWS\system32> (Get-WmiObject -Class Win32_Bios).SMBIOSBIOSVERSION
6.00
PS C:\WINDOWS\system32> $BIOS_VER = (Get-WmiObject -Class Win32_Bios).SMBIOSBIOSVERSION
PS C:\WINDOWS\system32> echo $BIOS_VER
6.00
```
### Setup username
```html
PS C:\WINDOWS\system32> $username = Read-Host -Prompt "Please enter your username"                                                                                                                                 Please enter your username: xilongj
PS C:\WINDOWS\system32> echo $username
xilongj                                                                                                                                                                         xilongj
PS C:\WINDOWS\system32>
```
```html
PS C:\WINDOWS\system32> $username = Read-Host -Prompt "Please enter your username"                                                                                                                                 
Please enter your username: xilongj
PS C:\WINDOWS\system32> echo $username                                                                                                                                                                             
xilongj
PS C:\WINDOWS\system32> $username > namelst.txt                                                                                                                                                                    
PS C:\WINDOWS\system32> Get-Content namelst.txt                                                                                                                                                                    
xilongj
PS C:\WINDOWS\system32> 
```
```html
# mission.ps1
$UserInput = Read-Host -Prompt "Please tell our mission"
Set-Content -Value $UserInput -Path C:\Users\xilongj\Desktop\mission.txt
```
### PowerShell Arrays
```html
PS C:\WINDOWS\system32> $MyArray = "Cheese"
PS C:\WINDOWS\system32> $MyArray
Cheese

PS C:\WINDOWS\system32> $MyArray = @("Cheese")
PS C:\WINDOWS\system32> $MyArray[0]
Cheese
```
```html
PS C:\WINDOWS\system32> $MyArray = @("Cheese", "Apple", "Orange")
PS C:\WINDOWS\system32> $MyArray
Cheese
Apple
Orange
PS C:\WINDOWS\system32> $MyArray[0]
Cheese
PS C:\WINDOWS\system32> $MyArray[1]
Apple
PS C:\WINDOWS\system32> $MyArray[2]
Orange
```
```html
PS C:\WINDOWS\system32> $MyArray = @()
PS C:\WINDOWS\system32> $MyArray

PS C:\WINDOWS\system32> $MyArray += "Apple"
PS C:\WINDOWS\system32> $MyArray
Apple

PS C:\WINDOWS\system32> $MyArray += @("Peppers", "Olives")
PS C:\WINDOWS\system32> $MyArray
Apple
Peppers
Olives
```
```html
PS C:\WINDOWS\system32> $Alphabet = @("C", "D", "E", "A", "B")

PS C:\WINDOWS\system32> $Alphabet
C
D
E
A
B

PS C:\WINDOWS\system32> $Alphabet | Sort-Object
A
B
C
D
E

PS C:\WINDOWS\system32> $Alphabet | Sort-Object -Descending
E
D
C
B
A
```
```html
PS C:\WINDOWS\system32> $Alphabet = @("C", "D", "E", "A", "B")
PS C:\WINDOWS\system32> $Alphabet = $Alphabet | Sort

PS C:\WINDOWS\system32> $Alphabet
A
B
C
D
E
```
```html
PS C:\WINDOWS\system32> $MyArray = @("Apple", "Orange", "Olives")

PS C:\WINDOWS\system32> $MyArray
Apple
Orange
Olives

PS C:\WINDOWS\system32> $MyArray | where {$_ -ne "Orange"}
Apple
Olives
```
```html
PS C:\WINDOWS\system32> $MyArray = @("Apple", "Orange", "Olives")
PS C:\WINDOWS\system32> $MyArray = $MyArray | where {$_ -ne "Olives"}

PS C:\WINDOWS\system32> $MyArray
Apple
Orange
PS C:\WINDOWS\system32> $MyArray += "Peppers"

PS C:\WINDOWS\system32> $MyArray
Apple
Orange
Peppers
```
```html
PS C:\WINDOWS\system32> $MyArray = @("Apple", "Orange", "Olives")

PS C:\WINDOWS\system32> $MyArray
Apple
Orange
Olives

PS C:\WINDOWS\system32> $MyArray = $MyArray | where {$_ -ne $MyArray[1]}

PS C:\WINDOWS\system32> $MyArray
Apple
Olives
```
```html
PS C:\WINDOWS\system32> $MyArray
Apple
Olives

PS C:\WINDOWS\system32> $MyArray = $null

PS C:\WINDOWS\system32> $MyArray
```
