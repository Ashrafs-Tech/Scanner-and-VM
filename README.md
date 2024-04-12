# Vulnerability Scanner Set Up + Virutal Machine

![image](https://github.com/Ashraf-In-Tech/Preparing-the-Scanner/assets/165876025/67864846-04fb-47aa-aa39-b46541175851)

## Intro
In this project, I will be doing a Vulnerability Management technical lab in the cloud. I will create a vulnerability management server using OpenVAS inside a virutal machine. Then I will create a 2nd virtual machine in the same network where I will download insecure software.  Then scans will be performed with OpenVAS to detect the vulnerabilites. After which, I will employ remediations. This will alo be done with Microsoft Azure.

To begin, I signed into my Azure account. To prepare the vulnerability management scanner, I need the server virtual machine that has the OpenVas software on it. I went to the Azure portal and entered "OpenVAS". I clicked "Start with a pre-set configuration"

![VL 1](https://github.com/Ashraf-In-Tech/Preparing-the-Scanner/assets/165876025/99fe1540-e2a5-43fd-af9f-c0dd91fee329)

After picked the defualt settings, I configured the virtual machine that will be running the vulnerability management software. 
- I called the Resource Group "Vulnerability-Management"
- I named the virtual machine "OpenVAS"
- For authentication type, I picked password.
- I created my own username and password. 

![VL 3](https://github.com/Ashraf-In-Tech/Preparing-the-Scanner/assets/165876025/9c962489-40c4-463d-864a-02378c4e273e)
![VL 4](https://github.com/Ashraf-In-Tech/Preparing-the-Scanner/assets/165876025/f79f75bd-43a6-4059-a57c-bce41a09814b)




Then I clicked the "Review and Create" button and after some waitng, the virutal machine will be deployed. 
![VL 5](https://github.com/Ashraf-In-Tech/Preparing-the-Scanner/assets/165876025/1606bce1-0bcc-49cf-b3d4-1b29705d0d8d)




After it was complete, I will ssh(a way to connect and manage Linux machines) into it with Powershell(since I'm using Windows).
- In order to ssh into it, I have to copy the public IP address of the virutal machine I just created. 
- Then in Powershell, will enter ssh azureuser@74.249.93.61. 
- Then Powershell will ask if you want to continue connecting and I responded "yes"
- After that, I will enter the password into Powershell.

![VL 6](https://github.com/Ashraf-In-Tech/Preparing-the-Scanner/assets/165876025/4dea5d3f-b52b-46c7-bcad-d923ce85675a)
  

Doing this will generate the following
- A username: admit
- A password: 2de16a5d-9b6f-4cd9-90d4-6e5a5e740e21
- A URL https://74.249.93.61.c.hossted.app

![VL 7](https://github.com/Ashraf-In-Tech/Preparing-the-Scanner/assets/165876025/6bdd8970-5a9c-4148-8b49-8b37adc08d56)

Next I will enter the URL in the computer search bar and enter the username and password that was generated.  The website that open's up is Greenbone.

![VL 8](https://github.com/Ashraf-In-Tech/Preparing-the-Scanner/assets/165876025/b7928cc0-1f21-437d-b07c-96bb5b529719)

After logging into the Greenbone account, I had to change the generated password because it was too long. 

![VL 9](https://github.com/Ashraf-In-Tech/Preparing-the-Scanner/assets/165876025/cd0a0c1a-328b-4a0c-9944-ce624a694ad6)


## Step 1 is done.  The Virtual Machine for the OpenVAS vulnerability management has been created.  
