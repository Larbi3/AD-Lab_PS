# ActiveDirectoryLab

In this lab, the primary goal is to establish an Active Directory environment within VMware, including the bulk creation of users. The following section provides a visual representation of the processes, accompanied by detailed step-by-step instructions outlining each stage of the setup.

![image1](https://github.com/Larbi3/AD-Lab_PS/assets/133678071/7389b853-116d-468a-b582-d692f362a51c)


**Step 1: Preparations**

- Download and install Oracle VirtualBox on your computer.
- Obtain Windows 10 and Server 2019 ISO files.

**Step 2: Domain Controller Setup**

1. Create a new virtual machine (VM) which will act as your domain controller in VirtualBox.
2. Configure two network adapters: one for external internet connection and the other for the internal VirtualBox private network for clients to connect to.
3. Install Server 2019 on the domain controller VM.
4. Assign the IP addressing for internal network; external network obtains an IP automatically from your home router.
5. Install Active Directory and DNS on the domain controller.
6. Name the server and configure RAS/NAT routing for private network clients to access the internet through the domain controller.
7. Set up DHCP on the domain controller for automatic IP assignment for clients on the private network.
8. Run the PowerShell script that will automate the create 1000 users in Active Directory.

**Step 3: Client Machine Setup**

1. Create another VM and install Windows 10
2. Connect it to the private VirtualBox network.
3. Join the machine to the domain after naming it Client 1.
4. Log into the client machine using a domain account.

**Troubleshooting:**

- If network issues arise, check the network adapter configurations on both domain controller and client machines.
- Ensure proper DNS and DHCP settings.
- Troubleshoot IP configuration issues using ipconfig and renew IP if needed.

**Additional Tips:**

- Utilize the provided PowerShell script to automate user creation in Active Directory.
- Practice the setup process multiple times to build confidence and familiarity.
- Pay attention to network adapter configurations, IP addressing, and DNS settings for seamless communication between domain controller and client machines.







*All thanks and credit for this lab goes to Josh Madakor*


