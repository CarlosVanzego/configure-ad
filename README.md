<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1
- Step 2
- Step 3
- Step 4

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To begin, you need to set up an Azure Virtual Network (VNet) that will serve as the networking foundation for your Azure resources. Within the VNet, create a virtual machine (VM) using the Azure portal or Azure PowerShell. Ensure that the VM meets the necessary requirements for Active Directory, such as having adequate compute resources and being connected to the VNet.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once the VM is up and running, you can proceed with installing Active Directory Domain Services (AD DS). This involves promoting the VM to a domain controller by configuring it as an AD DS server. Use the Server Manager or PowerShell to install the Active Directory Domain Services role and follow the prompts to complete the installation. Specify a domain name and provide necessary credentials for the Active Directory forest and domain.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
With Active Directory installed, you can now configure the necessary DNS settings. Open the DNS Manager and create a forward lookup zone for your domain. Configure the DNS server to use itself as the primary DNS server, ensuring proper name resolution within the domain. Additionally, configure the VM's network adapter settings to point to the AD DS server as the preferred DNS server.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lastly, you need to join your other Azure VMs to the Active Directory domain. Access each VM's network settings and specify the AD DS server as the preferred DNS server. Join each VM to the domain by right-clicking on "This PC" (formerly "My Computer"), selecting "Properties," and navigating to the "Computer Name" tab. Click on "Change" and provide the domain name and appropriate credentials. Reboot the VMs, and they will be joined to the Active Directory domain, enabling centralized authentication and access control.
</p>
<br />

By following these four paragraphs of steps, you can successfully configure Active Directory within Azure VMs
