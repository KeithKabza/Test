# Exercise 1: Setting up your development environment

### Overview

This lab will require access to an Azure subscription. You can use an existing internal subscription or request an Azure pass for the lab. This bot will use the following Azure components

* Azure Bot Channels Registration
* Azure App Registration
* Azure Key Vault

> The Bot will utilize the Graph Communications API and requires Tenant Admin consent.

Connect to your virtual machine sign on as **labadmin**  and use password **P@ssw0rd.** Once connected we need to install the following prerequisites:

* [Azure Service Fabric](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-get-started)
* [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest)
* [Azure PowerShell](https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-6.8.1)
* [PostMan](https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop)
* [ngrok](https://ngrok.com/)

### Deploy Cloud App

Logon to your Azure subscription and click create _**Create a Resource**_ search for "Cloud Service"  and click create.

![](.gitbook/assets/image%20%2816%29.png)

Enter **huebotlabxxx** for the dns name

![](.gitbook/assets/image%20%2811%29.png)

### Setup SSL Certificate

Download the teamsbots.com wildcard certificate to your virtual server : [https://1drv.ms/u/s!Al-Ih3130\_Cik7NijkBoAUmwWPuDJQ?e=Eynf86](https://1drv.ms/u/s!Al-Ih3130_Cik7NijkBoAUmwWPuDJQ?e=Eynf86)  

Navigate to the newly deployed cloud services in Azure portal and select certificates and click the Upload menu option

 

![](.gitbook/assets/image%20%2815%29.png)

Browse for the certificate downloaded in the previous step and provide the certificate password: **summerready**

![](.gitbook/assets/image%20%285%29.png)

Refresh the certificate blade and you should see the imported wildcard certificate

![](.gitbook/assets/image%20%282%29.png)

