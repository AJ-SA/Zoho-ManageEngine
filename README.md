# Zoho ManageEngine Local Privilege Escalation
* **Reference:** https://www.manageengine.com/products/desktop-central/elevation-of-system-privilege.html
* **CVEs:** CVE-2018-13411, CVE-2018-13412
* **Application:** Desktop Central Agent, Self Service Portal Desktop Central
* **Notification Date:** July 5, 2018

#### What was the Problem?
Unauthorized users, whose computer is installed with Desktop Central Agent were able to access command prompt with SYSTEM privilege.

#### Effected Products:

* Desktop Central Version less than < 10.0.282

#### How do I fix it?
This has been identified and fixed on Aug 23, 2018. To apply this fix, follow the below steps:

* Log in to your Desktop Central console, click on your current build number on the top right corner.
* You can find the latest build applicable to you. Download the PPM and update.

#### Exploit:

In most ManageEngine windows that runs as system, you can also get Self Service Portal Desktop Central window running as system by executing this command: `C:\Program Files (x86)\DesktopCentral_Agent\bin\dcagenttrayicon.exe" -ssp`. When getting the window, there is a comment "Powered by Managed Engine Desktop Central" and it has ManageEngine logo. By clicking on the logo, it will open the link in a web browser which then runs as SYSTEM as well. To abuse these vulnerabilities, you can open a CMD.exe or PowerShell.exe from the browser.
