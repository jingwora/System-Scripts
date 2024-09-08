## `az` vs `azd`:
- `az` is a low-level tool focused on Azure resource management, while `azd` simplifies the development and deployment of full applications by managing both code and infrastructure.
- Use `az` (Azure CLI) if you need detailed control over specific resources (e.g., creating a virtual machine, managing storage accounts).
- Use `azd` (Azure Developer CLI) if you want to develop and deploy an entire application (e.g., a web app or microservice) with automated infrastructure provisioning, deployment, and environment management.

## Common Commands (az)

| Group                | Command                                  | Description                                                   | Format                          | Example                                                       |
|----------------------|------------------------------------------|---------------------------------------------------------------|----------------------------------|---------------------------------------------------------------|
| **Authentication**    | `az login`                               | Logs in to Azure account                                       | `az login`                      | `az login`                                                    |
| **General**           | `az account show`                        | Shows details of the current Azure account                     | `az account show`                 | `az account show`                                              |
| **General**           | `az account list`                        | Lists all Azure subscriptions for the logged-in account        | `az account list`                 | `az account list`                                              |
| **General**           | `az resource list`                       | Lists all resources in the specified subscription or resource group | `az resource list --resource-group <group>` | `az resource list --resource-group MyResourceGroup`           |
| **Resource Group**    | `az group create`                        | Creates a resource group in Azure                              | `az group create --name <name> --location <location>` | `az group create --name MyResourceGroup --location eastus`    |
| **Resource Group**    | `az group delete`                        | Deletes a resource group in Azure                              | `az group delete --name <name>` | `az group delete --name MyResourceGroup`                      |
| **Virtual Machines**  | `az vm create`                           | Creates a virtual machine in Azure                             | `az vm create --resource-group <group> --name <vm-name>` | `az vm create --resource-group MyResourceGroup --name MyVM`   |
| **Virtual Machines**  | `az vm start`                            | Starts a stopped virtual machine                               | `az vm start --resource-group <group> --name <vm-name>` | `az vm start --resource-group MyResourceGroup --name MyVM`    |
| **Virtual Machines**  | `az vm stop`                             | Stops a running virtual machine                                | `az vm stop --resource-group <group> --name <vm-name>` | `az vm stop --resource-group MyResourceGroup --name MyVM`     |
| **Storage**           | `az storage account create`              | Creates an Azure storage account                               | `az storage account create --name <account> --resource-group <group>` | `az storage account create --name mystorage --resource-group MyResourceGroup` |
| **Storage**           | `az storage account delete`              | Deletes an Azure storage account                               | `az storage account delete --name <account> --resource-group <group>` | `az storage account delete --name mystorage --resource-group MyResourceGroup` |
| **Kubernetes (AKS)**  | `az aks create`                          | Creates an Azure Kubernetes Service (AKS) cluster              | `az aks create --resource-group <group> --name <cluster>` | `az aks create --resource-group MyResourceGroup --name MyCluster` |
| **Kubernetes (AKS)**  | `az aks get-credentials`                 | Gets credentials for a managed Kubernetes cluster              | `az aks get-credentials --resource-group <group> --name <cluster>` | `az aks get-credentials --resource-group MyResourceGroup --name MyCluster` |
| **SQL Server**        | `az sql server create`                   | Creates an Azure SQL server                                    | `az sql server create --name <server-name> --resource-group <group>` | `az sql server create --name MySQLServer --resource-group MyResourceGroup` |
| **SQL Database**      | `az sql db create`                       | Creates a database in an Azure SQL server                      | `az sql db create --resource-group <group> --server <server> --name <db>` | `az sql db create --resource-group MyResourceGroup --server MySQLServer --name MyDatabase` |
| **Function App**      | `az functionapp create`                  | Creates an Azure Function App                                  | `az functionapp create --resource-group <group> --name <appname> --storage-account <storage>` | `az functionapp create --resource-group MyResourceGroup --name MyFunctionApp --storage-account mystorage` |
| **App Service**       | `az appservice plan create`              | Creates an App Service plan                                    | `az appservice plan create --name <plan-name> --resource-group <group>` | `az appservice plan create --name MyAppServicePlan --resource-group MyResourceGroup` |
| **Web App**           | `az webapp create`                       | Creates a web app                                              | `az webapp create --resource-group <group> --plan <plan-name> --name <app-name>` | `az webapp create --resource-group MyResourceGroup --plan MyAppServicePlan --name MyWebApp` |


## Common Commands (azd)

| Group              | Command                                  | Description                                                   | Format                          | Example                                                       |
|--------------------|------------------------------------------|---------------------------------------------------------------|----------------------------------|---------------------------------------------------------------|
| **Authentication** | `azd auth login`                         | Logs in to Azure with Azure Developer CLI                      | `azd auth login`                 | `azd auth login`                                               |
| **Authentication** | `azd auth logout`                        | Logs out of Azure Developer CLI                                | `azd auth logout`                | `azd auth logout`                                              |
| **Initialization** | `azd init`                               | Initializes a new project based on a template                  | `azd init --template <template>`  | `azd init --template azure-web-app`                            |
| **Provisioning**   | `azd provision`                          | Provisions Azure resources defined in your project             | `azd provision`                  | `azd provision`                                                |
| **Deployment**     | `azd deploy`                             | Deploys code to the Azure resources                            | `azd deploy`                     | `azd deploy`                                                   |
| **Monitor**        | `azd monitor`                            | Opens Azure Monitor for the project                            | `azd monitor`                    | `azd monitor`                                                  |
| **Pipeline**       | `azd pipeline config`                    | Configures CI/CD pipeline for the project                      | `azd pipeline config`            | `azd pipeline config`                                          |
| **Environment**    | `azd env list`                           | Lists all environments for the current project                 | `azd env list`                   | `azd env list`                                                 |
| **Environment**    | `azd env select`                         | Selects a specific environment                                 | `azd env select <env-name>`       | `azd env select dev`                                           |
| **Environment**    | `azd env new`                            | Creates a new environment for the project                      | `azd env new <env-name>`          | `azd env new staging`                                          |
| **Environment**    | `azd env delete`                         | Deletes an environment and its resources                       | `azd env delete <env-name>`       | `azd env delete dev`                                           |
| **Configuration**  | `azd config list`                        | Lists all configuration settings                               | `azd config list`                | `azd config list`                                              |
| **Configuration**  | `azd config set`                         | Sets a configuration setting for the current project           | `azd config set <setting> <value>`| `azd config set azd.default.location eastus`                   |
| **Configuration**  | `azd config get`                         | Retrieves a configuration setting                             | `azd config get <setting>`        | `azd config get azd.default.location`                          |
| **General**        | `azd version`                            | Shows the version of Azure Developer CLI                       | `azd version`                    | `azd version`                                                  |




