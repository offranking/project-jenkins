# project-jenkins
Introduction to jenkins

Open your aws.. by login into it and navigate to your EC2 instance
<img width="722" height="296" alt="Screenshot 2025-07-11 at 9 52 03 pm" src="https://github.com/user-attachments/assets/c3679795-a2f9-43bc-8678-ae99d1dad6af" />

#####Create a new EC2 instance and launch it using the Ubuntu operating system.

<img width="1354" height="559" alt="Screenshot 2025-07-11 at 9 53 31 pm" src="https://github.com/user-attachments/assets/f0652b08-08e4-400f-8de8-617b2f0ae4eb" />

Now, create a key pair and configure your security group to allow traffic, then launch your instance.

<img width="926" height="708" alt="Screenshot 2025-07-11 at 9 55 08 pm" src="https://github.com/user-attachments/assets/9b23088b-3e61-4af6-b9b0-ac894777d316" />

Now, connect to your computer using the SSH key you downloaded from AWS.
First, open your terminal and navigate to the directory where the key file is saved. For example cd ~/Downloads

<img width="852" height="93" alt="Screenshot 2025-07-11 at 10 01 17 pm" src="https://github.com/user-attachments/assets/f7a0c692-3000-4915-9841-7828a91c8dd6" />

Next, set the correct permissions for your SSH key by running the following command chmod 400 "newubuntu-server.pem"

<img width="1051" height="158" alt="Screenshot 2025-07-11 at 10 01 49 pm" src="https://github.com/user-attachments/assets/b9de5560-a487-4c10-a516-9a5e4bb29d3b" />


Now that you’re connected to your AWS instance via SSH from your local terminal, the next step is to update the package list.
Run the following command: sudo apt update

This ensures your system has the latest package information before installing any new software.

<img width="1059" height="896" alt="Screenshot 2025-07-11 at 4 35 55 pm" src="https://github.com/user-attachments/assets/568b55ca-aa8c-423a-bbab-efe48b5e3fe8" />

<img width="1013" height="263" alt="Screenshot 2025-07-11 at 4 37 21 pm" src="https://github.com/user-attachments/assets/d52e1b4e-8a2f-4b01-9ac2-5ff41e2b137a" />

Install JDK
run "sudo apt install default-jdk-headless"

<img width="1406" height="371" alt="Screenshot 2025-07-11 at 4 38 19 pm" src="https://github.com/user-attachments/assets/aaeeaa02-fba4-4a29-998a-f875dbfe46d2" />

now install jenkins with the following command 
    wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
    sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > \
    /etc/apt/sources.list.d/jenkins.list'
    sudo apt update
    sudo apt-get install jenkins
    
<img width="1150" height="385" alt="Screenshot 2025-07-11 at 4 40 01 pm" src="https://github.com/user-attachments/assets/947205c5-701d-4922-8120-20e3fc960133" />

sudo systemctl status jenkins

<img width="1440" height="425" alt="Screenshot 2025-07-11 at 4 40 48 pm" src="https://github.com/user-attachments/assets/ab7b7a19-db1f-4077-b3ba-ba901ff854f0" />

on our jenkins instance , create new inbound rules for port 8080 in the security group


<img width="1440" height="783" alt="Screenshot 2025-07-11 at 4 45 03 pm" src="https://github.com/user-attachments/assets/b64bc79b-a401-4120-b656-3b88abd16acc" />

Next, you’ll need to set up Jenkins through the web interface.
Open your browser and enter your Jenkins instance’s public IP address followed by port 8080. For example: http://your-public-ip-address:8080



<img width="1196" height="698" alt="Screenshot 2025-07-11 at 5 21 28 pm" src="https://github.com/user-attachments/assets/dc4df5f2-bea8-4479-b388-6ca920248a02" />



Now we have to view the password by "at /var/lib/jenkins/secrets/initialAdminPassword"

<img width="1044" height="104" alt="Screenshot 2025-07-11 at 5 23 06 pm" src="https://github.com/user-attachments/assets/87bf5790-1607-42eb-9ee4-a992a700e980" />



Creating first admin user

<img width="1083" height="693" alt="Screenshot 2025-07-11 at 5 25 20 pm" src="https://github.com/user-attachments/assets/347ca178-158c-4199-8ac3-0f7a003975ef" />

Login to the Jenkins console

<img width="992" height="683" alt="Screenshot 2025-07-11 at 5 25 41 pm" src="https://github.com/user-attachments/assets/1872e914-ad7a-4234-aca7-4b7859c87e65" />



<img width="984" height="587" alt="Screenshot 2025-07-11 at 5 26 30 pm" src="https://github.com/user-attachments/assets/7f265c88-1524-4ed9-9646-b77034327ae8" />

<img width="1417" height="736" alt="Screenshot 2025-07-11 at 5 27 24 pm" src="https://github.com/user-attachments/assets/9934221b-30e2-4793-9d8e-94be92945749" />

