<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
Hello! A good ticketing system is at the heart of many jobs in information technology. In this tutorial, I will walk through the prerequisites and installation of the open-source ticketing system osTicket. osTicket is a free and excellent way to learn about user creation, ticket severity, SLAs, and more.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines, Cloud Computing)
- Remote Desktop
- Internet Information Services (IIS)
- MySQL Database

<h2>Operating Systems Used</h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites to Install</h2>

- osTicket
- MySQL
- HeidiSQL
- PHP Manager for IIS
- Rewrite Module for IIS
- Visual C++ Redistributable

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/suJr4nf.png" height="80%" width="80%" alt="Screenshot of Azure's create resource group page"/>
</p>
<p>
First, create a resource group with Azure. The group's name can be anything you like. Click on the button that says "Review + create" then click "Create" on the next screen.
</p>
<br />

<p>
<img src="https://i.imgur.com/QlYhDIl.png" height="80%" width="80%" alt="Screenshot of Azure's virtual machine creation page"/>
</p>
<p>
Create a virtual machine (VM) with Azure. To reach this screen easily, you can type "virtual machines" in the search bar. Click on the button that says "Create" and it will take you to a new page. Fill out the boxes as follows (and everything else can be left at its default). </p>
</p>

<ul>
<li>Resource group: click on the one you created earlier</li>
<li>Virtual machine name: osTicket</li>
<li>Region: choose the closest one to you </li>
<li>Image: Windows 10 Pro, version 21H2 - x64 Gen2</li>
<li>Size: ideally one with 4 vcpus, 16 GiB of memory</li>
<li>Username/password: choose any that you will remember for this project</li>
<li>Licensing: check the box to confirm</li>
</ul>

<p>Click on the button that says "Review + create" then click "Create."</p>
<br />

<p>
<img src="https://i.imgur.com/klw7Dsw.png" height="80%" width="80%" alt="Screenshot of the Azure menu showing details of a virtual machine, including its public IP address"/>
</p>
<p>
Click on the name of your newly created VM to copy its public internet protocol (IP) address.
</p>
<br />

<p>
<img src="https://i.imgur.com/gSjJoRa.png" height="80%" width="80%" alt="Screenshot of the Remote Desktop menu"/>
</p>
<p>
Enter the IP address into the Remote Desktop application along with your previously chosen username and password. If you are using Windows, the Remote Desktop app is already installed. If you are using Mac, you will need to download it from the App Store.
</p>
<br />

<p>
<img src="https://i.imgur.com/j2YhazW.png" height="80%" width="80%" alt="Screenshot showing list of files to install"/>
</p>
<p>
Open Microsoft Edge inside your VM and download the necessary files to run osTicket, listed in the "Prerequisites to Install" section of this tutorial.
</p>
<br />

<p>
<img src="https://i.imgur.com/9p0aEuc.png" height="80%" width="80%" alt="Screenshot showing the Windows Features menu with the checkbox for CGI enabled"/>
</p>
<p>
Enable Internet Information Services (IIS). An easy way is to type "turn Windows features on or off." Check the box for IIS, then expand the dropdown menu and navigate to World Wide Web Services > Application Development Features. Check the box beside CGI.  
</p>
<br />

<p>
<img src="https://i.imgur.com/VlkG7rq.png" height="80%" width="80%" alt="Screenshot showing the installation window of PHP Manager for IIS"/>
</p>
<p>
Click on the installers for PHP Manager for IIS, then the Rewrite Module. They are simple installations so you can click next/agree when prompted.
</p>
<br />

<p>
Next, navigate to the C: drive and create a folder titled PHP. Unzip the contents of PHP (whichever version you downloaded) into the folder. Continue by installing Visual C++ Redistributable, which is also a simple installation.
</p>
<br />

<p>
Click on the installer for MySQL. Configure it as follows:
</p>

<ol>
<li>Choose "Typical Setup"</li>
<li>Check the box for "Launch Configuration Wizard"</li>
<li>Choose "Standard Configuration"</li>
<li>Type a password you will remember</li>
</ol>
<br />

<p>
<img src="https://i.imgur.com/sSJP14o.png" height="80%" width="80%" alt="Screenshot showing the PHP Manager window within IIS"/>
</p>
<p>
Type "IIS" into the search bar and open the program as an administrator (this is required for it to work properly). Register PHP by clicking on "PHP Manager" and navigating to the PHP folder inside C: when prompted, then clicking on php-cgi. Reload IIS so the changes register by clicking stop then start on the Manage Server pane to the right.
</p>
<br />

<p>
<img src="https://i.imgur.com/U4fvcV2.png" height="80%" width="80%" alt="Screenshot of the osTicket website's landing page"/>
</p>
<p>
Extract the archive installaiton file for osTicket into the C:\inetpub\wwwroot location. Rename the "upload" folder to "osTicket" and double-check that it's typed correctly. Any errors will cause it to fail. Stop and start IIS once again.</p>
<br />

<p>
<img src="https://i.imgur.com/U4fvcV2.png" height="80%" width="80%" alt="Screenshot of the osTicket website's landing page"/>
</p>
<p>
Extract the archive installaiton file for osTicket into the C:\inetpub\wwwroot location. Rename the "upload" folder to "osTicket" and double-check that it's typed correctly. Any errors will cause it to fail. Stop and start IIS once again.</p>
<br />

---

➡️ For post-installation setup of osTicket itself (the fun part!) and to learn about configuring users, roles, departments, and SLAs——continue with <a href='https://github.com/hjalmardev/post-install-config'>part two</a> of this tutorial.
