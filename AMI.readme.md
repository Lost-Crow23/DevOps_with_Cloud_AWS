<h1>AMIs (Amazon Machine Image)</h1>

<h3>Amazon Machine Image</h3>

<img width="691" alt="AMI diagram" src="https://user-images.githubusercontent.com/126012715/232049937-ebaecaa0-1f4d-4401-8169-6860420ac2e8.png">

The Architecture diagram shows the overall deployment architecture with the data flow, ec2 image builder and the ec2 console with AMI.

<h4>Step 1</h4>

Creating AMI within AWS:

Previously as we made our instances, we had installed nginx. Create an AMI, we do not have to install it manually through a long process, and instead launch it with the AMI.

- Go on the AMI tab under the "ec2"  and create an image under Actions.

<img width="629" alt="Step1 Ami_create_image" src="https://user-images.githubusercontent.com/126012715/232089237-82b6f327-ce36-4afd-bb0c-d1e84be21fbe.png">

<h4>Step 2 </h4>

<img width="1097" alt="Step2 create image name" src="https://user-images.githubusercontent.com/126012715/232089256-ccf64bb3-9a9b-427b-8bf1-750e23ecbbec.png">

- Convey a name and a description to the image instance. As we created "nginx ami". To illustrate our first testing of our AMI's.

<h4>Step 3</h4>

<img width="280" alt="step3 click create image" src="https://user-images.githubusercontent.com/126012715/232095288-5c743661-2ce1-44eb-a38d-8536d5bc264a.png">

- Create the image

<h4>Step 4</h4>

<img width="1207" alt="Step4 Change the name (AMI)" src="https://user-images.githubusercontent.com/126012715/232089271-4dcacd53-30b9-49c5-a2b1-d7cf804d256a.png">

- Click the pencil icon and edit your name to a more suitable, to your AMI name.

<h4>Step 5</h4>

<img width="1193" alt="Step5 launch instance AMI" src="https://user-images.githubusercontent.com/126012715/232089278-3569338f-9302-479e-a2e1-1c0b9e6434b6.png">

- Launch your instance that you have just created, under the previous instance and use the "launch from AMI".

<h4>Step 6</h4>

<img width="747" alt="Step6 AMI_catalog" src="https://user-images.githubusercontent.com/126012715/232089285-e2a7d6bc-f3b8-41d1-91b0-b1e8ec331cc4.png">

- Double check if it's under the AMI and select your catalog.

<h4>Step 7</h4>

<img width="796" alt="Step7 key_pair_AMI" src="https://user-images.githubusercontent.com/126012715/232089338-76e483f8-0fbc-4581-ab94-ba5c5ca7c15d.png">

- Enter your name of the private group for instance "tech221" and fill in the details as normal. 

<h4>Step 8</h4>

<img width="396" alt="Step8 Launch_finish_ami" src="https://user-images.githubusercontent.com/126012715/232089361-f7a933a0-b79c-4ab4-b1dc-e190d493f086.png">

- Double check the summary and launch the instance.

<h4>Step 9</h4>

<img width="1199" alt="Step9 back to instances ami" src="https://user-images.githubusercontent.com/126012715/232089376-296e935f-2348-4815-b00f-9903eca323be.png">

- This should track yourself back to the instances.

<h4>Step 10</h4>

<img width="1199" alt="Step10 Click connect on ami " src="https://user-images.githubusercontent.com/126012715/232089386-85b80841-339e-4dce-8e18-03694b5ca930.png">

- Click the connect and follow the steps as shown.

- `chmod 400 tech221.pem` 

- `ssh -i "tech221.pem" ubuntu@ec2-34-255-182-176.eu-west-1.compute.amazonaws.com`

<h4>Nginx</h4>

<img width="304" alt="Ip nginx _ami" src="https://user-images.githubusercontent.com/126012715/232089407-88cd4197-c9d8-4d3a-8084-e54ecfea5ca8.png">

- Enter the IP address shown below onto your browser and this should show.


<img width="857" alt="AMI Nginx" src="https://user-images.githubusercontent.com/126012715/232103029-1282ff1a-5317-4b86-9a45-ddb9c597fc65.png">

<h1>Launching Nginx Via User-data</h1>

<h4>Step 1</h4>

- As before, we Launch Instance and we create a name to our AMI.
- Making sure we select Ubunto 20.04 as a our catalogue instead of our previous AMI.

<img width="1241" alt="user data launch instance" src="https://user-images.githubusercontent.com/126012715/232109865-ff5d5c1d-1aaa-42f0-98a9-64a2bbfa1363.png">

<h4>Step 2</h4>

<img width="804" alt="Select Security group" src="https://user-images.githubusercontent.com/126012715/232110805-aa8e2c39-d84e-42c5-be71-b0a384253227.png">

- Now as before, we select our existing security group, to assign ourself to our group. 

<h4>Step 3</h4>

<img width="755" alt="step 2- Advance details user data" src="https://user-images.githubusercontent.com/126012715/232113316-394f2fa8-77b7-437e-843d-c5ea2fbb328e.png">

- Scroll down the catalogue to the Advanced Settings and you should see a range of information. 

<h4>Final Iteration</h4>

- Stop at the user data and input the corresponding bash script commands to apply the Nginx. 

`#!/bin/bash`

`sudo apt update -y`

`sudo apt upgrade -y`

`sudo apt install nginx -y`

`sudo systemctl restart nginx`

`sudo systemctl enable nginx`

<img width="1232" alt="User data" src="https://user-images.githubusercontent.com/126012715/232113862-a7bf6bbd-207f-4df6-91ad-b41faa460a03.png">

- We input the ssh key to our terminal "git/bash" `ssh -i "tech221.pem" ubuntu@ec2-34-255-182-176.eu-west-1.compute.amazonaws.com`. Making sure we 
change our "root" to "ubuntu"

<img width="586" alt="Change to ubuntu" src="https://user-images.githubusercontent.com/126012715/232123551-105fa0f3-723f-429a-868a-567c0fc38e43.png">

- Now, use the IP address within the details section, for Nginx.

<img width="904" alt="Nginx-user-data" src="https://user-images.githubusercontent.com/126012715/232114676-3c82b75e-d50e-4363-8c09-f27afbffe2b1.png">





