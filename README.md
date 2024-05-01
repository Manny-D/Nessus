# Nessus
![Nessus Banner](https://github.com/Manny-D/Nessus/assets/99146530/dc9fe6f8-a05f-4617-ba29-d20f2613eb7d)



## Description 

In this project, I will go through the process of installing Nessus Essentials in a Kali Linux VM, then perform a Vulnerability Scan. 

<br/>


## Installation 

Step #1 <br>

Goto [https://www.tenable.com/products/nessus/nessus-essentials](https://www.tenable.com/products/nessus/nessus-essentials) and register an account.

![Register for an Activation Code](https://github.com/Manny-D/Nessus/assets/99146530/712d3226-b404-4e1e-aacb-80056111d228)

You will need to do this for an activation code.

<br>

Step #2 <br>

Download the Nessus-#.##.#-debian6_amd64.deb file -> save it to the <b>/Downloads/</b> folder.

![Debian file](https://github.com/Manny-D/Nessus/assets/99146530/1e706a66-c29b-4881-b847-ede800cfe794)

<br>

Step #3 <br>

Open a Kali terminal, navigate to the <b>/Downloads/</b> folder and run the following command:
<b>sudo dpkg -i package_file.deb</b>

![Nessus debian file install on Kali](https://github.com/Manny-D/Nessus/assets/99146530/e681436d-9657-4bd8-b6be-78c54a02abec)

<b>Note</b>: be sure to replace package_file.deb with the file name you downloaded!

<br>

Step #4 

Start the Nessus Service with the following command: <br>
<b>sudo /bin/systemctl start nessusd.service</b> <br>

![Starting Nessus](https://github.com/Manny-D/Nessus/assets/99146530/ad2fa72f-b52d-4bc4-b7af-e74ecf59ebc7)

<br>

Step #5

Open Firefox and navigate to the following URL:
https://localhost:8834/

If prompted with a security risk alert -> click <b>Advanced...</b> -> click <b>Accept the Risk and Continue</b>

![Warning Potential Security Risk Ahead](https://github.com/Manny-D/Nessus/assets/99146530/1e5bb3f0-5212-4227-8009-52bb3aad68fc)

<br>

Step #6

To set up the scanner, select the <b>Nessus Essentials</b> radio button. 

![Nessus Essentials radio](https://github.com/Manny-D/Nessus/assets/99146530/fed84959-abf4-466f-83db-7b9f6d134e84)

Click the Skip button. It will load the following page where we can input the code we received in the email from Nessus in Step #1.

![Activation Code](https://github.com/Manny-D/Nessus/assets/99146530/5cb0fdd2-bbdc-40fa-b2f2-bbbd0e58b33d)

Enter the <b>Activation Code</b> -> <b>Continue</b>

<br>

Step #7

Create a Nessus administrator account and note your credentials. 

![Admin account creation](https://github.com/Manny-D/Nessus/assets/99146530/d7a0202c-d9e3-4401-bdb2-6d42ba5a8177)

<br>

Step #8

Required plugins will be downloaded which will take some time.

![Downloading plugins](https://github.com/Manny-D/Nessus/assets/99146530/a5c07c83-070c-4fe1-b7db-13db746b36ef)

<b>Note</b>: If the progress bar is not moving, it means you do not have enough space on the VM to install.

<br>

Step #9

Log in with the admin account credentials created in Step #7.

![Login](https://github.com/Manny-D/Nessus/assets/99146530/b0dc39a4-1903-4741-8b81-37a266152f8c)

<br>

Step #10

Installation completed!

![Installed](https://github.com/Manny-D/Nessus/assets/99146530/e7b4c849-541a-48a9-9dd8-4987aa7ca448)

<br>

## Scanning

