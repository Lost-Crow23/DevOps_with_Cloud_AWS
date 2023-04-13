<h1>AWS Security Group </h1>

These are the steps to create a new SSH key instance, through the EC2 dashboard.

<h3>Step 1</h3>

We click the instances under the instances tab and click your name. 

![Picking a new instance.png](..%2F..%2F..%2FDesktop%2FAWS%20Security%20Group%2FPicking%20a%20new%20instance.png)

<h3>Step 2</h3>

Click the security tab to open up the security group.

![step 2.png](..%2F..%2F..%2FDesktop%2FAWS%20Security%20Group%2Fstep%202.png)

<h3>Step 3</h3>

Once opened, you need to edit the inbound to create a ssh security group.

![step 3.png](..%2F..%2F..%2FDesktop%2FAWS%20Security%20Group%2Fstep%203.png)

<h3>Step 4</h3>

Edit your inbound to add a rule thus creating your SSH security file. And under custom, select your personal 
IP address.

![step 4.png](..%2F..%2F..%2FDesktop%2FAWS%20Security%20Group%2Fstep%204.png)

And click save rules.

![Select SSH.png](..%2F..%2F..%2FDesktop%2FAWS%20Security%20Group%2FSelect%20SSH.png)

<h3>Step 5</h3>

Now you should have two inbounds one for HTTP and one you just created SSH security group.

![2 inbounds.png](..%2F..%2F..%2FDesktop%2FAWS%20Security%20Group%2F2%20inbounds.png)

<h3>Step 6</h3>

Now to connect to the terminal and the cloud. 
By clicking connect, it should pop up with the following page in step 7.

![step 2.png](..%2F..%2F..%2FDesktop%2FAWS%20Security%20Group%2Fstep%202.png)

<h3>Step 7</h3>

Now you would want to click the SSH client tab, as you just created the SSH security file in inbounds.
You can use the steps provided to enter it onto your bash terminal.

![Connecting using terminal.png](..%2F..%2F..%2FDesktop%2FAWS%20Security%20Group%2FConnecting%20using%20terminal.png)

<h3>Step 8 </h3>

Locate the folder of your SSH key in terminal.

Adding the:

    `chmod 400 tech221.pem` 

which runs the command to ensure your key is not publicly viewable.

Then use the 

    `ssh -i "tech221.pem" ubuntu@ec2-34-242-60-20.eu-west-1.compute.amazonaws.com` 

which establishes the connection from the local server
to the ubuntu AWS server.

![adding to terminal from aws.png](..%2F..%2F..%2FDesktop%2FAWS%20Security%20Group%2Fadding%20to%20terminal%20from%20aws.png)

<h3>Final Step</h3>

Once it is authenticated, it should connect your local to the ubuntu server privately.
Which outputs your valid IP and ubuntu can be accessed from your terminal which in turn connects to the cloud.

![IP Address.png](..%2F..%2F..%2FDesktop%2FAWS%20Security%20Group%2FIP%20Address.png)