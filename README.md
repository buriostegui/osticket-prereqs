<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Desktop
- Azure Virtual Machine
- osTicket Installation Files
- Heidi SQL

<h2>Installation Steps</h2>

Create a Virtual Machine (VM) on Azure:

- Start by creating a VM on Microsoft Azure with 2-4 CPUs.
- Use a resource group and name it "osTicket" for organization.
![image](https://github.com/buriostegui/osticket-prereqs/assets/148411510/3dac4927-cc2f-47d0-9bc2-a5091e743c7b)

Connect to the VM:
- Access your newly created VM using Remote Desktop Protocol (RDP) and its public IPv4 address.
- Mac users need to download Microsoft RDP for this.

![image](https://github.com/buriostegui/osticket-prereqs/assets/148411510/a4c4233c-ded3-485f-aaef-8b6e6829143f)

Enable IIS (Internet Information Services):

- Open the Control Panel on your VM and select "Uninstall a program."
- In the left-hand menu, choose "Turn Windows features on or off" and enable IIS.

![image](https://github.com/buriostegui/osticket-prereqs/assets/148411510/d6b5a388-7268-4ff6-a967-f58e25893b15)

Install Web Platform Installer:

- Download the necessary files provided via a provided link.
- Install Web Platform Installer by clicking on the link.

![image](https://github.com/buriostegui/osticket-prereqs/assets/148411510/5b2eecdd-4ff7-42eb-85e5-da9beec85a87)

Install MySQL and PHP:
- Open Web Platform Installer and install MySQL 5.5.
- Install the x86 version of PHP, up to version 7.3. Some files might fail, but you can find them through the provided install link.

![image](https://github.com/buriostegui/osticket-prereqs/assets/148411510/6561e7bc-1f14-4948-981f-5c4774b13705)

Download and Set Up osTicket:
- Download osTicket and extract it.
- Copy the "upload" folder to c:\inetpub\wwwroot and rename it to osTicket.

![image](https://github.com/buriostegui/osticket-prereqs/assets/148411510/74c7dcd7-ac63-441c-8a58-ee5a3500346d)

Open IIS Manager and Restart the Server:
- In IIS Manager, go to Sites->Default->osTicket, and click "Browse*.80" to open the osTicket web server.

![image](https://github.com/buriostegui/osticket-prereqs/assets/148411510/a00a5338-51ae-48a9-80ec-60a33db85553)

Enable Extensions in IIS Manager:
- In IIS Manager, go to Sites->Default->osTicket and double click on PHP Manager.
- Enable "php_intl.dll" and "php_opcache.dll."
- Refresh the osTicket web server to observe the changes.

![image](https://github.com/buriostegui/osticket-prereqs/assets/148411510/c84e05c0-78af-4548-94ef-401e3d1babc5)

Continue Setting Up osTicket in the Browser:
- Continue the setup in the browser, naming the Helpdesk as desired.
- Select a default email for receiving customer-submitted tickets.

![image](https://github.com/buriostegui/osticket-prereqs/assets/148411510/a207e1a1-a4c9-4332-914e-cbdd65025fc0)

Finalize osTicket Installation:
- Complete the setup in the browser by providing MySQL database details, MySQL username, and password.
- Click "Install Now!" and hopefully, the installation is error-free.
- Clean up by deleting the setup folder and setting permissions for ost-config.php.
- Access the osTicket Admin Panel (http://localhost/osTicket/scp/login.php).

![image](https://github.com/buriostegui/osticket-prereqs/assets/148411510/b230e62c-3d64-4ad1-bdc5-0ebe5f2ce835)


These steps guide you through setting up osTicket on a virtual machine hosted on Azure and configuring the necessary components for its operation.

