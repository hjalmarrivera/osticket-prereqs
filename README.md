<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
Hello! A good ticketing system is at the heart of many jobs in information technology. In this tutorial, I will walk through the prerequisites and installation of the open-source ticketing system osTicket. osTicket is a free and excellent way to learn about ticket severity, SLAs, assigning users, and more.<br />

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
- Visual Basic

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
Open Microsoft Edge inside your VM and download the necessary files to run osTicket, listed in the "Prerequisites to Install" section of this tutorial. Install them to proceed.
</p>
<br />

---

For post-installation configuration of osTicket itself, continue with <a href='https://github.com/hjalmardev/post-install-config'>part two</a> of this tutorial.
