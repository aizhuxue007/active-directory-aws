# Active Directory Basics with AWS
## 1. Launching an EC2 Instance
- Step 1: Sign in to the AWS Management Console and navigate to the EC2 Dashboard.
![Alt text](/path/to/image.png)
- Step 2: Click on Launch Instance and select the Microsoft Windows Server 2019 Base AMI.
- Step 3: Choose a t2.micro instance (eligible for the AWS Free Tier) and click Next: Configure Instance Details.
- Step 4: Leave the default settings and proceed to Add Storage, adjusting if necessary for your lab.
- Step 5: Add Tags as needed, then configure the Security Group to allow RDP access on port 3389. Proceed to review and launch the instance.
- Step 6: Select an existing key pair or create a new one, then launch the instance.
## 2. Connecting to Your Instance
- Step 1: Once the instance is running, navigate to the EC2 Dashboard to find your instance's public DNS or IP.
- Step 2: Use Microsoft Remote Desktop or another RDP client to connect using the instance's public DNS/IP.
## 3. Installing Active Directory Domain Services
- Step 1: Open Server Manager, then select Add roles and features.
- Step 2: Follow the wizard, selecting Active Directory Domain Services when you reach the server roles section.
- Step 3: Complete the wizard and install.
## 4. Promoting the Server to a Domain Controller
- Step 1: In Server Manager, click on the notification flag and select Promote this server to a domain controller.
- Step 2: Choose Add a new forest and enter your desired domain name (e.g., lab.local).
- Step 3: Set a DSRM password, then proceed through the wizard and complete the promotion.
