<h1>Automation of Nginx</h1>

<h3>Step 1</h3>

Within the virtual environment and the ssh folder.

Creating an enabling a shell script within git bash terminal

`sudo touch provision.sh`

- This creates a file within the ssh folder.

<h3>Step 2</h3>

- Open the file within the folder.

`sudo nano provision.sh`

<h3>Step 3</h3>

- Once opened enter the following as commands within the file.

<img width="592" alt="provision_ssh" src="https://user-images.githubusercontent.com/126012715/232351327-44ba8342-215f-4bdf-a9d3-6fa7e0209312.png">

<h3>Step 4</h3>

`Cntrl X or C` to save the file then type `Yes` as prompted.

<h3>Step 5</h3>

- Permission can be changed using `Sudo chmod += provision.sh` to make file executable.

- Run and Check the status of the script `sudo ./provision.sh` and then `sudo systemctl status nginx`

<h3>Final Iteration</h3>

- Copy the IP address as shown under details in the instance and paste it as a new URL. 

<img width="846" alt="Welcome to nginx!" src="https://user-images.githubusercontent.com/126012715/232351414-e632d8ee-f292-4f08-ad5b-5245c14781c6.png">

