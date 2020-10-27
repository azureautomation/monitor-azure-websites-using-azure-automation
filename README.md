Monitor Azure Websites using Azure Automation
=============================================

            

This runbook demonstrates how you could monitor websites in your Azure subscription and alert the on call engineer of any issues via text message, as demonstrated in the
[Azure Automation announcement](http://channel9.msdn.com/Events/Build/2014/3-621). It is intended for demonstration purposes only and is not meant for production use (see disclaimer at bottom of this description).






In addition to this runbook, you will need an OrgID credential with access to your Azure subscription    ([http://azure.microsoft.com/blog/2014/08/27/azure-automation-authenticating-to-azure-using-azure-active-directory/](http://azure.microsoft.com/blog/2014/08/27/azure-automation-authenticating-to-azure-using-azure-active-directory/))  
   stored in a credential asset, a Twilio account, and the Twilio PowerShell module.


 


In Azure Automation: 


  *  Import the Twilio module ([https://gallery.technet.microsoft.com/scriptcenter/Twilio-PowerShell-Module-8a8bfef8](https://gallery.technet.microsoft.com/scriptcenter/Twilio-PowerShell-Module-8a8bfef8))

  *  Import this runbook 
  *  Create a connection asset for Twilio, with your Twillio AccountSid and authtoken. These can be obtained on the Twilio website 

  *  Update this runbook to contain the name of your Azure OrgID credential asset, subscription, and Twilio connection asset. 


  *  Start this runbook, providing a value for the OnCallPhone parameter.
   

To cause the runbook to send a text message, stop one of your Azure websites.



**WARNING: This runbook loops continually and never stops. To avoid using up all of your free job execution time, DO NOT LEAVE IT RUNNING!**


**If you want to use this runbook in production scenarios, modify it to only perform a check once, and execute it on a schedule. Or consider modifying it to fit with the monitoring solution described here:   
[http://azure.microsoft.com/blog/2014/11/17/monitoring-azure-services-and-external-systems-with-azure-automation/](http://azure.microsoft.com/blog/2014/11/17/monitoring-azure-services-and-external-systems-with-azure-automation/)**


** **


** **


** **

** **




        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.
