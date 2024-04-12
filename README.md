# Vulnerability Scanner Set Up + Virutal Machine



## Intro
In this project, I will be doing a Vulnerability Management technical lab in the cloud. I will create a vulnerability management server using OpenVAS inside a virutal machine. Then I will create a 2nd virtual machine in the same network where I will download insecure software.  Then scans will be performed with OpenVAS to detect the vulnerabilites. After which, I will employ remediations. This will alo be done with Microsoft Azure.

To begin, I signed into my Azure account. To prepare the vulnerability management scanner, I need the server virtual machine that has the OpenVas software on it. I went to the Azure portal and entered "OpenVAS". I clicked "Start with a pre-set configuration"

![VL 1](https://github.com/Ashrafs-Tech/Scanner-and-VM/assets/166546026/54df602d-9d40-4f2b-b468-8623bff93e04)

![VL 2](https://github.com/Ashrafs-Tech/Scanner-and-VM/assets/166546026/09dbd0b0-9400-4778-9aec-40e5a2b72091)


After picked the defualt settings, I configured the virtual machine that will be running the vulnerability management software. 
- I called the Resource Group "Vulnerability-Management"
- I named the virtual machine "OpenVAS"
- For authentication type, I picked password.
- I created my own username and password. 

![VL 3](https://github.com/Ashrafs-Tech/Scanner-and-VM/assets/166546026/c8404d39-1b95-4eeb-aa3f-12fc8ab67b27)

![VL 4](https://github.com/Ashrafs-Tech/Scanner-and-VM/assets/166546026/0ee58b2c-d6b8-4ec3-aed2-de6933fe5a46)




Then I clicked the "Review and Create" button and after some waitng, the virutal machine will be deployed. 
![VL 5](https://github.com/Ashrafs-Tech/Scanner-and-VM/assets/166546026/c245f9e1-6752-4084-8e8c-4730cbc23a1c)





After it was complete, I will ssh(a way to connect and manage Linux machines) into it with Powershell(since I'm using Windows).
- In order to ssh into it, I have to copy the public IP address of the virutal machine I just created. 
- Then in Powershell, will enter ssh azureuser@74.249.93.61. 
- Then Powershell will ask if you want to continue connecting and I responded "yes"
- After that, I will enter the password into Powershell.

![VL 6](https://github.com/Ashrafs-Tech/Scanner-and-VM/assets/166546026/679e1fbf-9ca1-45c0-b6df-9d46085bbb77)

  

Doing this will generate the following
- A username: admit
- A password: 2de16a5d-9b6f-4cd9-90d4-6e5a5e740e21
- A URL https://74.249.93.61.c.hossted.app

![VL 7](https://github.com/Ashrafs-Tech/Scanner-and-VM/assets/166546026/6be35288-c920-492e-9cd7-7a2b0acefeb5)


Next I will enter the URL in the computer search bar and enter the username and password that was generated.  The website that open's up is Greenbone.

![VL 8](https://github.com/Ashrafs-Tech/Scanner-and-VM/assets/166546026/fcafac91-803d-47b1-aff3-8e318187f0ac)


After logging into the Greenbone account, I had to change the generated password because it was too long. 

![VL 9](https://github.com/Ashrafs-Tech/Scanner-and-VM/assets/166546026/3929edbb-5146-4cb5-937b-27752cc41a33)


## Step 1 is done.  The Virtual Machine for the OpenVAS vulnerability management has been created.  
