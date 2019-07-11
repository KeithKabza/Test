# Table of Contents

#### [Developing a Teams Media Bot](./)

Exercise 1: Setting up your development environment

[Exercise 2: Registering your Media Bot](exercise-2-registering-your-media-bot.md)

[Exercise 3: Clone the Source Code in Visual Studio](exercise-3-clone-the-source-code-in-visual-studio.md)

[Exercise 4: Publish Bot application to Azure](exercise-4-publish-bot-application-to-azure.md)

[Exercise 5: Test HueBot Using Microsoft Teams](exercise-5-test-huebot-using-microsoft-teams.md)

[Exercise 6: Configure Azure Unified Speech API](exercise-6-configure-azure-unified-speech-api.md)

[Exercise 7: Modify Speech Recognition and Publish in Debug mode.]()

[Exercise 8: Add a new Color option and debug locally](exercise-7-add-a-new-color-option-and-debug-locally.md)

[Conclusion](conclusion.md)





## Lab: Developing a Teams Media Bot

During this lab, you will learn how to build and deploy a Microsoft Teams media bot in Office 365 that will you allow your Bot to join a Teams meeting and gain access to the audio and video streams in the meeting. During the lab you will use the Microsoft Teams clients to join meetings and interact with the media bot.  The lab is divided into several exercises that will help you understand how to intelligent media bots that can perform advanced tasks using cognitive services. 

Estimated time to complete: _**40 minutes**_

### Before you begin

The type text feature **\[T\]** used in this lab will send the specific text string to the active window in the virtual machine. Always compare the text in the lab document with the typed text in the virtual machine and verify the expected text shown.

To complete the exercises in this lab, you will need a an O365 Tenant with an enterprise E5 Trial subscription and an Active Azure subscription. You can obtain one by registering for the Office Developer Program here [https://developer.microsoft.com/office/profile](https://developer.microsoft.com/office/profile)

Follow the prompts to create a new subscription and complete the required forms. 

![New Office 365 Developer Subscription](.gitbook/assets/image%20%2878%29.png)

Provide your phone number and complete the process by entering the 5 digit code you received via text message. Once complete your subscription will be created!

![](.gitbook/assets/image%20%289%29.png)

You should be able to logon to your subscription now. Now you need to assign some licenses and create a few test users. Using the Office 365 Admin center create at least two test users. Assign one of the provided E3 Licenses to each of your users. 

![](.gitbook/assets/image%20%2896%29.png)

### Enable Azure Pass

Navigate to this url [https://www.microsoftazurepass.com/](https://www.microsoftazurepass.com/) to activate the Azure Pass for this lab instance.

![](.gitbook/assets/image%20%2895%29.png)

Click the start button and sign on with the O365 administrator account you created in the previous step.

![](.gitbook/assets/image%20%2882%29.png)

Click **Confirm Microsoft Account**

![](.gitbook/assets/image%20%288%29.png)

Now enter the Azure Pass you were provided for the lab and click **Claim Promo Code**

![](.gitbook/assets/image%20%2828%29.png)

Click Next on the following screen

![](.gitbook/assets/image%20%2852%29.png)

Agree to the subscription agreement and click signup.

![](.gitbook/assets/image%20%2833%29.png)

Once your subscription is active you will be redirect to the Azure portal 

![](.gitbook/assets/image%20%2887%29.png)

### Scenario

You are developing a bot application that can be used with your Microsoft Teams deployment. This lab scenario will get you familiar with deploying Bots for Teams and using the Graph Communications API for real-time media Bots that can join meetings, make calls and process inbound and outbound media streams.



## Exercise 1: Setting up your development environment

### Overview

This lab will require access to an Azure subscription. You can use an existing internal subscription or request an Azure pass for the lab. This bot will use the following Azure components

* Azure Bot Channels Registration
* Azure App Registration
* Azure Key Vault

{% hint style="info" %}
The Bot will utilize the Graph Communications API and requires Tenant Admin consent.
{% endhint %}

Connect to your lab virtual machine here: [https://labondemand.com/LabProfile/x](https://labondemand.com/LabProfile/55694)xx sign on as **xxx** and use password **xxx.** 

### Deploy Cloud App

Logon to your Azure subscription and click create _**Create a Resource**_ search for "Cloud Service"  and click create.

![](.gitbook/assets/image%20%2893%29.png)

Enter **huebotlabxxx** for the dns name

![](.gitbook/assets/image%20%2879%29.png)

### Setup SSL Certificate

Download the teamsbots.com wildcard certificate to your virtual server : [https://1drv.ms/u/s!Al-Ih3130\_Cik7NijkBoAUmwWPuDJQ?e=Eynf86](https://1drv.ms/u/s!Al-Ih3130_Cik7NijkBoAUmwWPuDJQ?e=Eynf86)  

Navigate to the newly deployed cloud services in Azure portal and select certificates and click the Upload menu option

 

![](.gitbook/assets/image%20%2888%29.png)

Browse for the certificate downloaded in the previous step and provide the certificate password: **summerready**

![](.gitbook/assets/image%20%2823%29.png)

Refresh the certificate blade and you should see the imported wildcard certificate

![](.gitbook/assets/image%20%2813%29.png)

Save the certificate thumbprint it will be needed in Exercise 3. The lab uses a wildcard certificate for the domain teamsbots.com   
The Thumbprint is: **1E872674EDE0781ECE8C209C2D9EEC5822D04B77**

![](.gitbook/assets/image%20%2820%29.png)

### **Deploy a Classic Cloud Storage Account**

From Azure portal select Create Resource and select Storage Account

![](.gitbook/assets/image%20%2873%29.png)

From the create storage account blade click the link called "**Choose classic deployment model**"

![](.gitbook/assets/image%20%2825%29.png)

Now update the form with your resource group, use your huebotlabxxx value for the storage name and change the replication to Locally Redundant Storage. Then click Review + Create and click the Create button on the preceding page.

![](.gitbook/assets/image%20%2886%29.png)





