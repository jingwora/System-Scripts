
## Commond Commands

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

## Azure Related Commands

| Group            | Command                                  | Description                                                   | Format                          | Example                                                       |
|------------------|------------------------------------------|---------------------------------------------------------------|----------------------------------|---------------------------------------------------------------|
| **Resource Group**| `New-AzResourceGroup`                   | Creates a resource group in Azure                              | `New-AzResourceGroup -Name <name> -Location <location>` | `New-AzResourceGroup -Name MyResourceGroup -Location EastUS`  |
| **Virtual Machines**| `New-AzVM`                            | Creates a virtual machine in Azure                             | `New-AzVM -ResourceGroupName <group> -Name <vm-name>` | `New-AzVM -ResourceGroupName MyResourceGroup -Name MyVM`      |
| **Storage**       | `Set-AzStorageAccount`                  | Configures an Azure storage account                            | `Set-AzStorageAccount -ResourceGroupName <group> -Name <account>` | `Set-AzStorageAccount -ResourceGroupName MyResourceGroup -Name MyStorageAccount` |
| **Function App**  | `New-AzFunctionApp`                     | Creates an Azure Function App                                  | `New-AzFunctionApp -ResourceGroupName <group> -Name <appname> -StorageAccountName <storage>` | `New-AzFunctionApp -ResourceGroupName MyResourceGroup -Name MyFunctionApp -StorageAccountName MyStorageAccount` |
| **App Service**   | `New-AzAppServicePlan`                  | Creates an App Service plan                                    | `New-AzAppServicePlan -ResourceGroupName <group> -Name <plan-name>` | `New-AzAppServicePlan -ResourceGroupName MyResourceGroup -Name MyAppServicePlan` |
| **Web App**       | `New-AzWebApp`                          | Creates an Azure Web App                                       | `New-AzWebApp -ResourceGroupName <group> -Name <app-name> -AppServicePlan <plan>` | `New-AzWebApp -ResourceGroupName MyResourceGroup -Name MyWebApp -AppServicePlan MyAppServicePlan` |
| **Kubernetes**    | `New-AzAks`                             | Creates an Azure Kubernetes Service (AKS) cluster              | `New-AzAks -ResourceGroupName <group> -Name <aks-name>` | `New-AzAks -ResourceGroupName MyResourceGroup -Name MyAKS`    |
| **SQL Server**    | `New-AzSqlServer`                       | Creates an Azure SQL server                                    | `New-AzSqlServer -ResourceGroupName <group> -ServerName <name> -Location <location>` | `New-AzSqlServer -ResourceGroupName MyResourceGroup -ServerName MySQLServer -Location EastUS` |
| **SQL Database**  | `New-AzSqlDatabase`                     | Creates an Azure SQL database                                  | `New-AzSqlDatabase -ResourceGroupName <group> -ServerName <server> -DatabaseName <db>` | `New-AzSqlDatabase -ResourceGroupName MyResourceGroup -ServerName MySQLServer -DatabaseName MyDatabase` |
| **VM Management** | `Start-AzVM`                            | Starts a virtual machine                                       | `Start-AzVM -ResourceGroupName <group> -Name <vm-name>` | `Start-AzVM -ResourceGroupName MyResourceGroup -Name MyVM`    |
| **VM Management** | `Stop-AzVM`                             | Stops a virtual machine                                        | `Stop-AzVM -ResourceGroupName <group> -Name <vm-name>` | `Stop-AzVM -ResourceGroupName MyResourceGroup -Name MyVM`     |
| **VM Management** | `Restart-AzVM`                          | Restarts a virtual machine                                     | `Restart-AzVM -ResourceGroupName <group> -Name <vm-name>` | `Restart-AzVM -ResourceGroupName MyResourceGroup -Name MyVM`  |
| **VM Management** | `Remove-AzVM`                           | Deletes a virtual machine                                      | `Remove-AzVM -ResourceGroupName <group> -Name <vm-name>` | `Remove-AzVM -ResourceGroupName MyResourceGroup -Name MyVM`   |
| **Resource Group**| `Remove-AzResourceGroup`                | Deletes a resource group                                       | `Remove-AzResourceGroup -Name <name>` | `Remove-AzResourceGroup -Name MyResourceGroup`                |
| **General**       | `Get-AzResource`                        | Lists all Azure resources in a subscription                    | `Get-AzResource`                   | `Get-AzResource`                                              |









