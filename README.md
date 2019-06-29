# Lab: Developing a Teams Media Bot

During this lab, you will learn how to build and deploy a Microsoft Teams media bot in Office 365 that will you allow your Bot to join a Teams meeting and gain access to the audio and video streams in the meeting. During the lab you will use the Microsoft Teams clients to join meetings and interact with the media bot.  The lab is divided into several exercises that will help you understand how to intelligent media bots that can perform advanced tasks using cognitive services. 

Estimated time to complete: _**50 minutes**_

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

