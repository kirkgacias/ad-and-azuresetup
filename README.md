<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Building the Foundation: Preliminary Setup for Active Directory and Network Traffic Analysis between Azure VMs</h1>


<p>Welcome to the inaugural project in a comprehensive series of tutorials focused on Azure and Active Directory implementation. This initial project serves as the foundational cornerstone and setup for the subsequent  parts of this tutorial series. The primary objective is to lay the groundwork for a simple lab environment on Azure to simulate the environment in which Active Directory is employed within an enterprise setting.
</p>

<h2>Overview </h2>

<p>In this first project, I will configure and interconnect two virtual machines, each assuming distinct roles. The first virtual machine will be designated as the Domain Controller. The second virtual machine will be configured as the Client.</p>

<h2>Key Objectives</h2>
<h3>Virtual Machine Setup</h3>

-  Configure the Domain Controller virtual machine
-  Establish the Client virtual machine

<h3>Remote Connectivity</h3>

- Enable a connection using remote desktop connection

<h3> Traffic Inspection</h3>

- Undertake a basic inspection of the network traffic between the Domain Controller and Client virtual machines.



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)


<h2>Configuration Steps</h2>

<h3>&#9312; Create the Domain Controller</h3>

- Create a virtual machine on Azure.
- Name it DC-01 
- Select Windows Server 2022: Azure Edition - x64 Gen2 as the image


<p>
<img width="776" alt="VM image" src="https://github.com/kirkgacias/ad-and-azuresetup/assets/158519921/f072cd7b-b547-4006-9ddb-ae6ba39c497e">
</p>
<p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<strong> NOTE: Make sure to select at least 2 vcpus and 16 GiB memory and take note of the vnet that the VM has created.</strong>
</p>
<br />

<p>
<img width="736" alt="DC-vm" src="https://github.com/kirkgacias/ad-and-azuresetup/assets/158519921/323e78b9-4e86-46e3-b021-6ac529ccb600">
</p>
<p>
</p>
<br />
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h3>&#9313; Set the Domain Controller's Private IP to static </h3>

-  Once the VM has been deployed, proceed to the VM overview page and select "Networking" on the left side. 
<img width="692" alt="networking" src="https://github.com/kirkgacias/ad-and-azuresetup/assets/158519921/a35e1aad-57e1-4c1c-9e4e-aefa4fcf31ea">
<br>
<br>
<br>

-  Select Network Interface Card -> IP configurations -> ipconfig1 and set Private IP address allocation to static.

<br>

<p>
<img width="518" alt="static" src="https://github.com/kirkgacias/ad-and-azuresetup/assets/158519921/8629a747-9809-4329-859f-2d38896ec484">
</p>

<br />
