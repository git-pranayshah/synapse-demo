# Synapse Demo Environment with Adventureworks Sample Data

Synapse comes with the multiple flavour including ETL, Storage & Analytics. Current solution will help you to prepare synapse analytics to transfer data from SQL Server to Synapse dedicated SQL pool with the Azure Data factory pipeline. Infrastructure architects/developers will have better understanding of configuring Synapse to connect SQL Server with the Azure KeyVault & will help Data Engineers to use Azure Data factory pipeline with Copy Table component to move Sales data from the Adventure Works Sales data to the Synapse Dedicated pool.  

# Demo Environment Template

Template should help you to kick start working with the Synapse environment with the preloaded sales data. ARM template will deploy following components in the environment.
1.	Microsoft SQL Server with Sales Adventureworks Database
2.	Azure Key Vault with Connection Strings for the SQL Server
4.  Storage Account
3.	Synapse Analytics workspace 
    - Dedicated SQLServer Pool
    - Create Table Script
    - Select Table Script
    - Azure Data Factory pipeline to move data from SQL Server to Synapse Storage
    - Linked Service with its connection configurations


## Target audience

- Infrastructure Engineer
- Data Engineer
- Cloud Solution Architect
- Data Archtiect

# Product/LZ architecture

The [Template.json](https://github.com/git-pranayshah/template/blob/master/template.json) Azure Resource Manager template will help you automatically deploy the diagram below architecture

![alt image](https://github.com/git-pranayshah/template/blob/master/images/Landing_Zone_Template.png)

[Template.json](https://github.com/git-pranayshah/template/blob/master/template.json) can be modified to match your current infrastructure needs.

# Pre-requisite to deploy the Template

## One Click Deploying Teamplate
<!-- Powershell command for Translating Git URL for template.json
    $url = "https://raw.githubusercontent.com/git-pranayshah/synapse-demo/dev/ARM%20Template/SQL-Server/azure_sql.json"
    [uri]::EscapeDataString($url)
    >> uri = https%3A%2F%2Fraw.githubusercontent.com%2Fgit-pranayshah%2FAnalysisService%2Fmaster%2Ftemplate.json

Base URL: https://portal.azure.com/#create/Microsoft.Template/uri
Final URL: <Base URL>/<uri>
-->
[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fgit-pranayshah%2Fsynapse-demo%2Fdev%2FARM%2520Template%2Fdeployment.json)


## Deploying an ARM Template using the Azure portal

- Visit https://portal.azure.com

Using the search bar on top type Templates

![alt image](https://github.com/git-pranayshah/template/blob/master/images/Search.png)

- Create a new template

![alt image](https://github.com/git-pranayshah/template/blob/master/images/create.png)

- Give a name and a description to the template

![alt image](https://github.com/git-pranayshah/template/blob/master/images/Name%20and%20Description.png)

- Add for modified [Template.json](https://github.com/git-pranayshah/template/blob/master/template.json) and save it

![alt image](https://github.com/git-pranayshah/template/blob/master/images/add%20code.png)

- Select the newly added template and click deploy

![alt image](https://github.com/git-pranayshah/template/blob/master/images/Select%20and%20deploy%20template.png)

- Fill out the blanks with your details and click purchase

![alt image](https://github.com/git-pranayshah/template/blob/master/images/Fill%20out%20the%20details%20and%20purchase.png)

- Allow 30 minutes for the deployment to complete
- Peer your Hub and Spoke Virtual Networks as needed

## Azure services and related products

example!!
- Azure Networking
- Security

## Related references
example!!
- https://docs.microsoft.com/en-us/azure/virtual-desktop/overview
- https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/ready/landing-zone/
- https://docs.microsoft.com/en-us/azure/virtual-network/tutorial-connect-virtual-networks-portal#peer-virtual-networks
- https://docs.microsoft.com/en-us/azure/virtual-desktop/safe-url-list#virtual-machines

## License & Contribute

You are responsible for the performance, the necessary testing, and if needed any regulatory clearance for any of the models produced by this toolbox.
Please refer [LICENSE](LICENSE) &  [Contribute](https://github.com/git-pranayshah/AnalysisService/blob/master/Contribute.md) for more details









## One Click Deploying Teamplate
<!-- Powershell command for Translating Git URL for template.json
    $url = "https://raw.githubusercontent.com/git-pranayshah/synapse-demo/dev/ARM%20Template/SQL-Server/azure_sql.json"
    [uri]::EscapeDataString($url)
    >> uri = https%3A%2F%2Fraw.githubusercontent.com%2Fgit-pranayshah%2FAnalysisService%2Fmaster%2Ftemplate.json

Base URL: https://portal.azure.com/#create/Microsoft.Template/uri
Final URL: <Base URL>/<uri>
-->
[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fgit-pranayshah%2Fsynapse-demo%2Fdev%2FARM%2520Template%2Fdeployment.json)


## One Click Test Deploying Teamplate
<!-- Powershell command for Translating Git URL for template.json
    $url = "https://raw.githubusercontent.com/git-pranayshah/synapse-demo/dev/ARM%20Template/SQL-Server/azure_sql.json"
    [uri]::EscapeDataString($url)
    >> uri = https%3A%2F%2Fraw.githubusercontent.com%2Fgit-pranayshah%2FAnalysisService%2Fmaster%2Ftemplate.json

Base URL: https://portal.azure.com/#create/Microsoft.Template/uri
Final URL: <Base URL>/<uri>
-->
[![Test Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fgit-pranayshah%2Fsynapse-demo%2Fdev%2FARM%2520Template%2FTestDeployment.json)