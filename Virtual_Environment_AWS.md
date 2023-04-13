<h1>AWS - Virtual Linux Environment and connecting the SSH</h1>

Amazon Web Services is on-demand cloud computing platform. It includes services to help build sophisticated applications
with the increased reliability, scalability, flexibility. 

<h3>AWS</h3>

- Deploy steps

Once logged into AWS you'll be prompted to change region, to the closest data center with the most availability.
We have chosen ireland. 
- Once chosen, search "EC2" and choose EC2 

<h3>Launching Instance</h3>

<img width="426" alt="Launch instance" src="https://user-images.githubusercontent.com/126012715/231855752-bbb5f22d-cb71-42c6-94b6-5347c8b50f13.png">

- Launch instance under the "EC2" tab and click instance to build a virtual environment 

<h3>Editing the instance</h3>

<img width="1017" alt="ubuntu select" src="https://user-images.githubusercontent.com/126012715/231855952-15873d1b-d79d-46db-9f68-241ac46e7b64.png">

- Make a name for your instance and locate the Ubuntu Server 20.04 lts(HMV) 64-bit(x86)

<h3>Network settings and rules</h3>

<img width="690" alt="Network settings IP" src="https://user-images.githubusercontent.com/126012715/231856030-08837334-c157-43de-a61d-0c2716222b9a.png">

- Change your IP in your "my IP" and use your personal on the SSH traffic, which means
that it would be only available to yourself and be private so no one can access it.
- The HTTP traffic allows the public to see your web server.

![Uploading Network Settings group rules.png…]()

- Make sure the inbound security group rules, are sourced typed correctly, and is within your IP (SSH).

<h3>Key Pair Login</h3>

<img width="813" alt="Key pair login tech 221" src="https://user-images.githubusercontent.com/126012715/231856176-f14caac1-5c9e-4105-b982-60f5dc04f1d2.png">

- Select "tech221.pem" (SSH key) on the drop-down menu.
- View summary and "launch instance" once all confirmed

<h3>Connecting the instance</h3>

<img width="631" alt="Success instance" src="https://user-images.githubusercontent.com/126012715/231856627-3bd66ea4-a1ee-412b-b995-d06f46c748f5.png">

- Once successful, click the link to divert you to the instance

<img width="1189" alt="Connect the instance" src="https://user-images.githubusercontent.com/126012715/231856658-c4e00bc8-9c33-48f4-8d63-623f3f1bb9da.png">

- Find your instance and check the "instant state" to start and wait to see if it's running
- Click the box to "connect" the instance 

<h3>Connect to instance</h3>

<img width="835" alt="New Connect Instance" src="https://user-images.githubusercontent.com/126012715/231856783-09810e43-b133-47e3-8a59-cea1a01a89cd.png">

- Click the SSH client tab and follow the steps shown in the ID.

![Uploading Connection terminal part 1.png…]()

- Open git bash terminal and open the .ssh directory and connect using its public DNS.
- 
  - Use and enter the commands

        chmod 400 tech221.pem


        ssh -i "tech221.pem" ubuntu@ec2-52-50-69-251.eu-west-1.compute.amazonaws.com`
  
- Enter the Public DNS provided by AWS 
- Enter "yes" when prompted 

You are now connected to Linux 

<h2>Editing Security Groups</h2>

- Select "Security Tab" on the instances summary window
- click the Security Groups code link
- Select Actions and pick to "Edit inbound rules"
- Now add rule under the "source type" as "SSH" and choose "My IP" and save
