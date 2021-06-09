## Objects, Properties and Methods
### Kill()
```html
# open notepad app
PS C:\WINDOWS\system32> Get-Process -Name notepad

Handles  NPM(K)    PM(K)      WS(K)     CPU(s)     Id  SI ProcessName                                                                                                
-------  ------    -----      -----     ------     --  -- -----------                                                                                                
    231      14     3132       1140       0.13   7632   1 notepad
```
```html
PS C:\WINDOWS\system32> Get-Process -Name notepad | Get-Member


   TypeName: System.Diagnostics.Process

Name                       MemberType     Definition                                                                                                                 
----                       ----------     ----------                                                                                                                 
Handles                    AliasProperty  Handles = Handlecount                                                                                                      
Name                       AliasProperty  Name = ProcessName                                                                                                         
NPM                        AliasProperty  NPM = NonpagedSystemMemorySize64                                                                                           
PM                         AliasProperty  PM = PagedMemorySize64                                                                                                     
SI                         AliasProperty  SI = SessionId                                                                                                             
VM                         AliasProperty  VM = VirtualMemorySize64                                                                                                   
WS                         AliasProperty  WS = WorkingSet64                                                                                                          
Disposed                   Event          System.EventHandler Disposed(System.Object, System.EventArgs)                                                              
ErrorDataReceived          Event          System.Diagnostics.DataReceivedEventHandler ErrorDataReceived(System.Object, System.Diagnostics.DataReceivedEventArgs)     
Exited                     Event          System.EventHandler Exited(System.Object, System.EventArgs)                                                                
OutputDataReceived         Event          System.Diagnostics.DataReceivedEventHandler OutputDataReceived(System.Object, System.Diagnostics.DataReceivedEventArgs)    
BeginErrorReadLine         Method         void BeginErrorReadLine()                                                                                                  
BeginOutputReadLine        Method         void BeginOutputReadLine()                                                                                                 
CancelErrorRead            Method         void CancelErrorRead()                                                                                                     
CancelOutputRead           Method         void CancelOutputRead()                                                                                                    
Close                      Method         void Close()                                                                                                               
CloseMainWindow            Method         bool CloseMainWindow()                                                                                                     
CreateObjRef               Method         System.Runtime.Remoting.ObjRef CreateObjRef(type requestedType)                                                            
Dispose                    Method         void Dispose(), void IDisposable.Dispose()                                                                                 
Equals                     Method         bool Equals(System.Object obj)                                                                                             
GetHashCode                Method         int GetHashCode()                                                                                                          
GetLifetimeService         Method         System.Object GetLifetimeService()                                                                                         
GetType                    Method         type GetType()                                                                                                             
InitializeLifetimeService  Method         System.Object InitializeLifetimeService()                                                                                  
Kill                       Method         void Kill()                                                                                                                
Refresh                    Method         void Refresh()                                                                                                             
Start                      Method         bool Start()                                                                                                               
ToString                   Method         string ToString()                                                                                                          
WaitForExit                Method         bool WaitForExit(int milliseconds), void WaitForExit()                                                                     
WaitForInputIdle           Method         bool WaitForInputIdle(int milliseconds), bool WaitForInputIdle()                                                           
__NounName                 NoteProperty   string __NounName=Process                                                                                                  
BasePriority               Property       int BasePriority {get;}                                                                                                    
Container                  Property       System.ComponentModel.IContainer Container {get;}                                                                          
EnableRaisingEvents        Property       bool EnableRaisingEvents {get;set;}                                                                                        
ExitCode                   Property       int ExitCode {get;}                                                                                                        
ExitTime                   Property       datetime ExitTime {get;}                                                                                                   
Handle                     Property       System.IntPtr Handle {get;}                                                                                                
HandleCount                Property       int HandleCount {get;}                                                                                                     
HasExited                  Property       bool HasExited {get;}                                                                                                      
Id                         Property       int Id {get;}                                                                                                              
MachineName                Property       string MachineName {get;}                                                                                                  
MainModule                 Property       System.Diagnostics.ProcessModule MainModule {get;}                                                                         
MainWindowHandle           Property       System.IntPtr MainWindowHandle {get;}                                                                                      
MainWindowTitle            Property       string MainWindowTitle {get;}                                                                                              
MaxWorkingSet              Property       System.IntPtr MaxWorkingSet {get;set;}                                                                                     
MinWorkingSet              Property       System.IntPtr MinWorkingSet {get;set;}                                                                                     
Modules                    Property       System.Diagnostics.ProcessModuleCollection Modules {get;}                                                                  
NonpagedSystemMemorySize   Property       int NonpagedSystemMemorySize {get;}                                                                                        
NonpagedSystemMemorySize64 Property       long NonpagedSystemMemorySize64 {get;}                                                                                     
PagedMemorySize            Property       int PagedMemorySize {get;}                                                                                                 
PagedMemorySize64          Property       long PagedMemorySize64 {get;}                                                                                              
PagedSystemMemorySize      Property       int PagedSystemMemorySize {get;}                                                                                           
PagedSystemMemorySize64    Property       long PagedSystemMemorySize64 {get;}                                                                                        
PeakPagedMemorySize        Property       int PeakPagedMemorySize {get;}                                                                                             
PeakPagedMemorySize64      Property       long PeakPagedMemorySize64 {get;}                                                                                          
PeakVirtualMemorySize      Property       int PeakVirtualMemorySize {get;}                                                                                           
PeakVirtualMemorySize64    Property       long PeakVirtualMemorySize64 {get;}                                                                                        
PeakWorkingSet             Property       int PeakWorkingSet {get;}                                                                                                  
PeakWorkingSet64           Property       long PeakWorkingSet64 {get;}                                                                                               
PriorityBoostEnabled       Property       bool PriorityBoostEnabled {get;set;}                                                                                       
PriorityClass              Property       System.Diagnostics.ProcessPriorityClass PriorityClass {get;set;}                                                           
PrivateMemorySize          Property       int PrivateMemorySize {get;}                                                                                               
PrivateMemorySize64        Property       long PrivateMemorySize64 {get;}                                                                                            
PrivilegedProcessorTime    Property       timespan PrivilegedProcessorTime {get;}                                                                                    
ProcessName                Property       string ProcessName {get;}                                                                                                  
ProcessorAffinity          Property       System.IntPtr ProcessorAffinity {get;set;}                                                                                 
Responding                 Property       bool Responding {get;}                                                                                                     
SafeHandle                 Property       Microsoft.Win32.SafeHandles.SafeProcessHandle SafeHandle {get;}                                                            
SessionId                  Property       int SessionId {get;}                                                                                                       
Site                       Property       System.ComponentModel.ISite Site {get;set;}                                                                                
StandardError              Property       System.IO.StreamReader StandardError {get;}                                                                                
StandardInput              Property       System.IO.StreamWriter StandardInput {get;}                                                                                
StandardOutput             Property       System.IO.StreamReader StandardOutput {get;}                                                                               
StartInfo                  Property       System.Diagnostics.ProcessStartInfo StartInfo {get;set;}                                                                   
StartTime                  Property       datetime StartTime {get;}                                                                                                  
SynchronizingObject        Property       System.ComponentModel.ISynchronizeInvoke SynchronizingObject {get;set;}                                                    
Threads                    Property       System.Diagnostics.ProcessThreadCollection Threads {get;}                                                                  
TotalProcessorTime         Property       timespan TotalProcessorTime {get;}                                                                                         
UserProcessorTime          Property       timespan UserProcessorTime {get;}                                                                                          
VirtualMemorySize          Property       int VirtualMemorySize {get;}                                                                                               
VirtualMemorySize64        Property       long VirtualMemorySize64 {get;}                                                                                            
WorkingSet                 Property       int WorkingSet {get;}                                                                                                      
WorkingSet64               Property       long WorkingSet64 {get;}                                                                                                   
PSConfiguration            PropertySet    PSConfiguration {Name, Id, PriorityClass, FileVersion}                                                                     
PSResources                PropertySet    PSResources {Name, Id, Handlecount, WorkingSet, NonPagedMemorySize, PagedMemorySize, PrivateMemorySize, VirtualMemorySiz...
Company                    ScriptProperty System.Object Company {get=$this.Mainmodule.FileVersionInfo.CompanyName;}                                                  
CPU                        ScriptProperty System.Object CPU {get=$this.TotalProcessorTime.TotalSeconds;}                                                             
Description                ScriptProperty System.Object Description {get=$this.Mainmodule.FileVersionInfo.FileDescription;}                                          
FileVersion                ScriptProperty System.Object FileVersion {get=$this.Mainmodule.FileVersionInfo.FileVersion;}                                              
Path                       ScriptProperty System.Object Path {get=$this.Mainmodule.FileName;}                                                                        
Product                    ScriptProperty System.Object Product {get=$this.Mainmodule.FileVersionInfo.ProductName;}                                                  
ProductVersion             ScriptProperty System.Object ProductVersion {get=$this.Mainmodule.FileVersionInfo.ProductVersion;} 
```
```html
# run below command to kill notepad process
PS C:\WINDOWS\system32> (Get-Process -Name notepad).Kill()
```
### CopyTo()
```html
PS C:\WINDOWS\system32> Get-ChildItem | Get-Member


   TypeName: System.IO.DirectoryInfo

Name                      MemberType     Definition                                                                                                                  
----                      ----------     ----------                                                                                                                  
LinkType                  CodeProperty   System.String LinkType{get=GetLinkType;}                                                                                    
Mode                      CodeProperty   System.String Mode{get=Mode;}                                                                                               
Target                    CodeProperty   System.Collections.Generic.IEnumerable`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5...
Create                    Method         void Create(), void Create(System.Security.AccessControl.DirectorySecurity directorySecurity)                               
CreateObjRef              Method         System.Runtime.Remoting.ObjRef CreateObjRef(type requestedType)                                                             
CreateSubdirectory        Method         System.IO.DirectoryInfo CreateSubdirectory(string path), System.IO.DirectoryInfo CreateSubdirectory(string path, System.S...
Delete                    Method         void Delete(), void Delete(bool recursive)                                                                                  
EnumerateDirectories      Method         System.Collections.Generic.IEnumerable[System.IO.DirectoryInfo] EnumerateDirectories(), System.Collections.Generic.IEnume...
EnumerateFiles            Method         System.Collections.Generic.IEnumerable[System.IO.FileInfo] EnumerateFiles(), System.Collections.Generic.IEnumerable[Syste...
EnumerateFileSystemInfos  Method         System.Collections.Generic.IEnumerable[System.IO.FileSystemInfo] EnumerateFileSystemInfos(), System.Collections.Generic.I...
Equals                    Method         bool Equals(System.Object obj)                                                                                              
GetAccessControl          Method         System.Security.AccessControl.DirectorySecurity GetAccessControl(), System.Security.AccessControl.DirectorySecurity GetAc...
GetDirectories            Method         System.IO.DirectoryInfo[] GetDirectories(), System.IO.DirectoryInfo[] GetDirectories(string searchPattern), System.IO.Dir...
GetFiles                  Method         System.IO.FileInfo[] GetFiles(string searchPattern), System.IO.FileInfo[] GetFiles(string searchPattern, System.IO.Search...
GetFileSystemInfos        Method         System.IO.FileSystemInfo[] GetFileSystemInfos(string searchPattern), System.IO.FileSystemInfo[] GetFileSystemInfos(string...
GetHashCode               Method         int GetHashCode()                                                                                                           
GetLifetimeService        Method         System.Object GetLifetimeService()                                                                                          
GetObjectData             Method         void GetObjectData(System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext con...
GetType                   Method         type GetType()                                                                                                              
InitializeLifetimeService Method         System.Object InitializeLifetimeService()                                                                                   
MoveTo                    Method         void MoveTo(string destDirName)                                                                                             
Refresh                   Method         void Refresh()                                                                                                              
SetAccessControl          Method         void SetAccessControl(System.Security.AccessControl.DirectorySecurity directorySecurity)                                    
ToString                  Method         string ToString()                                                                                                           
PSChildName               NoteProperty   string PSChildName=0409                                                                                                     
PSDrive                   NoteProperty   PSDriveInfo PSDrive=C                                                                                                       
PSIsContainer             NoteProperty   bool PSIsContainer=True                                                                                                     
PSParentPath              NoteProperty   string PSParentPath=Microsoft.PowerShell.Core\FileSystem::C:\WINDOWS\system32                                               
PSPath                    NoteProperty   string PSPath=Microsoft.PowerShell.Core\FileSystem::C:\WINDOWS\system32\0409                                                
PSProvider                NoteProperty   ProviderInfo PSProvider=Microsoft.PowerShell.Core\FileSystem                                                                
Attributes                Property       System.IO.FileAttributes Attributes {get;set;}                                                                              
CreationTime              Property       datetime CreationTime {get;set;}                                                                                            
CreationTimeUtc           Property       datetime CreationTimeUtc {get;set;}                                                                                         
Exists                    Property       bool Exists {get;}                                                                                                          
Extension                 Property       string Extension {get;}                                                                                                     
FullName                  Property       string FullName {get;}                                                                                                      
LastAccessTime            Property       datetime LastAccessTime {get;set;}                                                                                          
LastAccessTimeUtc         Property       datetime LastAccessTimeUtc {get;set;}                                                                                       
LastWriteTime             Property       datetime LastWriteTime {get;set;}                                                                                           
LastWriteTimeUtc          Property       datetime LastWriteTimeUtc {get;set;}                                                                                        
Name                      Property       string Name {get;}                                                                                                          
Parent                    Property       System.IO.DirectoryInfo Parent {get;}                                                                                       
Root                      Property       System.IO.DirectoryInfo Root {get;}                                                                                         
BaseName                  ScriptProperty System.Object BaseName {get=$this.Name;}                                                                                    


   TypeName: System.IO.FileInfo

Name                      MemberType     Definition                                                                                                                  
----                      ----------     ----------                                                                                                                  
LinkType                  CodeProperty   System.String LinkType{get=GetLinkType;}                                                                                    
Mode                      CodeProperty   System.String Mode{get=Mode;}                                                                                               
Target                    CodeProperty   System.Collections.Generic.IEnumerable`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5...
AppendText                Method         System.IO.StreamWriter AppendText()                                                                                         
CopyTo                    Method         System.IO.FileInfo CopyTo(string destFileName), System.IO.FileInfo CopyTo(string destFileName, bool overwrite)              
Create                    Method         System.IO.FileStream Create()                                                                                               
CreateObjRef              Method         System.Runtime.Remoting.ObjRef CreateObjRef(type requestedType)                                                             
CreateText                Method         System.IO.StreamWriter CreateText()                                                                                         
Decrypt                   Method         void Decrypt()                                                                                                              
Delete                    Method         void Delete()                                                                                                               
Encrypt                   Method         void Encrypt()                                                                                                              
Equals                    Method         bool Equals(System.Object obj)                                                                                              
GetAccessControl          Method         System.Security.AccessControl.FileSecurity GetAccessControl(), System.Security.AccessControl.FileSecurity GetAccessContro...
GetHashCode               Method         int GetHashCode()                                                                                                           
GetLifetimeService        Method         System.Object GetLifetimeService()                                                                                          
GetObjectData             Method         void GetObjectData(System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext con...
GetType                   Method         type GetType()                                                                                                              
InitializeLifetimeService Method         System.Object InitializeLifetimeService()                                                                                   
MoveTo                    Method         void MoveTo(string destFileName)                                                                                            
Open                      Method         System.IO.FileStream Open(System.IO.FileMode mode), System.IO.FileStream Open(System.IO.FileMode mode, System.IO.FileAcce...
OpenRead                  Method         System.IO.FileStream OpenRead()                                                                                             
OpenText                  Method         System.IO.StreamReader OpenText()                                                                                           
OpenWrite                 Method         System.IO.FileStream OpenWrite()                                                                                            
Refresh                   Method         void Refresh()                                                                                                              
Replace                   Method         System.IO.FileInfo Replace(string destinationFileName, string destinationBackupFileName), System.IO.FileInfo Replace(stri...
SetAccessControl          Method         void SetAccessControl(System.Security.AccessControl.FileSecurity fileSecurity)                                              
ToString                  Method         string ToString()                                                                                                           
PSChildName               NoteProperty   string PSChildName=@AdvancedKeySettingsNotification.png                                                                     
PSDrive                   NoteProperty   PSDriveInfo PSDrive=C                                                                                                       
PSIsContainer             NoteProperty   bool PSIsContainer=False                                                                                                    
PSParentPath              NoteProperty   string PSParentPath=Microsoft.PowerShell.Core\FileSystem::C:\WINDOWS\system32                                               
PSPath                    NoteProperty   string PSPath=Microsoft.PowerShell.Core\FileSystem::C:\WINDOWS\system32\@AdvancedKeySettingsNotification.png                
PSProvider                NoteProperty   ProviderInfo PSProvider=Microsoft.PowerShell.Core\FileSystem                                                                
Attributes                Property       System.IO.FileAttributes Attributes {get;set;}                                                                              
CreationTime              Property       datetime CreationTime {get;set;}                                                                                            
CreationTimeUtc           Property       datetime CreationTimeUtc {get;set;}                                                                                         
Directory                 Property       System.IO.DirectoryInfo Directory {get;}                                                                                    
DirectoryName             Property       string DirectoryName {get;}                                                                                                 
Exists                    Property       bool Exists {get;}                                                                                                          
Extension                 Property       string Extension {get;}                                                                                                     
FullName                  Property       string FullName {get;}                                                                                                      
IsReadOnly                Property       bool IsReadOnly {get;set;}                                                                                                  
LastAccessTime            Property       datetime LastAccessTime {get;set;}                                                                                          
LastAccessTimeUtc         Property       datetime LastAccessTimeUtc {get;set;}                                                                                       
LastWriteTime             Property       datetime LastWriteTime {get;set;}                                                                                           
LastWriteTimeUtc          Property       datetime LastWriteTimeUtc {get;set;}                                                                                        
Length                    Property       long Length {get;}                                                                                                          
Name                      Property       string Name {get;}                                                                                                          
BaseName                  ScriptProperty System.Object BaseName {get=if ($this.Extension.Length -gt 0){$this.Name.Remove($this.Name.Length - $this.Extension.Lengt...
VersionInfo               ScriptProperty System.Object VersionInfo {get=[System.Diagnostics.FileVersionInfo]::GetVersionInfo($this.FullName);}  
```
```html
PS C:\WINDOWS\system32> (Get-ChildItem C:\Users\xilongj\Desktop\netdom.txt).CopyTo("C:\Users\xilongj\Desktop\netdom2.txt")

Mode                LastWriteTime         Length Name                                                                                                                
----                -------------         ------ ----                                                                                                                
-a----        5/14/2021  12:40 PM            348 netdom2.txt                                                                                                         



PS C:\WINDOWS\system32> (Get-ChildItem C:\Users\xilongj\Desktop\netdom.txt).CopyTo("\\cbsdb01\xilongj\netdom.txt")

Mode                LastWriteTime         Length Name                                                                                                                
----                -------------         ------ ----                                                                                                                
-a----        5/14/2021  12:40 PM            348 netdom.txt 
```
```html
PS C:\WINDOWS\system32> (Get-ChildItem $PSHOME\powershell.exe).CreationTime

Tuesday, March 19, 2019 12:46:56 PM
```
```html
PS C:\WINDOWS\system32> Get-EventLog -LogName Security -Newest 6 | Select-Object Source, TimeWritten, MachineName, Message

Source                              TimeWritten           MachineName              Message                                                                           
------                              -----------           -----------              -------                                                                           
Microsoft-Windows-Security-Auditing 5/14/2021 1:16:28 PM  CBSWS01.cnbs.cnblogs.com Special privileges assigned to new logon....                                      
Microsoft-Windows-Security-Auditing 5/14/2021 1:16:28 PM  CBSWS01.cnbs.cnblogs.com An account was successfully logged on....                                         
Microsoft-Windows-Security-Auditing 5/14/2021 1:00:28 PM  CBSWS01.cnbs.cnblogs.com Special privileges assigned to new logon....                                      
Microsoft-Windows-Security-Auditing 5/14/2021 1:00:28 PM  CBSWS01.cnbs.cnblogs.com An account was successfully logged on....                                         
Microsoft-Windows-Security-Auditing 5/14/2021 12:57:37 PM CBSWS01.cnbs.cnblogs.com Special privileges assigned to new logon....                                      
Microsoft-Windows-Security-Auditing 5/14/2021 12:57:37 PM CBSWS01.cnbs.cnblogs.com An account was successfully logged on....   
```
### Get-TimeZone
```html
PS C:\WINDOWS\system32> Get-TimeZone


Id                         : China Standard Time
DisplayName                : (UTC+08:00) Beijing, Chongqing, Hong Kong, Urumqi
StandardName               : China Standard Time
DaylightName               : China Daylight Time
BaseUtcOffset              : 08:00:00
SupportsDaylightSavingTime : False
```

### Practices
```html
PS C:\WINDOWS\system32> (Get-Process -Name chrome).Kill()
```
```html
PS C:\WINDOWS\system32> (Get-ChildItem C:\Users\xilongj\Desktop\netdom.html).CopyTo("C:\Users\xilongj\Desktop\netdom.txt")
```
```html
PS C:\WINDOWS\system32> (Get-TimeZone).DaylightName
China Daylight Time
```
```html
PS C:\WINDOWS\system32> Get-WmiObject -Class Win32_Bios

SMBIOSBIOSVersion : 1.19.0
Manufacturer      : Dell Inc.
Name              : 1.19.0    
SerialNumber      : 9Z6J5S2
Version           : DELL  - 1072009

PS C:\WINDOWS\system32> (Get-WmiObject -Class Win32_Bios).SMBIOSBIOSVERSION
1.19.0
```