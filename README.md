<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark](https://youtu.be/TaRA-Bq5ixM)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create Resources
- Observe ICMP Traffic
- Observe SSH Traffic
- Observe DNS Traffic
- Observe RDP Traffic

<h2>Actions and Observations</h2>

-Create our Resources-

  
Create a Windows 10 Virtual Machine (VM)

<img src="https://i.imgur.com/lUIGz6v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Create a Linux (Ubuntu) VM

<img src="https://i.imgur.com/m5eJdPk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<br />

-Observe ICMP Traffic-


Within your Windows 10 Virtual Machine, Install Wireshark

<img src="https://i.imgur.com/E0nKKGO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Open Wireshark and filter for ICMP traffic only

<img src="https://i.imgur.com/Ugza9aB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Retrieve the private IP address of the Ubuntu VM

<img src="https://i.imgur.com/cGsjFqF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Attempt to ping it from within the Windows 10 VM

<img src="https://i.imgur.com/1Cr5QPw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

From The Windows 10 VM, open command line or PowerShell and attempt to ping a public website (such as www.google.com) and
observe the traffic in WireShark


<img src="https://i.imgur.com/sOPYGRb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

-Observe SSH Traffic-


Back in Wireshark, filter for SSH traffic only

<img src="https://i.imgur.com/sOPYGRb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
From your Windows 10 VM, “SSH into” your Ubuntu Virtual Machine (via its private IP address)
      
  a. Type commands (username, pwd, etc) into the linux SSH connection and observe SSH traffic spam in WireShark
      
  b. Exit the SSH connection by typing ‘exit’ and pressing [Enter]
  
<img src="https://i.imgur.com/ZvRpDkR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<br />
  
  
-Observe DNS Traffic-
  
Back in Wireshark, filter for DNS traffic only. From your Windows 10 VM within a command line, use nslookup to see what google.com and disney.com’s IP addresses are.

<img src="https://i.imgur.com/MwWoI4R.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
  
-Observe RDP Traffic-

Back in Wireshark, filter for RDP traffic only (tcp.port == 3389)
  
<img src="https://i.imgur.com/CgQGbls.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
  </p>
<p>
<br />
