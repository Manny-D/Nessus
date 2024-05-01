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

In the Scan Templates section, there is a list of pre-defined templates (as seen below). 

![Scan Templates](https://github.com/Manny-D/Nessus/assets/99146530/f113d3d2-9126-4555-a900-36ea0ff04ef7)

<br>

### Basic Network Scan
Click on <b>Basic Network Scan</b> and on the page that follows, enter in a name (anything you want) and enter the IP(s) of your Targets (eg. what you want to scan). 

![New Scan](https://github.com/Manny-D/Nessus/assets/99146530/9db116a2-b566-47b9-9c43-5476a693865f)

Next, click Save (bottom left corner) and we'll be taken to My Scans page. Start the scan by pressing the icon to the right that looks like a play button. 

![Test Scan](https://github.com/Manny-D/Nessus/assets/99146530/02e2e95e-16bd-451f-a5b1-9eab801158c5)

Once completed, a check will appear and we can view the results.

<br>

### Scan Results

![Results Pane](https://github.com/Manny-D/Nessus/assets/99146530/85df538a-56ea-4e65-9038-c5e88f50040c)

This results pane provides all of the information the scan collected. On the left there is list of hosts scanned, then a summary of any vulnerabilities discovered. If we were scanning an entire network, this would likely contain various hosts. Also, the vulnerabilities are arranged by criticality by default. On the right are the Scan Details and below it is a donut chart of identified security issues. We can click on the Vulnerabilities tab to see what the Nessus discovered.

<br>

![Vulnerabilities](https://github.com/Manny-D/Nessus/assets/99146530/1a8a49ec-d188-43a0-b432-42be2b80f980)

Here, any of the rows can be ordered by clicking on them. We can also gain more insight on a vulnerability by clicking on any one of them. 

<br>

![SSL](https://github.com/Manny-D/Nessus/assets/99146530/3d6c0467-f7ee-4957-b275-969e36f77597)

This page gives a description of the issue, the plugin used to detect it, and risk information. Solution(s) to address the issue are usually found below the description. As a best practice when contacting a system owner after a scan's completion, we should attach an exported .pdf and add a summary including hosts, issues and remediation steps. 
