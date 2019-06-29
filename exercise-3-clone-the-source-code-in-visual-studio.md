# Exercise 3: Clone the source code in Visual Studio

The lab sample is hosted in Azure DevOps and you will need to use your @microsoft.com ID to access the code base. From your lab virtual machine open Visual Studio 2019. Click on the Team Explorer Tab and click on the green plug icon on the top menu. Click on **Clone**

![](.gitbook/assets/image%20%2891%29.png)

Paste the following Repo URL into the text box: [https://vsogd.visualstudio.com/ServicesCode-Assets/\_git/BP-HueBotClouldServiceVersion](https://vsogd.visualstudio.com/ServicesCode-Assets/_git/BP-HueBotClouldServiceVersion) and click the Clone button.

![](.gitbook/assets/image%20%2818%29.png)

If prompted for credentials use your Microsoft corp account.  
Now expand the Local Media Samples folder and double click on HueBot.sln

![](.gitbook/assets/image%20%2824%29.png)

If you are prompted to download .NET Framework 4.6.2 select the download option and click OK. You may receive this prompt a second time select the download option. 

![](.gitbook/assets/image%20%2839%29.png)

Scroll down to the .NET Framework section and download the Developer Pack for version 4.6.2

![](.gitbook/assets/image%20%2850%29.png)

Select to Run the installation

![](.gitbook/assets/image%20%283%29.png)

![](.gitbook/assets/image%20%2811%29.png)

Once the .NET 4.6.2 Framework is installed close Visual Studio and reopen the HueBot.sln   
Expand the WorkerRole project and open the app.config file. Scroll down until you see the appSettings section.

![](.gitbook/assets/image%20%2843%29.png)

Update the values you saved from Exercise two. The BotID will be your Bot names used when you Registered the Bot Channel.

![](.gitbook/assets/image%20%2826%29.png)

Now save your changes and expand the HueBot Cloud Service project in Solution Explorer. Open the file **ServiceConfiguration.Clouc.cscfg** file. Scroll down to the ConfigurationSetting section

![](.gitbook/assets/image%20%2885%29.png)

Update the ServiceDnsName replace the xx with your hubotlabxxx value.  
Now update the ServiceName replace the xx with your huebotlabxx value  
Now update the DefaultCertificate replace the &lt;Paste Thumbprint&gt; with the certificate thumbprint you saved in Exercise 1.

![](.gitbook/assets/image%20%2840%29.png)

Save your changes!



