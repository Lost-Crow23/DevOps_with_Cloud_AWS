<h1>AMIs (Amazon Machine Image)</h1>

Amazon Machine Image 

<img width="691" alt="AMI diagram" src="https://user-images.githubusercontent.com/126012715/232049937-ebaecaa0-1f4d-4401-8169-6860420ac2e8.png">

Step 1 Creating AMI within AWS:

Previously as we made our instances, we had installed nginx. Create an AMI, we do not have to install 
it manually through a long process, and instead launch it with the AMI.

- Go on the AMI tab under the "ec2"  and create an image under Actions.

<img width="629" alt="Step1 Ami_create_image" src="https://user-images.githubusercontent.com/126012715/232089237-82b6f327-ce36-4afd-bb0c-d1e84be21fbe.png">

Step 2 

<img width="1097" alt="Step2 create image name" src="https://user-images.githubusercontent.com/126012715/232089256-ccf64bb3-9a9b-427b-8bf1-750e23ecbbec.png">

- Convey a name and a description to the image instance. As we created "nginx ami". To illustrate our first testing of our AMI's.

Step 3

<img width="280" alt="step3 click create image" src="https://user-images.githubusercontent.com/126012715/232095288-5c743661-2ce1-44eb-a38d-8536d5bc264a.png">

- Create the image

Step 4

<img width="1207" alt="Step4 Change the name (AMI)" src="https://user-images.githubusercontent.com/126012715/232089271-4dcacd53-30b9-49c5-a2b1-d7cf804d256a.png">

- Click the pencil icon and edit your name to a more suitable, to your AMI name.

Step 5

<img width="1193" alt="Step5 launch instance AMI" src="https://user-images.githubusercontent.com/126012715/232089278-3569338f-9302-479e-a2e1-1c0b9e6434b6.png">

- Launch your instance that you have just created, under the previous instance and use the "launch from AMI".

Step 6

<img width="747" alt="Step6 AMI_catalog" src="https://user-images.githubusercontent.com/126012715/232089285-e2a7d6bc-f3b8-41d1-91b0-b1e8ec331cc4.png">

- Double check if it's under the AMI and select your catalog.

Step 7

<img width="796" alt="Step7 key_pair_AMI" src="https://user-images.githubusercontent.com/126012715/232089338-76e483f8-0fbc-4581-ab94-ba5c5ca7c15d.png">

- Enter your name of the private group for instance "tech221" and fill in the details as normal. 

Step 8

<img width="396" alt="Step8 Launch_finish_ami" src="https://user-images.githubusercontent.com/126012715/232089361-f7a933a0-b79c-4ab4-b1dc-e190d493f086.png">

- Double check the summary and launch the instance.

Step 9

<img width="1199" alt="Step9 back to instances ami" src="https://user-images.githubusercontent.com/126012715/232089376-296e935f-2348-4815-b00f-9903eca323be.png">

- This should track yourself back to the instances.

Step 10 

<img width="1199" alt="Step10 Click connect on ami " src="https://user-images.githubusercontent.com/126012715/232089386-85b80841-339e-4dce-8e18-03694b5ca930.png">

- Click the connect and follow the steps as shown.

- `chmod 400 tech221.pem` 

- `ssh -i "tech221.pem" ubuntu@ec2-34-255-182-176.eu-west-1.compute.amazonaws.com`

Nginx

<img width="304" alt="Ip nginx _ami" src="https://user-images.githubusercontent.com/126012715/232089407-88cd4197-c9d8-4d3a-8084-e54ecfea5ca8.png">

- Enter the IP address shown below onto your browser and this should show.

<img width="852" alt="Nginx " src="https://user-images.githubusercontent.com/126012715/232101056-37fa12ec-0866-49a6-871d-9211ac1a9616.png"



