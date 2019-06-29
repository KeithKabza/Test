# Exercise 6: Configure Azure Unified Speech API

### Configure a new Speech Subscription

Logon to Azure portal and click on Create Resource and enter "Speech" 

![](.gitbook/assets/image%20%2894%29.png)

Now enter the configuration below and click create. 

{% hint style="info" %}
For the name user you **huebotlabxxx** assigned value.
{% endhint %}

![](.gitbook/assets/image%20%2815%29.png)

Once the resource is created navigate to it.

![](.gitbook/assets/image%20%2863%29.png)

Navigate to Keys from the left menu and copy Key 1. We will use it later in the Exercise

![](.gitbook/assets/image%20%2897%29.png)

Now return to your Lab Virtual Machine. We need to update the sources for in the HueBot solution. Under the FrontEnd project open the CallHandler.cs file.

![](.gitbook/assets/image%20%2819%29.png)

We need to update the code with our new Speech API Key on line 84

![](.gitbook/assets/image%20%2865%29.png)

Paste your API Key 1 value from the previous step. If you used the US West data Center when you configured the Speech service you will need to enter uswest as the ServiceRegion. If you are not using US West use the correct value below

| Region | Speech SDK Parameter |
| :--- | :--- |
| West US | westus |
| West US 2 | westus2 |
| East US | eastus |
| East US 2 | eastus2 |

{% hint style="info" %}
You will find a complete list of Service Regions here:  [https://docs.microsoft.com/en-us/azure/cognitive-services/speech-service/regions](https://docs.microsoft.com/en-us/azure/cognitive-services/speech-service/regions)
{% endhint %}

So your updated code should look something like this

![](.gitbook/assets/image%20%2821%29.png)

Save your changes and select the HueBot cloud service project. Right click and select Publish.

![](.gitbook/assets/image%20%2838%29.png)

![](.gitbook/assets/image%20%2827%29.png)

When the publishing wizard appears just click on Publish. If you receive a deployment warning just click replace to overwrite the previous deployment. The update will take approximately 3 minutes. 

![](.gitbook/assets/image%20%2836%29.png)

![](.gitbook/assets/image%20%2866%29.png)

Once the deployment is complete return to you Teams meeting that you joined in a previous Exercise.

![](.gitbook/assets/image%20%2851%29.png)

When you redeployed the Bot solution to Azure cloud service HueBot was dropped from the meeting. Return to postman and send the same HTTP POST command we sent the first time.

![](.gitbook/assets/image%20%2844%29.png)

Now inside the Teams meeting make sure you Microphone is unmuted and you can speak **Red, Green or Blue** and HueBot will change the color of the video stream it is currently sending. 

![](.gitbook/assets/image%20%2817%29.png)

![](.gitbook/assets/image%20%2871%29.png)

![](.gitbook/assets/image%20%2841%29.png)



