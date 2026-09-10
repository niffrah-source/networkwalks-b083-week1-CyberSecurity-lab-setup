# Kali Linux Cybersecurity Lab Setup
## Lab Overview
This project documents the setup of a cybersecurity lab environment using Kali Linux and VirtualBox.
The lab environment will be used for hands-on cybersecurity practice, including vulnerability assessment, penetration testing, incident response, digital forensics, and risk assessment so all testing activities can be performed.
## objectives
Set up and configure a Kali Linux virtual machine using VirtualBox.
Configure the virtual machine's hardware and network settings.
Establish and verify network connectivity within the lab environment.
When configuring NAT setup change the name , configure IPv4 address , enable DHCP.
Setup linux on virtualBox and configure and troubleshoot IP connectivity issues.
take snapshot of VM
Build a safe and controlled environment for cybersecurity practice.
## Lab Environment
The lab environment was created using the following setup:
* **Host Operating System:** Windows 11
* **Virtualization Platform:** VirtualBox
* **Guest Operating System:** Kali Linux
* **Network Configuration:** NAT
 ## Important Note
  please make sure to use this lab for systems with permissions.
## Lab Setup
## Step 1 — Installing 7-Zip
Before setting up Kali Linux, 7-Zip was installed to extract the downloaded Kali Linux archive.
(https://www.7-zip.org/)
## Step 2 - Install virtualBox
download virtualBox on your laptop.
virtualBox was installed to manage virtual machine used on kali linux.
https://www.virtualbox.org/
![VirtualBox Setup](Screenshot%202026-09-10%20204227.png)
 ![VirtualBox Setup](Screenshot%202026-09-10%233430.png)

## Step 3 - Configure NAT
configure network settings on virtualbox (create NATNetwork in 10.0.0.0/24)
![VirtualBox Setup](Screenshot%202026-09-10%202338.png)
![VirtualBox Setup](Screenshot%202026-09-10%202408.png)

## Step 4 - Download and import kali linux
 download kali linux through this link:
 https://www.kali.org/get-kali/

 ## Step 5 - setup the IP configuration of kali linux
 The Kali Linux virtual machine was configured to use NAT networking. After configuration, the IP settings were checked to verify network connectivity and troubleshoot any connectivity issues.
 ![VirtualBox Setup](Screenshot%202026-09-10%225456.png)

## step 6 - troubleshoot connectivity issues
* **check if your network settings are correct.
* **Check if you created NATNetwork properly 
* ** Check if all your network settings are correct 
* ** Check that no other VM on the same NAT Network is using 10.0.0.2
 * ** Run below 3 commands & restart your Kali Linux
* **sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0 
* **sudo nmcli connection down "Wired connection 1" 
* **sudo nmcli connection up "Wired connection 1"
* ** Restart your Virtual machines & your main OS.
## Challenges and Troubleshooting
During the lab setup, I encountered a minor network connectivity issue while manually configuring the IPv4 address in Kali Linux. I checked the network configuration and troubleshooting steps to identify the cause of the connectivity issue and successfully established network connectivity.



.
