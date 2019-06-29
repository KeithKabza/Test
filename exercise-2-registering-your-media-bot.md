# Exercise 2: Registering your Media Bot

### Overview

In this exercise you will register your Bot in Azure active directory and assign the required Graph API permissions. You will also enable the Teams channel and calling features for your Bot. The final step will be to provide tenant admin consent for your Bot application .

### Register The Bot Application

Logon to Azure portal and click the _Create Resource_ menu option.

![](.gitbook/assets/image%20%2872%29.png)

Search for Bot Channels Registration and click the _Create_  button

![](.gitbook/assets/image%20%2814%29.png)

Enter the Bot name provided for your lab session **huebotlabxxx**. Select or create a resource group and leave the Messaging endpoint blank for now we will update this later in the lab. You will need to create a resource group for the lab we used one called HueBot.

![](.gitbook/assets/image%20%2822%29.png)

Note is you receive this error set application insights to **OFF**

![](.gitbook/assets/image%20%2877%29.png)

Click create to complete the registration. Once the Bot registration resource becomes available navigate to the bots settings and copy the Microsoft App ID it will be used in a future exercise.

### Configure the Microsoft Teams Channel

Now click on the Channels menu option to configure your bot to work with Microsoft Teams.

![](.gitbook/assets/image%20%2884%29.png)

Now click on the Teams Icon

![](.gitbook/assets/image%20%2832%29.png)

No click on the Teams calling tab. Check the box to enable calling and enter the webhook URL. Use your huebotlabxxx value ****for example**:**   **https://huebotlabxxx.teamsbots.com/api/call** click the save button when finished**.** You must agree to the Terms of Service when prompted.

![](.gitbook/assets/image%20%2855%29.png)

### Collect the App Id and create a new Secret

Navigate to the new Bot registration and select the settings menu option from the left menu. Copy the Microsoft App Id and save this for later in Exercise 3.

![](.gitbook/assets/image%20%2853%29.png)

Once you have saved your App Id click the Manage link to create a new client secret. Click on the Certificates & Secrets options from the left menu and click the **New client secret** button

![](.gitbook/assets/image%20%2831%29.png)

Provide a description for your new secret and click the **Add** button

![](.gitbook/assets/image%20%2876%29.png)

Copy and save the newly generated secret for later in Exercise 3.

![](.gitbook/assets/image%20%2854%29.png)

Now Select API Permissions form the left menu and click on Add Permissions.

![](.gitbook/assets/image%20%2837%29.png)

Click on the **Microsoft Graph** permissions button

![](.gitbook/assets/image%20%286%29.png)

Select Application permissions 

![](.gitbook/assets/image%20%2860%29.png)

Expand the Calls permissions group and check the following: 

* **Calls.AccessMedia.All**
* **Calls.JoinGroupCall.All**

![](.gitbook/assets/image%20%2862%29.png)

Back on the API Permissions page click on the Grant Admin Consent button. You must have global administrator permissions for the Azure subscription.

![](.gitbook/assets/image%20%2847%29.png)

### 



