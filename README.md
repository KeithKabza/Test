# Lab: Developing a Teams Media Bot

During this lab, you will learn how to build and deploy a Microsoft Teams media bot in Office 365 that will you allow your Bot to join a Teams meeting and gain access to the audio and video streams in the meeting. During the lab you will use the Microsoft Teams clients to join meetings and interact with the media bot.  The lab is divided into several exercises that will help you understand how to intelligent media bots that can perform advanced tasks using cognitive services. 

Estimated time to complete: _**50 minutes**_

### Before you begin

The type text feature **\[T\]** used in this lab will send the specific text string to the active window in the virtual machine. Always compare the text in the lab document with the typed text in the virtual machine and verify the expected text shown.

To complete the exercises in this lab, you will need a an O365 Tenant with an enterprise E5 Trial subscription. You can obtain one by registering for the Office Developer Program here [https://developer.microsoft.com/office/profile](https://developer.microsoft.com/office/profile)

Follow the prompts to create a new subscription and complete the required forms. 

![New Office 365 Developer Subscription](.gitbook/assets/image%20%2819%29.png)

Provide your phone number and complete the process by entering the 5 digit code you received via text message. Once complete your subscription will be created!

![](.gitbook/assets/image%20%281%29.png)

You should be able to logon to your subscription now. Now you need to assign some licenses and create a few test users. Using the Office 365 Admin center create at least two test users. Assign one of the provided E3 Licenses to each of your users. 

![](.gitbook/assets/image%20%2827%29.png)

### Scenario

You are developing a bot application that can be used with your Microsoft Teams deployment. This lab scenario will get you familiar with deploying Bots for Teams and using the Graph Communications API for real-time media Bots that can join meetings, make calls and process inbound and outbound media streams.

