# Exercise 2: Registering your Media Bot

### Overview

In this exercise you will register your Bot in Azure active directory and assign the required Graph API permissions. You will also enable the Teams channel and calling features for your Bot. The final step will be to provide tenant admin consent for your Bot application .

### Register The Bot Application

Logon to Azure portal and click the _Create Resource_ menu option.

![](.gitbook/assets/image%20%2816%29.png)

Search for Bot Channels Registration and click the _Create_  button

![](.gitbook/assets/image%20%284%29.png)

Enter the Bot name provided for your lab session **huebotlabxxx**. Select or create a resource group and leave the Messaging endpoint blank for now we will update this later in the lab.

![](.gitbook/assets/image%20%285%29.png)

Click create to complete the registration. Once the Bot registration resource becomes available navigate to the bots settings and copy the Microsoft App ID it will be used in a future exercise.

![](.gitbook/assets/image%20%2811%29.png)

Click the manage link to create a new client secret. Click on the Certificates & Secrets options from the left menu and click the **New client secret** button

![](.gitbook/assets/image%20%287%29.png)

Provide a description and click the **Add** button

![](.gitbook/assets/image%20%2818%29.png)

Copy and save the secret for a future exercise. 

![](.gitbook/assets/image%20%2812%29.png)

Now Select API Permissions form the left menu and click on Add Permissions.

![](.gitbook/assets/image%20%288%29.png)

Click on the **Microsoft Graph** permissions button

![](.gitbook/assets/image.png)

Select Application permissions 

![](.gitbook/assets/image%20%2813%29.png)

Expand the Calls permissions group and check both: 

* **Calls.AccessMedia.All**
* **Calls.JoinGroupCall.All**

![](.gitbook/assets/image%20%2814%29.png)

Back on the API Permissions page click on the Grant Admin Consent button. You must have global administrator permissions for the Azure subscription.

![](.gitbook/assets/image%20%289%29.png)

