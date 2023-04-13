<h1>AWS - Virtual Linux Environment and connecting the SSH</h1>

Amazon Web Services is on-demand cloud computing platform. It includes services to help build sophisticated applications
with the increased reliability, scalability, flexibility. 

<h3>AWS</h3>

- Deploy steps

Once logged into AWS you'll be prompted to change region, to the closest data center with the most availability.
We have chosen ireland. 
- Once chosen, search "EC2" and choose EC2 

<h3>Launching Instance</h3>

![Launch instance.png](..%2F..%2F..%2FDesktop%2FLaunch%20instance.png)

- Launch instance under the "EC2" tab and click instance to build a virtual environment 

<h3>Editing the instance</h3>

![ubuntu select.png](..%2F..%2F..%2FDesktop%2Fubuntu%20select.png)

- Make a name for your instance and locate the Ubuntu Server 20.04 lts(HMV) 64-bit(x86)

<h3>Network settings and rules</h3>

![Network settings IP.png](..%2F..%2F..%2FDesktop%2FNetwork%20settings%20IP.png)

- Change your IP in your "my IP" and use your personal on the SSH traffic, which means
that it would be only available to yourself and be private so no one can access it.
- The HTTP traffic allows the public to see your web server.

![Network Settings group rules.png](..%2F..%2F..%2FDesktop%2FNetwork%20Settings%20group%20rules.png)

- Make sure the inbound security group rules, are sourced typed correctly, and is within your IP (SSH).

<h3>Key Pair Login</h3>

![Key pair login tech 221.png](..%2F..%2F..%2FDesktop%2FKey%20pair%20login%20tech%20221.png)

- Select "tech221.pem" (SSH key) on the drop-down menu.
- View summary and "launch instance" once all confirmed

<h3>Connecting the instance</h3>

![Success instance.png](..%2F..%2F..%2FDesktop%2FSuccess%20instance.png)

- Once successful, click the link to divert you to the instance

![Connect the instance.png](..%2F..%2F..%2FDesktop%2FConnect%20the%20instance.png)

- Find your instance and check the "instant state" to start and wait to see if it's running
- Click the box to "connect" the instance 

<h3>Connect to instance</h3>

![New Connect Instance.png](..%2F..%2F..%2FDesktop%2FNew%20Connect%20Instance.png)

- Click the SSH client tab and follow the steps shown in the ID.

![Connection terminal part 1.png](..%2F..%2F..%2FDesktop%2FConnection%20terminal%20part%201.png)

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