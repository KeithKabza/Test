# LAB FIXES

* Publish the source code to my Github so there is one less step and free up some time. 
  * UPDATE Exercise 3 and the URL needed
* Fix the source code in ServiceConfiguration.Cloud.cscfg file. There are two invalid certificate thumbprints that need to be updated. Just replace abc123 with this string  **&lt;Paste Thumbprint&gt;** on LINE 20 & LINE 23 and check in the code update.
  * DELETE the Certificate settings in the  ServiceConfiguration.Local.cscfg They caused a problem for me when trying to publish. They are not needed for the lab.
* .NET 4.6.2 is not installed on the LearnOnDemand Virtual Machine Image is there anyway to get the image updated to save some time?

