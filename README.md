# Active Directory Basics Setup with AWS

## 1. Launching an EC2 Instance

- Step 1: Sign in to the `AWS Management Console` and navigate to the `EC2 Dashboard`.

  <img width="800" alt="AWS Management Console" src="https://github.com/aizhuxue007/active-directory-aws/assets/17282458/6b9be881-f33a-4526-bfff-50354397853e">

  
- Step 2: Click on `Launch Instance` and select the `Microsoft Windows Server 2019 Base`.
  
  <img width="800" alt="Launch an EC2 instance" src="https://github.com/aizhuxue007/active-directory-aws/assets/17282458/d5964c7a-0a44-4faa-8477-b17db628cffd">

  
- Step 3: Choose a `t2.micro instance` (eligible for the AWS Free Tier)
  
  <img width="800" alt="choosing t2.micro free tier" src="https://github.com/aizhuxue007/active-directory-aws/assets/17282458/8f0e0b39-d4c2-4adf-8445-ead364acfc77">

  
- Step 4: Add a `key pair name `to securely receive user password to remotely connect to server.
  
  <img width="800" alt="Creating a key value pair to receive passwords on your computer for remote connection" src="https://github.com/aizhuxue007/active-directory-aws/assets/17282458/a5b60248-6e94-49fc-bf39-0440720c4bff">

  
- Step 5: Verify that `Allow RDP traffic from` checkbox is checked
  
  <img width="800" alt="allow RDP traffic" src="https://github.com/aizhuxue007/active-directory-aws/assets/17282458/d43a7f8c-694e-47c2-9cd0-12534d117e89">

  
- Step 6: Click the orange `Launch instance` button.
  
  <img width="800" alt="instance successfully created notification" src="https://github.com/aizhuxue007/active-directory-aws/assets/17282458/88c8a375-13bf-45b7-87c1-1374377096ea">


## 2. Connecting to Your Instance
- Step 1: Once the instance is running, navigate to the `EC2 Dashboard` to find your instance's public `DNS` or `IP`.
  
  <img width="800" alt="Finding public domain name server" src="https://github.com/aizhuxue007/active-directory-aws/assets/17282458/f219a07d-51a8-4d8c-9a6f-d35430494d77">

  
- Step 2: Use `Microsoft Remote Desktop` or another RDP client to connect using the instance's public DNS/IP.
  
  <img width="800" alt="microsoft remote desktop" src="https://github.com/aizhuxue007/active-directory-aws/assets/17282458/9d487614-8e56-4760-b1c0-73539c8390f4">
  
  Note if you forgot the login info, head to `EC2 Dashboard`, click `Actions`, `Security` and `Get Windows Password`. Drag the `key pair name file` to the prompt to receive username and password.
  
## 3. Installing Active Directory Domain Services

- Step 1: Open `Server Manager`, then select `Add roles and features`.

  <img width="800" alt="window server app" src="https://github.com/aizhuxue007/active-directory-aws/assets/17282458/27235c87-7629-4ae1-98ea-43ced936a9d8">
  
- Step 2: Follow the wizard, selecting `Active Directory Domain Services` when you reach the server roles section.

<img width="800" alt="adding Active Directory Domain Services to roles and features" src="https://github.com/aizhuxue007/active-directory-aws/assets/17282458/e4118c2f-1950-48a2-bd25-924300ac5fad">

- Step 3: Complete the wizard and install.

<img width="800" alt="finish installing Active Directory Services" src="https://github.com/aizhuxue007/active-directory-aws/assets/17282458/70a894a1-eb03-41d9-99b5-cff3f75c8f59">


## 4. Promoting the Server to a Domain Controller

- Step 1: In Server Manager, click on the notification flag and select Promote this server to a domain controller.
  
  <img width="800" alt="promote to domain controller" src="https://github.com/aizhuxue007/active-directory-aws/assets/17282458/5e7b2460-b21e-4189-9267-35e6d10bd5be">

  
- Step 2: Choose Add a new forest and enter your desired domain name (e.g., lab.local).

<img width="800" alt="add new forest and domain name" src="https://github.com/aizhuxue007/active-directory-aws/assets/17282458/5defc48e-ab22-4aaf-8eda-681d5c070574">

- Step 3: Set a DSRM password

<img width="800" alt="Directory service restore mode password setup" src="https://github.com/aizhuxue007/active-directory-aws/assets/17282458/2b61aeae-4985-49ba-ac96-65f88c3f451b">

- Step 4: Proceed through the wizard and complete the promotion.
  
<img width="800" alt="continuing  promoting domain controller wizard" src="https://github.com/aizhuxue007/active-directory-aws/assets/17282458/437cfdfb-0af4-4ced-92a9-d473bbf1eed9">
