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
4.  Security Firewall
    - Synapse Workspace will have its access only from the client ip given at the time of deployment
    - Add more ip whitelisting in network firewall to allow other to use the synapse workspace


## Target audience

- Infrastructure Engineer
- Data Engineer
- Cloud Solution Architect
- Data Architect

# Landing Zone Architecture

The [Deployment.json](https://github.com/git-pranayshah/synapse-demo/blob/master/ARM%20Template/deployment.json) Azure Resource Manager template will help you automatically deploy the diagram below architecture

![alt image](https://raw.githubusercontent.com/git-pranayshah/synapse-demo/master/images/Landing_Zone_Template.png)

[Deployment.json](https://github.com/git-pranayshah/synapse-demo/blob/master/ARM%20Template/deployment.json) can be modified to match your current infrastructure needs.

# Pre-requisite to deploy the Template
To use this solution, you will need access to an Azure subscription. Also have to look for correct public ip. You can find your public ipv4 ip from the website https://whatsmyip.com/

## One Click Deploying Template
<!-- Powershell command for Translating Git URL for template.json
    $url = "https://raw.githubusercontent.com/git-pranayshah/synapse-demo/master/ARM%20Template/SQL-Server/azure_sql.json"
    [uri]::EscapeDataString($url)
    >> uri = https%3A%2F%2Fraw.githubusercontent.com%2Fgit-pranayshah%2FAnalysisService%2Fmaster%2Ftemplate.json

Base URL: https://portal.azure.com/#create/Microsoft.Template/uri
Final URL: <Base URL>/<uri>
-->
[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fgit-pranayshah%2Fsynapse-demo%2Fmaster%2FARM%2520Template%2Fdeployment.json)


## Deploying an ARM Template using the Azure portal

- Visit https://portal.azure.com

Using the search bar on top type Templates

![alt image](https://raw.githubusercontent.com/git-pranayshah/synapse-demo/master/images/Search.png)

- Create a new template

![alt image](https://raw.githubusercontent.com/git-pranayshah/synapse-demo/master/images/create.png)

- Give a name and a description to the template

![alt image](https://raw.githubusercontent.com/git-pranayshah/synapse-demo/master/images/Name%20and%20Description.png)

- Add for modified [Deployment.json](https://github.com/git-pranayshah/synapse-demo/blob/master/ARM%20Template/deployment.json) and save it

![alt image](https://raw.githubusercontent.com/git-pranayshah/synapse-demo/master/images/add%20code.png)

- Select the newly added template and click deploy

![alt image](https://raw.githubusercontent.com/git-pranayshah/synapse-demo/master/images/Select%20and%20deploy%20template.png)

- Fill out the blanks with your details and click purchase

![alt image](https://raw.githubusercontent.com/git-pranayshah/synapse-demo/master/images/CustomDeployment.jpeg)

- Allow 30 minutes for the deployment to complete
- Once deployment is completed please proceed with the Post deployment tasks

# Post Deployment tasks

Post deployment its required to configure correct Azure KeyVault which has required credentials to connect to the Microsoft SQL Server having sample Sales data. ARM template will comission,
ARM template will deploy required infrastructure with Synapse. Also, it will deploy following items in synapse to kickstart with the demo
1.	Under Data 1 Database
    -	dedicatedsqlpool(SQL)
2.	Under Develop 2 Scripts,
    -	01 Customer_Table
    -	02 Select_Customer_Data
3.	Under Integrate 1 Pipeline
    -	Copy Customer Data Demo


## 1. Validate Deployed Services

Validate deployed services which will have similar to below screenshot except the suffix "pagi6to7auim2". This suffix is unique for each resource group name.

![alt image](https://raw.githubusercontent.com/git-pranayshah/synapse-demo/master/images/Deployed%20Services.jpeg)

## 2. Open Synapse Workspace

![alt image](https://raw.githubusercontent.com/git-pranayshah/synapse-demo/master/images/Synapse-OpenWorkspace.gif)

## 3. Update Linked Service & Confirm SQL Connectivity

![alt image](https://raw.githubusercontent.com/git-pranayshah/synapse-demo/master/images/Synapse-Setup.gif)

## 4. Create Table Schema in Synapse SQL Dedicated Pool

![alt image](https://raw.githubusercontent.com/git-pranayshah/synapse-demo/master/images/Synapse-CreateTable.gif)

## 5. Execute Data Pipeline & Validate Data load

![alt image](https://raw.githubusercontent.com/git-pranayshah/synapse-demo/master/images/Synapse-ExecuteTable.gif)

## Related references
- https://docs.microsoft.com/en-us/azure/synapse-analytics/overview-what-is
- https://docs.microsoft.com/en-us/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-overview-what-is
- https://docs.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver16&tabs=ssms
- https://docs.microsoft.com/en-us/azure/devops/pipelines/release/azure-key-vault?view=azure-devops&tabs=yaml
- https://docs.microsoft.com/en-us/azure/data-factory/how-to-use-azure-key-vault-secrets-pipeline-activities
- https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/ready/landing-zone/


## License & Contribute

You are responsible for the performance, the necessary testing, and if needed any regulatory clearance for any of the models produced by this toolbox.
Please refer [LICENSE](LICENSE) &  [Contribute](https://github.com/git-pranayshah/AnalysisService/blob/master/Contribute.md) for more details