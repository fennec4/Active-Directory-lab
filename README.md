
<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=windows" />
    <h1 align="center">Active-Directory-lab </h1>
  </a>
</p>

<p align="center"><img src="img/Active Directory lab.png"/></p> 

*Ref 1: Diagram*

## Objective

<p>this lab simulates a real world enterprise network where I set up a whole soc lab to follow along to know more about this lab</p>
<p>you can find here the <a href="https://youtu.be/5OessbOgyEo?si=TgaMxJH3zi4oQWGY">source link</a></p>

### Skills Learned


- Building a domain, managing users, and joining client VMs.
- Deploying Splunk and forwarding logs across multiple operating systems.
- Installing Microsoft Sysmon and configuring Windows audit policies.

### Tools Used


- Oracle VirtualBox.
- OpenSSH.
- Splunk Enterprise & Splunk Universal Forwarder.
- Microsoft Sysmon.

## Steps
### 1/ Planification
<p>in this phase, I created the diagram in <a href="img/Active Directory lab.png">Ref 1</a> to  organize the lab structure, the lab contains 4 virtual machines :</p>
<p align="center"><img src="img/vms.png"/></p>

*Ref 2: virtual machines*

- Ubuntu Server running Splunk Enterprise (SIEM).
- Windows Server 2022 that hosts Active Directory Domain Services.
- Windows 10 Enterprise, a corporate workstation joined to the active directory domain.
- Kali Linux used to conduct target discovery and brute-force attacks.

for the network part I created a virtualbox NAT  network with the IPv4 prefix of `192.168.10.0/24`.
<p>After the conception of the diagram I started building the VMs using VirtualBox Hypervisor <a href="img/vms.png">ref 2</a>.</p>

### 2/ SIEM setup
In this phase, I set up the Ubuntu server with the Splunk SIEM.

- first I attributed the Splunk Server the static IP address `192.168.10.1` as shown in the <a href="img/Splunk server setup.png">ref 3</a>.
<img src="img/Splunk server setup.png"/>

*Ref 3: IP setup*
