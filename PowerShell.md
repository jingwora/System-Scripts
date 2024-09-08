
Commond Commands

| Group            | Command                   | Description                                               | Format                          | Example                                                      |
|------------------|---------------------------|-----------------------------------------------------------|----------------------------------|--------------------------------------------------------------|
| **Help & Info**  | `Get-Help`                | Displays information about PowerShell commands            | `Get-Help <CommandName>`         | `Get-Help Get-Process`                                       |
| **Help & Info**  | `Get-Command`             | Lists all available PowerShell commands                   | `Get-Command`                   | `Get-Command`                                                |
| **Service**      | `Get-Service`             | Retrieves the status of services on a local or remote computer | `Get-Service`                   | `Get-Service`                                                |
| **Service**      | `Start-Service`           | Starts a stopped service                                  | `Start-Service <ServiceName>`    | `Start-Service Spooler`                                      |
| **Service**      | `Stop-Service`            | Stops a running service                                   | `Stop-Service <ServiceName>`     | `Stop-Service Spooler`                                       |
| **Process**      | `Get-Process`             | Retrieves the processes running on the computer           | `Get-Process`                   | `Get-Process`                                                |
| **Process**      | `Stop-Process`            | Stops a process by process ID or name                     | `Stop-Process <ProcessName>`     | `Stop-Process -Name notepad`                                 |
| **File Handling**| `Get-Content`             | Displays the contents of a file                           | `Get-Content <FilePath>`         | `Get-Content C:\Logs\example.txt`                            |
| **Navigation**   | `Set-Location`            | Changes the current working directory                     | `Set-Location <Path>`            | `Set-Location C:\Windows`                                    |
| **File Handling**| `Get-ChildItem`           | Lists all files and directories within a specified path    | `Get-ChildItem <Path>`           | `Get-ChildItem C:\Users`                                     |
| **File Handling**| `Copy-Item`               | Copies an item (file/folder) to a new location            | `Copy-Item <Source> <Destination>`| `Copy-Item C:\Temp\file.txt C:\Backup\file.txt`              |
| **File Handling**| `Move-Item`               | Moves an item (file/folder) to a new location             | `Move-Item <Source> <Destination>`| `Move-Item C:\Temp\file.txt C:\Backup\file.txt`              |
| **File Handling**| `Remove-Item`             | Deletes files, folders, or other objects                  | `Remove-Item <Path>`             | `Remove-Item C:\Temp\file.txt`                               |
| **File Handling**| `Rename-Item`             | Renames a file or folder                                  | `Rename-Item <Path> <NewName>`   | `Rename-Item C:\Temp\file.txt newfile.txt`                   |
| **File Handling**| `New-Item`                | Creates a new file or folder                              | `New-Item -Path <Path> -ItemType`| `New-Item -Path C:\Temp\newfile.txt -ItemType File`          |
| **Date/Time**    | `Get-Date`                | Retrieves the current date and time                       | `Get-Date`                      | `Get-Date`                                                   |
