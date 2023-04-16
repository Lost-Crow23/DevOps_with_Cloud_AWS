<h1>AWS Security Group </h1>

These are the steps to create a new SSH key instance, through the EC2 dashboard.

<h3>Step 1</h3>

We click the instances under the instances tab and click your name. 

<img width="1213" alt="step 1" src="https://user-images.githubusercontent.com/126012715/231765654-37e8e61f-b1e0-46e2-9f9d-589d5f788b9f.png">


<h3>Step 2</h3>

Click the security tab to open up the security group.

<img width="1213" alt="step 2" src="https://user-images.githubusercontent.com/126012715/231765716-eb436e70-fc0e-464b-833f-6e7f0736b376.png">


<h3>Step 3</h3>

Once opened, you need to edit the inbound to create a ssh security group.

<img width="1160" alt="step 3" src="https://user-images.githubusercontent.com/126012715/231765743-22234ce0-91fc-4ef7-9e52-ae0f858a1299.png">


<h3>Step 4</h3>

Edit your inbound to add a rule thus creating your SSH security file. And under custom, select your personal 
IP address.

<img width="1372" alt="step 4" src="https://user-images.githubusercontent.com/126012715/231766149-bc8e22dc-c8e1-4d79-82a7-9f6f6625b093.png">

And click save rules.

<h3>Step 5</h3>

Now you should have two inbounds one for HTTP and one you just created SSH security group.

<img width="1361" alt="Step 5" src="https://user-images.githubusercontent.com/126012715/231766206-eba2700f-4b65-4dac-88d5-8c32683a19e0.png">


<h3>Step 6</h3>

Now to connect to the terminal and the cloud. 
By clicking connect, it should pop up with the following page in step 7.

![step 2.png](..%2F..%2F..%2FDesktop%2FAWS%20Security%20Group%2Fstep%202.png)

<h3>Step 7</h3>

Now you would want to click the SSH client tab, as you just created the SSH security file in inbounds.
You can use the steps provided to enter it onto your bash terminal.

<img width="846" alt="7" src="https://user-images.githubusercontent.com/126012715/231766311-2753bbe2-c54e-40e1-a95d-020a3116008f.png">


<h3>Step 8 </h3>

Locate the folder of your SSH key in terminal.

Adding the:

    `chmod 400 tech221.pem` 

which runs the command to ensure your key is not publicly viewable.

Then use the 

    `ssh -i "tech221.pem" ubuntu@ec2-34-242-60-20.eu-west-1.compute.amazonaws.com` 

which establishes the connection from the local server
to the ubuntu AWS server.

<img width="578" alt="adding to terminal from aws" src="https://user-images.githubusercontent.com/126012715/231766360-e2ef77aa-752e-4f83-96fd-ae003fffc8fc.png">


<h3>Final Step</h3>

Once it is authenticated, it should connect your local to the ubuntu server privately.
Which outputs your valid IP and ubuntu can be accessed from your terminal which in turn connects to the cloud.

<img width="568" alt="IP Address" src="https://user-images.githubusercontent.com/126012715/231766416-807340db-4866-40f7-8680-2058be36921b.png">
